## Dev SSL | PEM CRT CER PFX

A chave privada original usada para o certificado


openssl pkcs12 -export -out certificate.usuporte.com.br.pfx -inkey privateKey.usuporte.com.br.key -in certificate.usuporte.com.br.crt -certfile more.usuporte.com.br.ca

