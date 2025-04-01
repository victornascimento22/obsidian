[[HTTP]]
Os servidores de banco de dados podem trabalhar juntos para permitir que um segundo servidor assuma o controle rapidamente se o servidor primário falhar (alta disponibilidade) ou para permitir que vários computadores forneçam os mesmos dados (balanceamento de carga). Idealmente, os servidores de banco de dados poderiam trabalhar juntos perfeitamente. Os servidores Web que atendem a páginas da Web estáticas podem ser combinados facilmente apenas balanceando a carga de solicitações da Web para várias máquinas. Na verdade, os servidores de banco de dados somente leitura também podem ser combinados com relativa facilidade. Infelizmente, a maioria dos servidores de banco de dados tem uma mistura de solicitações de leitura/gravação e os servidores de leitura/gravação são muito mais difíceis de combinar. Isso ocorre porque, embora os dados somente leitura precisem ser colocados em cada servidor apenas uma vez, uma gravação em qualquer servidor deve ser propagada para todos os servidores para que futuras solicitações de leitura para esses servidores retornem resultados consistentes.

- O load balancer opera no **nível de transporte (camada 4)**, redirecionando conexões [[TCP]] para diferentes servidores.
- Ele não processa HTTP, mas distribui conexões baseadas em regras, como round-robin, hash de IP, ou com base na carga de cada nó.


[[Postgres]]
[PostgreSQL: Documentação: 17: Capítulo 26. Alta disponibilidade, balanceamento de carga e replicação](https://www.postgresql.org/docs/current/high-availability.html)