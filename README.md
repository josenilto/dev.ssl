## 🛠 Dev SSL | Crie um arquivo de certificado .pfx / .p12 usando OpenSSL

Na criptografia, o formato PKCS # 12 ou PFX é um formato binário freqüentemente usado para armazenar todos os elementos da cadeia de confiança, como o certificado do servidor, quaisquer certificados intermediários e a chave privada em um único arquivo criptografável.         

Os arquivos PFX são geralmente encontrados com as extensões .pfx e .p12. Os arquivos PFX são normalmente usados ​​em máquinas Windows e macOS para importar e exportar certificados e chaves privadas.

A chave privada original usada para o certificado



Os comandos abaixo demonstram exemplos de como criar um arquivo .pfx / .p12 na linha de comando usando OpenSSL:

PEM (.pem, .crt, .cer) para PFX

> openssl pkcs12 -export -out certificate.usuporte.com.br.pfx -inkey privateKey.usuporte.com.br.key -in certificate.usuporte.com.br.crt -certfile more.usuporte.com.br.ca

Quebrando o comando:

✅ openssl       
O comando para executar OpenSSL       

✅ pkcs12      
O utilitário de arquivo para arquivos PKCS # 12 em OpenSSL     

✅ -export -out certificate.usuporte.com.br.pfx        
exportar e salvar o arquivo PFX como certificate.pfx     

✅-inkey privateKey.usuporte.com.br.key      
use o arquivo de chave privada privateKey.key como a chave privada a ser combinada com o certificado.       

✅-in certificate.usuporte.com.br.crt**     
use certificate.crt como o certificado com o qual a chave privada será combinada.     

✅-certfile more.usuporte.com.br.crt     
Isso é opcional, se você tiver quaisquer certificados adicionais que gostaria de incluir no arquivo PFX.     



*PKCS # 7 / P7B (.p7b, .p7c) para PFX*


Os arquivos P7B não podem ser usados ​​para criar diretamente um arquivo PFX.       
Os arquivos P7B devem ser convertidos para PEM. Depois de convertido em PEM, siga as etapas acima para criar um arquivo PFX a partir de um arquivo PEM.

> openssl pkcs7 -print_certs -in certificate.usuporte.com.br.p7b -out certificate.usuporte.com.br.crt

Quebrando o comando:

✅ openssl         
O comando para executar OpenSSL

✅ pkcs7         
O utilitário de arquivo para arquivos PKCS # 7 em OpenSSL

✅ -print_certs -in certificate.usuporte.com.br.p7b     
Imprime quaisquer certificados ou CRLs contidos no arquivo.

✅ -out certificate.usuporte.com.br.crt     
produza o arquivo como certificate.crt

![Badge em Desenvolvimento](http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=GREEN&style=for-the-badge)