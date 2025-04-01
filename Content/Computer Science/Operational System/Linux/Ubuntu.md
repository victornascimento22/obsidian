
adduser = criar usuário

	awk -F: '/\/bin\/bash/ {print $1}' /etc/passwd = listar usuario com shell ativo


ls

sudo sed -i 's/127\.0\.0\.1\/32\( \|\n\)/0.0.0.0\/0\1/g' pg_hba.conf


configurando dns 

instalar nginx 

sudo apt install nginx -t

sudo certbot certonly --manual --preferred-challenges=dns -d domain
criar txt com o valor que o certbot gerar no rpovedor de dns 



