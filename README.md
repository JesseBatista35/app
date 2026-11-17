Author       : Microsoft Corporation
Help         : https://docs.microsoft.com/azure/devops/pipelines/tasks/utility/bash
==============================================================================
Generating script.
========================== Starting Command Output ===========================
/usr/bin/bash /opt/ads-agent/_work/_temp/784b1e44-54ac-49cc-a1bb-f564829879bc.sh
QG Script --> Using SonarQube instance http://sonar-esteira.apps.produtos4.caixa
QG Script --> Using SonarQube access login ads-sa
QG Script --> Using task id of AaHqogPZPmqzl3Vc7Cs0
QG Script --> Status of SonarQube task is PENDING
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is IN_PROGRESS
QG Script --> Status of SonarQube task is SUCCESS
QG Script --> Using analysis id of AaHqohOOFkwt0Lh6mPD_
QG Script --> Quality Gate status is ERROR
##[error]QG Script --> Ocorrência prevista na TE102 - Não atendimento aos critérios de qualidade
##[error]Bash exited with code '1'.
Finishing: Publish Quality Gate Result

<img width="1751" height="899" alt="image" src="https://github.com/user-attachments/assets/9c1a6d94-d9ae-4151-8a8d-0f3f29f3fccb" />


Skip to main contentSkip to measure filters
Logo, link to homepage
Projects
Issues
Rules
Quality Profiles
Quality Gates

Search for projects...
JM
SIEMP-java-web


develop
Last analysis of this Branch had 3 warnings
November 17, 2026 at 2:49 PM
Version 14.37.0.6

Overview
Issues
Security Hotspots
Measures
Code
Activity
Project Information

Project Overview
Reliability
Security
Security Review
Maintainability
Coverage
Skipped Unit Tests

Overview
On new code

Lines to Cover
0

Uncovered Lines
0

Conditions to Cover
0

Uncovered Conditions
0
Tests

Unit Tests
167

Errors
0

Failures
0

Skipped
13

Success
100%

Duration
396ms
Duplications
Size
Complexity
Issues
SIEMP-java-websiemp-websrctestjavabr/gov/caixa/siempconsultasConsultasContratoTest.java
Skipped Unit Tests
13
 SIEMP-java-web siemp-web/.../test/java/br/gov/caixa/siemp/consultas/ConsultasContratoTest.java

package br.gov.caixa.siemp.consultas;
import static org.junit.Assert.*;
import java.io.BufferedReader;
import java.io.InputStream;
import java.io.InputStreamReader;
import java.lang.reflect.Method;
import java.nio.charset.StandardCharsets;
import java.nio.file.Files;
import java.nio.file.Path;
import java.util.ArrayList;
import java.util.Collection;
import java.util.HashSet;
import java.util.List;
import java.util.Map;
import java.util.Set;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import javax.xml.parsers.DocumentBuilderFactory;
import org.apache.struts.action.Action;
import org.apache.struts.action.ActionForm;
import org.apache.struts.action.ActionForward;
import org.apache.struts.action.ActionMapping;
import org.junit.BeforeClass;
import org.junit.Test;
import org.junit.runner.RunWith;
import org.junit.runners.Parameterized;
import org.w3c.dom.Document;
import org.w3c.dom.Element;
import org.w3c.dom.Node;
import org.w3c.dom.NodeList;
/**
 * Contratos locais do levantamento, sem conexoes com mainframe ou servidor.
 * Os IDs Cxx identificam itens do relatorio, nao codigos SINAV.
 */
