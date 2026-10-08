Como confirmar (2 minutos)

Abra direto os dois arquivos na develop:
https://github.com/caixagithub/siobs-intra-administracaopingfederate/blob/develop/PostmanCollection/SIOBS-AppPingFederate.postman_environment.json
https://github.com/caixagithub/siobs-intra-administracaopingfederate/blob/develop/SiobsAppPingFederate/Database/DbInitializer.cs
No primeiro arquivo, dê Ctrl+F por access_token e veja se o campo value ainda tem o JWT. Esse é o alerta #8.
No segundo, dê Ctrl+F por HashedRefreshToken e veja se os valores dos cli-ser-oba e TaobfOykDNc7... ainda estão lá. Esses são os alertas #6 e #5.
Alternativa: na barra de busca do topo do GitHub, use repo:caixagithub/siobs-intra-administracaopingfederate HashedRefreshToken. Essa busca procura conteúdo, mas só na branch padrão.



{
	"id": "cfbfe59d-966e-444a-a467-3c0fda06e3f7",
	"name": "SIOBS-AppPingFederate",
	"values": [
		{
			"key": "api_host_des",
			"value": "apppingfederate-des.azurewebsites.net",
			"type": "default",
			"description": "",
			"enabled": true
		},
		{
			"key": "api_grants_path",
			"value": "api/AccessGrants",
			"type": "default",
			"description": "",
			"enabled": true
		},
		{
			"key": "api_host_local",
			"value": "localhost:5001",
			"type": "default",
			"description": "",
			"enabled": true
		},
		{
			"key": "access_token",
			"value": "eyJhbGciOiJSUzI1NiIsInR5cCIgOiAiSldUIiwia2lkIiA6ICJNRmVKNjVfRC14cU55M1Zta01Ib01WS1NjZlA3S21ZazdtVjBJaEsta0F3In0.eyJqdGkiOiIxNzQwMTRjYS0xNmM5LTQyMTEtYTQ4Zi03MzE4YTcyMjM1OWMiLCJleHAiOjE3NjMwNDEyMzQsIm5iZiI6MCwiaWF0IjoxNzYzMDQwOTM0LCJpc3MiOiJodHRwczovL2xvZ2luLmRlcy5jYWl4YS9hdXRoL3JlYWxtcy9pbnRyYW5ldCIsInN1YiI6ImJkNjM1OTZkLTU2NTMtNGE0YS05YTkxLWE4ZWQzMzUzNDVhNCIsInR5cCI6IkJlYXJlciIsImF6cCI6ImNsaS1zZXItb2JzIiwiYXV0aF90aW1lIjowLCJzZXNzaW9uX3N0YXRlIjoiNTgwYjNiMzgtYTM3Yi00OGY5LWFhMzYtYzUxZDVhZTFkNGU0IiwiYWNyIjoiMSIsInJlYWxtX2FjY2VzcyI6eyJyb2xlcyI6WyJTRVRfU0VHVVJBTkNBIiwidW1hX2F1dGhvcml6YXRpb24iXX0sInNjb3BlIjoiZW1haWwgcHJvZmlsZSIsInNlZ21lbnRvX3Npc3RlbWEiOiIzMzEwIiwiZW1haWxfdmVyaWZpZWQiOmZhbHNlLCJjbGllbnRJZCI6ImNsaS1zZXItb2JzIiwiY2xpZW50SG9zdCI6IjEwLjIwNS4yNTMuMTUzIiwic2VydmljZV91c2VybmFtZSI6IlNPQkFTRDAxIiwicHJlZmVycmVkX3VzZXJuYW1lIjoic2VydmljZS1hY2NvdW50LWNsaS1zZXItb2JzIiwiY2xpZW50QWRkcmVzcyI6IjEwLjIwNS4yNTMuMTUzIiwiZW1haWwiOiJzZXJ2aWNlLWFjY291bnQtY2xpLXNlci1vYnNAcGxhY2Vob2xkZXIub3JnIn0.K5LqTxRKM5h_Hka2KcFWIooUxb36I_GtFf-N33_jb5ZnaijQcI4xsha0wcRt3We5h0HC3gmosGMdsukg5-vmxcLztogXip8gFCqQsCghQ05r82N-QhZHEKD1bMACu7jKrldAnul9mfAEHl60uhIkkO7T8kID1AmCxTWS99w2PI3OyKkYKT8JQs3j4s3VSsXXh4t_QYWSeyyuxpTXZ5qXHR3vYlUXmQ97ZAxDCuQtAKRNi31zyvAnLDOvfnvAF2PNt7M3pQH_J35Y29pTqye9uthpkC-fnD_JfJodmlYxJlgkkl1FOEbKciijEmxQP-gekNA2Tg02xikBNLohf6hdpQ",
			"type": "default",
			"description": "",
			"enabled": true
		},
		{
			"key": "api_auth_path",
			"value": "api/oauthclients",
			"type": "default",
			"description": "",
			"enabled": true
		},
		{
			"key": "client_id",
			"value": "urn:caixa:611039e2-4248-4d25-bd44-5ce6587bd559",
			"type": "default",
			"description": "",
			"enabled": true
		},
		{
			"key": "consent_id",
			"value": "urn:caixa:611039e2-4248-4d25-bd44-5ce6587bd559",
			"type": "default",
			"description": "",
			"enabled": true
		},
		{
			"key": "enrollment_id",
			"value": "urn:caixa:611039e2-4248-4d25-bd44-5ce6587bd559",
			"type": "default",
			"description": "",
			"enabled": true
		}
	],
	"_postman_variable_scope": "environment",
	"_postman_exported_at": "2025-11-14T14:19:18.280Z",
	"_postman_exported_using": "Postman/11.71.6"
}


