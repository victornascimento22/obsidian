


O Teorema CAP (Consistência, Disponibilidade e Tolerância à Partição) é um princípio fundamental para sistemas distribuídos, estabelecendo que é impossível alcançar simultaneamente as três propriedades em um sistema. Ou seja, ao projetar um sistema distribuído, é necessário escolher **duas dessas propriedades** como prioridade, deixando uma de fora:

1. **Consistência (C)**: Todos os nós veem os mesmos dados ao mesmo tempo. Isso garante que, após uma operação de gravação, todos os usuários terão acesso à versão mais recente dos dados.
    
2. **Disponibilidade (A)**: O sistema responde a todas as solicitações, mesmo que algumas partes do sistema estejam indisponíveis. Aqui, a prioridade é sempre manter o serviço funcionando.
    
3. **Tolerância à Partição (P)**: O sistema continua funcionando mesmo que ocorra uma falha de comunicação entre os nós, dividindo o sistema em partes desconectadas (partições).
    

Na prática:

- Escolher **Consistência e Disponibilidade (CA)** significa sacrificar a tolerância a partições. Funciona bem quando a conectividade entre os nós é garantida, mas falha durante interrupções de rede.
- Escolher **Consistência e Tolerância à Partição (CP)** sacrifica a disponibilidade, já que o sistema pode se recusar a responder até que os dados sejam consistentes entre os nós.
- Escolher **Disponibilidade e Tolerância à Partição (AP)** significa abrir mão da consistência, aceitando que os dados podem variar entre os nós em um curto período.

**Conclusão**: O Teorema CAP não é sobre o que é melhor, mas sobre o que priorizar com base nas necessidades do sistema. Sistemas como bancos de dados NoSQL frequentemente escolhem AP (Disponibilidade e Tolerância à Partição), enquanto sistemas financeiros podem optar por CP (Consistência e Tolerância à Partição).
