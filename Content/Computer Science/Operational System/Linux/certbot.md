

openssl s_client -connect domain:443 -servername domain
openssl verify -CAfile /etc/letsencrypt/live/domain/fullchain.pem /etc/letsencrypt/live/domain/cert.pem


 sudo certbot --nginx -d colocar dns aqui --preferred-challenges dns
sudo certbot certonly --manual --preferred-challenges dns -d domain