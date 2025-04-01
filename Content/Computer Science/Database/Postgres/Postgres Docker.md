
services:
  main:
     image: postgres:14
     ports:
	- target:5432
	published:5433
	protocol: tcp
	mode: host
	
environment:
	- POSTGRES_PASSWORD=123
	- PGDATA=/var/lib/PostgreSQL/ata
	-type:tmpfs
	target:/dev/shm


1 - criar um usuario backup dentro do pgadmin
2 - ir no pg_hba dentro do container e incluir o usuario backup na linha de replication e colocar pra acessar com senha scram 0.0.0.0/0

criar slot de replicacao

um espaçõ aonde o postgres vaia rmazenar os arquivos de wal e garantir que os arquivos vao ficar disponiveis das replicas.

SELECT pg_create_physical_replication_slot('slot_replicacao_master')

garantir que o servidor de replicacao ao se conectar co m oservidor master vai verificar os arquivos de wall nesse slot

