Opção 1, mais rápida: incluir a propriedade abaixo no persistence.xml do sirur-ejb.jar, dentro do bloco <properties> das duas unidades, fec.pu e fec.rur.pu:

xml
<property name="hibernate.jpa.compliance.global_id_generators" value="false"/>
