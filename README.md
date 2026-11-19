
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]# sed -n '120,140p' $B/conf/login-config.xml | sed -E 's#(name="password">)[^<]*#\1***#I'
    that will be used when a null username and password are presented as is
    the case for an unuathenticated web client or MDB. If you want to
    allow such users to be authenticated add the property, e.g.,
    unauthenticatedIdentity="nobody"
    -->
   <!-- <authentication>
      <login-module code="org.jboss.security.auth.spi.UsersRolesLoginModule"
        flag="required"/>
    </authentication> -->
</application-policy>

 <!-- SecureIdentityLoginModule Datasource usado para o SIGSJ em desenvolvimento -->
  <application-policy name="SIGSJDSEncrypt">
     <authentication>
        <login-module flag="required" code="org.jboss.resource.security.SecureIdentityLoginModule">
           <module-option name="username">SGSJSD01</module-option>
           <module-option name="password">***</module-option>
           <module-option name="managedConnectionFactoryName">jboss.jca:name=jdbc/SIGSJ04,service=LocalTxCM</module-option>
        </login-module>
     </authentication>
  </application-policy>
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
[root@sspdeapllx0039 lib]#