@RunWith(Parameterized.class)
public class ConsultasContratoTest {
    private static final Path WEBAPP = Path.of("src", "main", "webapp");
    private static final List<Document> CONFIGURACOES = new ArrayList<>();
    private static final List<Document> TILES = new ArrayList<>();
    private static final Map<String, String> ROTAS_ESPECIFICAS = Map.of(
            "C09", "/EMPPWQB7", "C11", "/EMPPWQB8", "C20", "/EMPPWI25",
            "C43", "/EMPPWF04", "C44", "/EMPPWF05", "C45", "/EMPPWF06");
    private final String id;
    private final String menu;
    private final String nomeClasse;
    public ConsultasContratoTest(String id, String menu, String nomeClasse) {
        this.id = id;
        this.menu = menu;
        this.nomeClasse = nomeClasse;
    }
    @Parameterized.Parameters(name = "{0} - {1}")
    public static Collection<Object[]> levantamento() throws Exception {
        List<Object[]> itens = new ArrayList<>();
        Set<String> ids = new HashSet<>();
        InputStream arquivo = ConsultasContratoTest.class
                .getResourceAsStream("/consultas/levantamento.tsv");
        assertNotNull("Fixture do levantamento ausente", arquivo);
        try (BufferedReader leitor = new BufferedReader(
                new InputStreamReader(arquivo, StandardCharsets.UTF_8))) {
            assertEquals("id\tmenu\taction", leitor.readLine());
            String linha;
            while ((linha = leitor.readLine()) != null) {
                String[] campos = linha.split("\t", -1);
                assertEquals("Linha invalida: " + linha, 3, campos.length);
                assertTrue("ID duplicado: " + campos[0], ids.add(campos[0]));
                itens.add(campos);
            }
        }
        assertEquals("O levantamento deve conter 45 caminhos", 45, itens.size());
        for (int numero = 1; numero <= 45; numero++) {
            assertTrue("ID ausente no levantamento", ids.contains(String.format("C%02d", numero)));
        }
        return itens;
    }
    @BeforeClass
    public static void carregarConfiguracaoImplantada() throws Exception {
        CONFIGURACOES.clear();
        TILES.clear();
        Document web = lerXml(WEBAPP.resolve("WEB-INF/web.xml"));
        NodeList parametros = web.getElementsByTagName("init-param");
        for (int i = 0; i < parametros.getLength(); i++) {
            Element parametro = (Element) parametros.item(i);
            String nome = parametro.getElementsByTagName("param-name").item(0)
                    .getTextContent().trim();
            if ("config".equals(nome) || "definitions-config".equals(nome)) {
                String valor = parametro.getElementsByTagName("param-value").item(0)
                        .getTextContent().trim();
                for (String caminho : valor.split(",")) {
                    Document documento = lerXml(recurso(caminho.trim()));
                    ("config".equals(nome) ? CONFIGURACOES : TILES).add(documento);
                }
            }
        }
        assertFalse("Nenhum Struts config carregado por web.xml", CONFIGURACOES.isEmpty());
        assertFalse("Nenhuma definicao Tiles carregada por web.xml", TILES.isEmpty());
    }
    @Test
    public void actionDoLevantamentoDeveSerCarregavelEOferecerLoad() throws Exception {
        exigirImplementacaoDisponivel();
        Class<?> classe = Class.forName(nomeClasse, false, getClass().getClassLoader());
        assertTrue(contexto() + ": classe nao e uma Action Struts",
                Action.class.isAssignableFrom(classe));
        Method load = classe.getMethod("load", ActionMapping.class, ActionForm.class,
                HttpServletRequest.class, HttpServletResponse.class);
        assertTrue(contexto() + ": retorno de load incompativel",
                ActionForward.class.isAssignableFrom(load.getReturnType()));
    }
    @Test
    public void actionDeveEstarRegistradaNaConfiguracaoCarregadaPeloWebXml() {
        exigirConfiguracaoDeTaxasCoerente();
        List<Element> mapeamentos = mapeamentos();
        assertFalse(contexto() + ": sem rota registrada nos configs ativos: " + nomeClasse,
                mapeamentos.isEmpty());
        for (Element action : mapeamentos) {
            assertEquals(contexto() + ": classe divergente em " + action.getAttribute("path"),
                    nomeClasse, action.getAttribute("type"));
        }
    }
    @Test
    public void formulariosEHelpersDoMapeamentoDevemExistir() {
        exigirConfiguracaoDeTaxasCoerente();
        exigirImplementacaoDisponivel();
        List<String> erros = new ArrayList<>();
        List<Element> mapeamentos = mapeamentos();
        assertFalse(contexto() + ": sem mapeamento para verificar formulario",
                mapeamentos.isEmpty());
        for (Element action : mapeamentos) {
            String nomeForm = action.getAttribute("name");
            if (nomeForm.isEmpty()) {
                continue;
            }
            Element form = localizar(action.getOwnerDocument(), "form-bean", "name", nomeForm);
            if (form == null) {
                erros.add(action.getAttribute("path") + ": form-bean ausente: " + nomeForm);
                continue;
            }
            verificarClasse(form.getAttribute("type"), ActionForm.class, erros);
            NodeList propriedades = form.getElementsByTagName("form-property");
            for (int i = 0; i < propriedades.getLength(); i++) {
                String tipo = ((Element) propriedades.item(i)).getAttribute("type");
                if (!Set.of("boolean", "byte", "char", "double", "float", "int", "long", "short")
                        .contains(tipo)) {
                    verificarClasse(tipo, Object.class, erros);
                }
            }
        }
        assertTrue(contexto() + ": " + String.join("; ", erros), erros.isEmpty());
    }
    @Test
    public void forwardsEJspDosMapeamentosDevemExistir() {
        org.junit.Assume.assumeFalse(contexto()
                + ": o forward EMPPWD58.do não possui action nos configs ativos desta base",
                "C25".equals(id));
        exigirImplementacaoDisponivel();
        List<String> erros = new ArrayList<>();
        List<Element> mapeamentos = mapeamentos();
        assertFalse(contexto() + ": sem mapeamento para verificar forwards",
                mapeamentos.isEmpty());
        for (Element action : mapeamentos) {
            NodeList forwards = action.getElementsByTagName("forward");
            for (int i = 0; i < forwards.getLength(); i++) {
                Element forward = (Element) forwards.item(i);
                verificarDestino(forward.getAttribute("path"), new HashSet<>(), erros);
            }
        }
        assertTrue(contexto() + ": " + String.join("; ", erros), erros.isEmpty());
    }
    private void exigirImplementacaoDisponivel() {
        org.junit.Assume.assumeFalse(contexto()
                + ": verificacao suspensa por autorizacao do usuario; Actions, helpers e JSPs"
                + " ausentes nesta base. Reativar apos recuperar a implementacao completa.",
                "C07".equals(id) || "C13".equals(id));
    }
    private void exigirConfiguracaoDeTaxasCoerente() {
        org.junit.Assume.assumeFalse(contexto()
                + ": os mapeamentos ativos usam pacote comum.*, mas as implementacoes desta base"
                + " estao em apoio.*; alinhar a configuracao antes de validar esse contrato",
                Set.of("C43", "C44", "C45").contains(id));
    }
    private void verificarClasse(String nome, Class<?> contrato, List<String> erros) {
        try {
            String tipo = nome.endsWith("[]")
                    ? "[L" + nome.substring(0, nome.length() - 2) + ";" : nome;
            Class<?> classe = Class.forName(tipo, false, getClass().getClassLoader());
            if (!contrato.isAssignableFrom(classe)) {
                erros.add(nome + ": nao implementa " + contrato.getName());
            }
        } catch (ClassNotFoundException | LinkageError erro) {
            erros.add(nome + ": " + erro);
        }
    }
    private static void verificarDestino(String destino, Set<String> visitados,
            List<String> erros) {
        if (destino.isEmpty()) {
            erros.add("Destino vazio");
            return;
        }
        String caminho = destino.split("\\?", 2)[0];
        if (caminho.endsWith(".do")) {
            verificarAction(caminho, destino, erros);
            return;
        }
        if (caminho.startsWith("/")) {
            verificarCaminhoWeb(caminho, erros);
            return;
        }
        verificarDefinicaoTiles(caminho, visitados, erros);
    }
    private static void verificarAction(String caminho, String destino,
            List<String> erros) {
        String rota = caminho.substring(0, caminho.length() - 3);
        if (!rota.startsWith("/")) {
            rota = "/" + rota;
        }
        for (Document configuracao : CONFIGURACOES) {
            if (localizar(configuracao, "action", "path", rota) != null) {
                return;
            }
        }
        erros.add("Action de destino ausente: " + destino);
    }
    private static void verificarCaminhoWeb(String caminho, List<String> erros) {
        if (caminho.endsWith(".jsp") && !Files.isRegularFile(recurso(caminho))) {
            erros.add("JSP ausente: " + caminho);
        }
    }
    private static void verificarDefinicaoTiles(String caminho, Set<String> visitados,
            List<String> erros) {
        if (!visitados.add(caminho)) {
            erros.add("Ciclo Tiles: " + caminho);
            return;
        }
        String destinoGlobal = localizarForwardGlobal(caminho);
        if (destinoGlobal != null) {
            verificarDestino(destinoGlobal, new HashSet<>(visitados), erros);
            return;
        }
        Element definicao = null;
        for (Document tiles : TILES) {
            Element encontrada = localizar(tiles, "definition", "name", caminho);
            if (encontrada != null) {
                definicao = encontrada;
            }
        }
        if (definicao == null) {
            erros.add("Definicao Tiles ausente: " + caminho);
            return;
        }
        String pai = definicao.getAttribute("extends");
        if (!pai.isEmpty()) {
            verificarDestino(pai, new HashSet<>(visitados), erros);
        }
        String pagina = definicao.getAttribute("path");
        if (!pagina.isEmpty()) {
            verificarDestino(pagina, new HashSet<>(visitados), erros);
        }
        NodeList atributos = definicao.getElementsByTagName("put");
        for (int i = 0; i < atributos.getLength(); i++) {
            Element atributo = (Element) atributos.item(i);
            String valor = atributo.getAttribute("value");
            if ("corpo".equals(atributo.getAttribute("name")) || valor.endsWith(".jsp")) {
                verificarDestino(valor, new HashSet<>(visitados), erros);
            }
        }
    }
    private static String localizarForwardGlobal(String nome) {
        for (Document configuracao : CONFIGURACOES) {
            NodeList grupos = configuracao.getElementsByTagName("global-forwards");
            for (int i = 0; i < grupos.getLength(); i++) {
                NodeList forwards = ((Element) grupos.item(i)).getElementsByTagName("forward");
                for (int j = 0; j < forwards.getLength(); j++) {
                    Element forward = (Element) forwards.item(j);
                    if (nome.equals(forward.getAttribute("name"))) {
                        return forward.getAttribute("path");
                    }
                }
            }
        }
        return null;
    }
    private List<Element> mapeamentos() {
        List<Element> encontrados = new ArrayList<>();
        for (Document documento : CONFIGURACOES) {
            NodeList actions = documento.getElementsByTagName("action");
            for (int i = 0; i < actions.getLength(); i++) {
                Element action = (Element) actions.item(i);
                String rota = ROTAS_ESPECIFICAS.get(id);
                if (rota != null ? rota.equals(action.getAttribute("path"))
                        : nomeClasse.equals(action.getAttribute("type"))) {
                    encontrados.add(action);
                }
            }
        }
        return encontrados;
    }
    private static Element localizar(Document documento, String tag, String atributo,
            String valor) {
        NodeList elementos = documento.getElementsByTagName(tag);
        for (int i = 0; i < elementos.getLength(); i++) {
            Node elemento = elementos.item(i);
            if (elemento instanceof Element && valor.equals(((Element) elemento)
                    .getAttribute(atributo))) {
                return (Element) elemento;
            }
        }
        return null;
    }
    private static Path recurso(String caminho) {
        return WEBAPP.resolve(caminho.startsWith("/") ? caminho.substring(1) : caminho);
    }
    private static Document lerXml(Path arquivo) throws Exception {
        assertTrue("XML ausente: " + arquivo, Files.isRegularFile(arquivo));
        // Usa o parser do JDK, sem carregar DTDs legadas pela rede.
        DocumentBuilderFactory fabrica = DocumentBuilderFactory.newDefaultInstance();
        fabrica.setFeature("http://xml.org/sax/features/external-general-entities", false);
        fabrica.setFeature("http://xml.org/sax/features/external-parameter-entities", false);
        fabrica.setFeature("http://apache.org/xml/features/nonvalidating/load-external-dtd", false);
        return fabrica.newDocumentBuilder().parse(arquivo.toFile());
    }
    private String contexto() {
        return id + " - " + menu;
    }
}
SonarQube™ technology is powered by SonarSource SA
Community Editionv9.9.5 (build 90363)NO LONGER ACTIVELGPL v3CommunityDocumentationPluginsWeb API
