 1 - acessar o psql sudo -u postgres psql

2 - \du lista os usuarios

3 - Criar super user CREATE ROLE dba_user WITH LOGIN SUPERUSER PASSWORD 'your_password';
sudo nano /etc/postgresql/14/main/pg_hba.


\list mostra os bancos e configurações


Z@#U.C'nnfB3.o]FrzE^M5aR,!WPu3Y,M9UH}i9T

escrever testes de carga com o pgbench

pgbench -c 10 -j 2 -t 10000 -U dba example

-c =  numero de clients
-j = numero de threads
-t = numero de transacoes 


psql -h 191.101.71.42 -p 5433 -U dba starlov -W


CREATE ROLE replicator WITH REPLICATION LOGIN PASSWORD 123; CRIANDO UM USUARIO PRA REPLICA DO SERVIDOR READONLNY

psql -h 127.0.0.1 -p 5432 -U dba starlov
banco starlov
senha do dba: 1234

logs 

sudo tail -f /var/log/pgpool/pgpool.log
sudo tail -f /var/log/syslog

**Substituir `md5` por `scram-sha-256`, mas ignorar ocorrências com aspas**:

No modo normal, digite o seguinte comando e pressione `Enter`:

vim

Copiar código

`:%s/\(md5\)\( \|\n\|$\)/scram-sha-256\2/g`

starlov=# ALTER ROLE dba WITH PASSWORD '123456';

sudo -i -u postgres > ENTRAR NO USUARIO POSTGRES


**`initdb -D /usr/local/pgsql/data`**