w
prestar atenção na hora de configurar essa bucha.

ele precisa apontar pro outro postgres do docker-compose para poder inciiar.

ele tem um script que tecnicamente ele cria um usuario e das permissoes necessarias pro n8n poder fazer as configurações porem a merda do script não roda.

tu tem que entrar dentro do container, usar psql pra entrar com o usuario postgres no banco setado no .env no meu caso é o n8n e criar o usuario, dar as permissoes e etc.

pra se conectar ao banco vc precisa colocar o host do container ou o ip.

-- Cria o usuário com a senha fornecida
CREATE USER devn8n WITH PASSWORD '123';

-- Concede todas as permissões no banco de dados para o novo usuário
GRANT ALL PRIVILEGES ON DATABASE n8n TO devn8n;

-- Concede permissões para criar objetos no esquema público
GRANT CREATE ON SCHEMA public TO devn8n;

docker exec -it <nome-do-contêiner> psql -U postgres

GRANT USAGE ON SCHEMA public TO devn8n; GRANT CREATE ON SCHEMA public TO devn8n;


