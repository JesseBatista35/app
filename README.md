group_id:artifact_id:version:extension
br.gov.caixa.siusr:siusr-loginModule:1.11.0:jar
br.gov.caixa.siusr:siusr-loginModule:1.11.0:jar

module add --name=br.gov.caixa.siusr --resource-delimiter=, --resources=/tmp/siusr-loginModule-1.11.0.jar --dependencies=javax.api,sun.jdk,org.apache.commons.lang,javaee.api,org.picketbox



package br.gov.caixa.pr.sicow.conres.ws;

import java.net.InetAddress;

import javax.annotation.Resource;
import javax.ejb.EJB;
import javax.ejb.Stateless;
import javax.jws.WebMethod;
import javax.jws.WebParam;
import javax.jws.WebResult;
import javax.jws.WebService;
import javax.jws.soap.SOAPBinding;
import javax.servlet.http.HttpServletRequest;
import javax.xml.bind.annotation.XmlSeeAlso;
import javax.xml.ws.WebServiceContext;
import javax.xml.ws.handler.MessageContext;

import org.apache.commons.lang3.StringUtils;
import org.jboss.ws.api.annotation.WebContext;

import br.gov.caixa.pr.sicow.conres.dao.SistemaWSDAO;
import br.gov.caixa.pr.sicow.conres.entity.Servidor;
import br.gov.caixa.pr.sicow.conres.entity.Sistema;
import br.gov.caixa.pr.sicow.conres.entity.WsServicosSistema;
import br.gov.caixa.pr.sicow.service.ws.ServicosWebService;
import br.gov.caixa.pr.ws.HeaderConresWS;
import br.gov.caixa.pr.ws.ObjectFactory;
import br.gov.caixa.pr.ws.ObjectFactoryConres;
import br.gov.caixa.pr.ws.ServicoEntradaDadosConresWS;
import br.gov.caixa.pr.ws.ServicoSaidaDadosConresWS;

@Stateless
@WebService(name = "SicowconresWS", serviceName = "OcorrenciaConresWS")
@SOAPBinding(style = SOAPBinding.Style.DOCUMENT, use = SOAPBinding.Use.LITERAL, parameterStyle = SOAPBinding.ParameterStyle.WRAPPED)
@WebContext(contextRoot = "/sicow-conres", urlPattern = "/OcorrenciaConresWS/SicowconresWS")
@XmlSeeAlso({ ObjectFactory.class, ObjectFactoryConres.class })
public class OcorrenciaConresWS extends ServicosWebService {

	private static final long serialVersionUID = 1L;
	private static final String SISTEMA_PREFIXO = "Sistema: ";
	@EJB
	private SistemaWSDAO sistemaDao;

	@Resource
	private transient WebServiceContext context;

	private Sistema sistema = null;

	private transient ServicoSaidaDadosConresWS saidaConresWS = new ServicoSaidaDadosConresWS();

	@Override
	public boolean equals(Object object) {
		return super.equals(object);
	}

	@Override
	public int hashCode() {
		return super.hashCode();
	}

	@WebMethod(operationName = "OCORRENCIA")
	@WebResult(name = "SERVICO_SAIDA", partName = "parameters")
	public ServicoSaidaDadosConresWS consultaOCORRENCIA(
			@WebParam(name = "SERVICO_ENTRADA", partName = "parameters") ServicoEntradaDadosConresWS parameters) {
		try {
			saidaConresWS = new ServicoSaidaDadosConresWS();
			if (parameters == null || parameters.getHeader() == null || parameters.getDados() == null) {
				return null;
			}
			if (parameters.getDados().getConsultaOcorrenciaCpf() != null) {
				return processarServico(parameters, "consultarCpf");
			}
			if (parameters.getDados().getConsultaOcorrenciaCnpj() != null) {
				return processarServico(parameters, "consultarCnpj");
			}
			if (parameters.getDados().getInsertMotivo17() != null) {
				return processarServico(parameters, "incluirOcorrenciaMotivo17");
			}
			if (parameters.getDados().getInsertMotivo18() != null) {
				return processarServico(parameters, "incluirOcorrenciaMotivo18");
			}

		} catch (Exception e) {
			this.saidaConresWS
					.setMsgretorno("Ocorreu um erro inesperado. Entre em contato com o administrador do sistema");
			return saidaConresWS;
		}

		return null;

	}

	private ServicoSaidaDadosConresWS processarServico(ServicoEntradaDadosConresWS parameters, String tipoServico) {
		if (!validateHeader(parameters.getHeader(), tipoServico)) {
			return saidaConresWS;
		}
		parameters.getDados().setIp(getIP());
		parameters.getDados().setHost(getHost());
		if ("consultarCpf".equals(tipoServico)) {
			return geraConsultaOcorrenciaPorCPF(parameters);
		}
		if ("consultarCnpj".equals(tipoServico)) {
			return geraConsultaOcorrenciaPorCNPJ(parameters);
		}
		return geraRetornoInsert(parameters);
	}

