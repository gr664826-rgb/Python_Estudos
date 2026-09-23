
Os **wait states (estados de espera)** são pulsos de clock extras adicionados temporariamente ao ciclo de acesso (leitura ou escrita) da memória RAM.

Como o processador é muito mais rápido do que a memória RAM dinâmica (DRAM), ele precisa "esperar" o tempo físico que a RAM leva para organizar e entregar ou receber os dados.

### Como funciona a matemática do atraso

Eletronicamente, o processador precisa de **dois pulsos de clock** para concluir um acesso padrão à memória RAM.

Se a placa-mãe estiver operando com um clock externo de **66 MHz**, cada pulso de clock dura exatamente **15 ns** (nanossegundos). Portanto, o ciclo básico de dois pulsos dura **30 ns**.

- **O problema:** Se você instalar nessa placa-mãe memórias antigas com tempo de acesso de **60 ns**, o ciclo padrão de 30 ns é rápido demais e a RAM não conseguirá responder.
- **A solução (Wait States):** O controlador de memória insere **dois wait states** (dois pulsos de clock adicionais) no ciclo. Com isso, o ciclo passa a ter quatro pulsos de clock (60 ns), permitindo que a memória de 60 ns funcione perfeitamente. Se a memória fosse ainda mais lenta, de **70 ns**, seriam necessários **três wait states** (cinco pulsos de clock = 75 ns).

### O impacto no desempenho

O grande problema é que, durante o período de wait state, **o processador fica completamente ocioso, sem fazer absolutamente nada**.

- A inserção de apenas **1 wait state reduz o desempenho do acesso à memória em 1/3** (pois de 3 pulsos usados, apenas 2 são de trabalho real).
- A inserção de **2 wait states reduz esse desempenho pela metade (50%)**.

### Como o PC moderno resolveu isso?

1. **Configuração no Setup:** Se você substituir as memórias do seu micro por modelos com tempo de acesso menor (mais rápidas), você deve entrar no **Setup** e reduzir manualmente a quantidade de wait states. Se não fizer isso, o processador continuará esperando o tempo antigo e você não terá ganho nenhum de velocidade.
2. [[Memória Cache (SRAM)]]:** É a solução definitiva. Usando uma quantidade pequena de memória estática (SRAM), que trabalha na mesma velocidade do processador e **não precisa de wait states**, o controlador de cache copia os dados da RAM para ela. O processador passa a conversar diretamente com o cache em mais de 80% do tempo.