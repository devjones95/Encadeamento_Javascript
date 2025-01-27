Encadeamento:

Imagina que você está pedindo para verificar o estado de uma casa. Só que essa verificação não acontece de forma imediata — ela leva um tempo, tipo quando você precisa esperar por uma resposta de alguém. No nosso código, esse "tempo de espera" é simulado com o `setTimeout`, que é como se fosse uma pausa temporária.

Agora, quando você faz esse pedido (no caso, a função `verificarStatusCasa`), ela vai retornar uma "promessa" — e o que é uma promessa? É como um compromisso de que, mais tarde, a operação vai terminar e você vai saber se deu certo ou se deu errado. A promessa pode ser **resolvida** (se a casa estiver boa) ou **rejeitada** (se precisar de reparos). Quando a promessa é resolvida, a gente recebe um retorno de sucesso, e quando ela é rejeitada, recebe uma mensagem de erro.

No código, a função `verificarStatus` da classe `Casa` chama a função `verificarStatusCasa`. E aí, o encadeamento acontece com o `.then()` e `.catch()`:
- **`.then()`**: Se a promessa for resolvida (ou seja, a casa está em boas condições), esse bloco de código vai rodar e vai mostrar a mensagem positiva.
- **`.catch()`**: Se a promessa for rejeitada (a casa precisa de reparos), o código no `catch` vai rodar e mostrar a mensagem de erro.

Isso tudo acontece de forma encadeada, ou seja, a gente não precisa ficar esperando manualmente cada parte do processo, porque o JavaScript lida com isso de maneira automática, cuidando do tempo de espera e nos dizendo se deu tudo certo ou não.

E o legal do encadeamento de promessas é que você pode fazer várias operações assíncronas uma atrás da outra, sem que o código fique todo bagunçado com múltiplos `setTimeout` ou callbacks. Assim, ele fica mais fácil de entender e manter.