	private boolean validateHeader(HeaderConresWS header, String tipoServico) {
		if (header.getSistemaorigem() == null) {
			saidaConresWS.setMsgretorno("Campo SISTEMA_ORIGEM não pode estar vazio.");
			return false;
		}
		if (!validaSistema(header.getSistemaorigem())) {
			saidaConresWS.setMsgretorno("Sistema " + header.getSistemaorigem()
					+ " sem permissão para realizar a consulta no SICOW.");
			return false;
		}
		if (!validaWsServicoParaTipo(header.getSistemaorigem(), tipoServico)) {
			return false;
		}
		if (!validaServidor(header.getSistemaorigem())) {
			return false;
		}
		return validaSenha(header);
	}

	private boolean validaWsServicoParaTipo(String sistemaOrigem, String tipoServico) {
		if (sistema.getVinculoWsServSistema().isEmpty() || validaWsServico(tipoServico)) {
			return true;
		}
		saidaConresWS.setMsgretorno(SISTEMA_PREFIXO + sistemaOrigem + ", sem acesso ao serviço "
				+ tipoServico + " do SICOW.");
		return false;
	}

	private boolean validaServidor(String sistemaOrigem) {
		if (!Boolean.TRUE.equals(sistema.getIcServidor()) || validaIp(false)) {
			return true;
		}
		saidaConresWS.setMsgretorno(SISTEMA_PREFIXO + sistemaOrigem + ", IP:" + getIP()
				+ " sem permissão para realizar a consulta no SICOW.");
		return false;
	}

	private boolean validaSenha(HeaderConresWS header) {
		if (!Boolean.TRUE.equals(sistema.getIcPassword())) {
			return true;
		}
		if (StringUtils.isEmpty(header.getAutenticacao())) {
			saidaConresWS.setMsgretorno(SISTEMA_PREFIXO + header.getSistemaorigem()
					+ ", senha é obrigatória para realizar a consulta no SICOW.");
			return false;
		}
		if (!validaPassword(header.getSistemaorigem(), header.getAutenticacao())) {
			saidaConresWS.setMsgretorno(SISTEMA_PREFIXO + header.getSistemaorigem()
					+ ", senha incorreta para realizar a consulta no SICOW.");
			return false;
		}
		return true;
	}

	private boolean validaPassword(final String sgSistema, final String passWord) {
		if (saidaConresWS.getMsgretorno() == null) {
			sistema = this.sistemaDao.findSistema(sgSistema);
			if (sistema != null && sistema.getPassWordSistema().getDsPassword().equals(passWord)) {
				return true;
			}
		}
		return false;
	}

	private boolean validaSistema(final String sgSistema) {
		if (saidaConresWS.getMsgretorno() == null) {
			sistema = this.sistemaDao.findSistema(sgSistema);
			if (sistema != null) {
				return true;
			}
		}
		return false;
	}

	private boolean validaWsServico(final String wsServico) {
		if (saidaConresWS.getMsgretorno() == null) {
			for (WsServicosSistema ws : sistema.getVinculoWsServSistema()) {
				if (ws.getWsServico().getDsServico().equals(wsServico)) {
					return true;
				}
			}
		}
		return false;
	}

	private String getIP() {
		try {
			final HttpServletRequest request = (HttpServletRequest) context.getMessageContext()
					.get(MessageContext.SERVLET_REQUEST);
			if (request != null) {
				String ipAddress = request.getHeader("X-Forwarded-for");
				if (ipAddress != null) {
					return ipAddress;
				}
				return request.getRemoteAddr();
			}
		} catch (Exception e) {
			e.getCause();
		}
		return "";
	}

	private String getHost() {
		try {
			final HttpServletRequest request = (HttpServletRequest) context.getMessageContext()
					.get(MessageContext.SERVLET_REQUEST);
			if (request != null) {
				return getHost(request);
			}
		} catch (Exception e) {
			e.getCause();
		}
		return "";
	}

	private String getHost(final HttpServletRequest request) {
		try {
			String ipAddress = request.getHeader("X-Forwarded-for");
			if (ipAddress == null) {
				ipAddress = request.getRemoteAddr();
			}
			InetAddress inetAddress = InetAddress.getByName(ipAddress);
			if (inetAddress != null) {
				return inetAddress.getHostName();
			}
			return ipAddress;
		} catch (Exception e) {
			return "";
		}
	}

	private boolean validaIp(boolean servidorAtivo) {

		for (Servidor servidor : sistema.getServidor()) {
			if (servidor.getNuIp().contains("*")) {
				String[] splitServerIPAuthorized = servidor.getNuIp().split("[.]");
				String[] splitRemoteIP = getIP().split("[.]");
				if (splitServerIPAuthorized.length >= 3 && splitRemoteIP.length >= 3
						&& splitServerIPAuthorized[0].equals(splitRemoteIP[0])
						&& splitServerIPAuthorized[1].equals(splitRemoteIP[1])
						&& splitServerIPAuthorized[2].equals(splitRemoteIP[2])) {
					servidorAtivo = true;
				}
			} else if (servidor.getNuIp().equals(getIP()) && servidor.getIcAtivo().getBooleanValue()) {
				servidorAtivo = true;

			}
		}
		return servidorAtivo;
	}

	@WebMethod(exclude = true)
	public void setSistemaDao(SistemaWSDAO sistemaDao) {
		this.sistemaDao = sistemaDao;
	}

        void setContext(WebServiceContext context) {
                this.context = context;
        }

}
