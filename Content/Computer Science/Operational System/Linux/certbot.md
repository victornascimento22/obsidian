

openssl s_client -connect api.capitalsistemas.srv.br:443 -servername intranet.capitalsistemas.srv.br
openssl verify -CAfile /etc/letsencrypt/live/api.capitalsistemas.srv.br/fullchain.pem /etc/letsencrypt/live/api.capitalsistemas.srv.br/cert.pem


 sudo certbot --nginx -d colocar dns aqui --preferred-challenges dns
sudo certbot certonly --manual --preferred-challenges dns -d infra.capitalsistemas.srv.br