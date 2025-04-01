
**Estatísticas de E/S de bloco:** A quantidade de dados que o contêiner leu e gravou de dispositivos de bloco no host. Em outras palavras, a quantidade de bytes gravados/lidos do contêiner para o disco.

**Estatísticas de E/S de rede**: A quantidade de dados que o contêiner enviou e recebeu por meio de sua interface de rede. Exibe o total de bytes recebidos (RX) e transmitidos (TX). Em outras palavras, a quantidade de bytes que seu contêiner enviou/recebeu pela rede.

fazer backup

docker exec pg-n8n pg_dump -U devn8n n8n > pg_backup.sql


1 - remover logs

verificar aonde está a pasta do container, no que eu fiz agora tava em var/lib/dokcer/containers/<container que eu quero achar> 

mas preciso que seja em root, dai pode entrar como sudo su pra bugar e 

Column nameDescription
`CONTAINER ID` and `Name`the ID and name of the container
`CPU %` and `MEM %: `the percentage of the host's CPU and memory the container is using
`MEM USAGE / LIMIT` : the total memory the container is using, and the total amount of memory it is allowed to use
`NET I/O`The amount of data the container has received and sent over its network interface
`BLOCK I/O`The amount of data the container has written to and read from block devices on the host
`PIDs`the number of processes or threads the container has created