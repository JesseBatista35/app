IFEC-CONSTRUCARD 1.23.1.2-b64: o deploy no 7.4 (DES) foi revertido por erro de CDI (WELD-001408). É correção no pacote.

As classes REST injetam os EJBs pela interface, mas estes 5 EJBs não expõem a interface (só a própria classe):

MaoDeObraConstrucardNegocioImpl → MaoDeObraConstrucardNegocio
CnaeConstrucardNegocioImpl → CnaeConstrucardNegocio
ConvenenteConstrucardNegocioImpl → ConvenenteConstrucardNegocio
CorrespondenteConstrucardNegocioImpl → CorrespondenteConstrucardNegocio
TotalizadorConstrucardBean → TotalizadorConstrucardService

Ajuste sugerido: em cada um, declarar implements <Interface> ou anotar com @Local(<Interface>.class), como já está em CompraConstrucardNegocioImpl e EstabelecimentoConstrucardNegocioImpl.

@Gustavo Duarte Lepesteur da Costa, quem é o dev do CONSTRUCARD para encaminharmos?