﻿using SiobsAppPingFederate.Database.DAL;
using SiobsAppPingFederate.Database.Entities;
using System;
using System.Linq;

namespace SiobsAppPingFederate.Database;

public class DbInitializer
{
    public static void Initialize(PingFederateDbContext context)
    {
        context.Database.EnsureCreated();

        // Look for any accessGrants.
        if (context.AccessGrants.Any())
        {
            return;   // DB has been seeded
        }

        var accessGrants = new PingFederateAccessGrant[]
        {
            new PingFederateAccessGrant
            {
                guid = Guid.NewGuid().ToString(), 
                client_id = "TaobfOykDNc7-kGw2ZrAs", 
                hashed_refresh_token= "USMg92YuIj1xPunD2OUL4Kd1lEnJOtbHmKWP6_TAFHQ",
                context_qualifier = "authz_req|apc.U76dWzrKRNiRY1lG", 
                grant_type = "authorization_code", 
                unique_user_id = "02086630964",
                scope = "openid resources accounts consent:urn:caixa:cbecb75c-defa-4ca3-9b61-7fa72b5459ae",
                expires = DateTime.Now.AddDays(10), issued = DateTime.Now, updated = DateTime.Now.AddMinutes(10)
            },
            new PingFederateAccessGrant
            {
                guid = Guid.NewGuid().ToString(), 
                client_id = "cli-ser-oba", 
                hashed_refresh_token= "FfWtvgjVF0vdzxeP3j6T87M8PvNYK5HeSYTpevgtv4E",
                context_qualifier = "authz_req|apc.U76dWzrKRNiRY1lG", 
                grant_type = "authorization_code", 
                unique_user_id = "11122240503",
                scope = "openid accounts consent:urn:caixa:fd87f190-e059-40de-af58-b4c62a9221f8",
                expires = DateTime.Now.AddDays(10), issued = DateTime.Now, updated = DateTime.Now.AddMinutes(10)
            }
        };
        foreach (PingFederateAccessGrant s in accessGrants)
        {
            context.AccessGrants.Add(s);
        }
        context.SaveChanges();
    }
}


Skip to content
GitHub Enterprise
Users managed by Caixa Economica Federal
code Search Results · repo:caixagithub/siobs-intra-administracaopingfederate HashedRefreshToken
Filter by
Paths
Advanced
3 files
 (103 ms)
3 files
in
caixagithub/siobs-intra-administracaopingfederate(press backspace or delete to remove)


SiobsAppPingFederate/Classes/DTO/PaymentsGrantDTO.cs
C#
·
2
 (2)
public class PaymentsGrantDTO 
{
    public string CPF { get; set; }
    public string HashedRefreshToken { get; set; }
    public string Scopes { get; set; }
    public DateTime ExpireTime { get; set; }
Show 1 more match


SiobsAppPingFederateTests/Classes/DtoMappingTests.cs
C#
·
1
 (1)
        var result = new PaymentsGrantDTO().MapFromEntity(entity);
        result.CPF.Should().Be("cpf");
        result.HashedRefreshToken.Should().Be("hash");
        result.Scopes.Should().Be("payments");
        result.ExpireTime.Should().Be(new DateTime(2026, 1, 1));
    }


SiobsAppPingFederateTests/Services/AccessGrantsServiceTests.cs
C#
·
1
 (1)
        result.Should().NotBeNull();
        result!.CPF.Should().Be("cpf");
        result.HashedRefreshToken.Should().Be("hash");
        result.Scopes.Should().Be("payments");
    }
