openssl s_client prod-mercury-wave.russian-lotteries.net:443

Проверка tls серта

openssl x509 -noout -modulus -in crt.crt| openssl md5
openssl rsa -noout -modulus -in key.key| openssl md5