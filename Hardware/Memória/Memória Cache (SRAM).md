A **memória RAM Estática (SRAM)** é a tecnologia utilizada para construir a **memória cache** do computador. ==Ela funciona como uma intermediária ultra-rápida entre o processador (que é extremamente veloz) e a memória RAM principal== (DRAM, que é mais lenta e introduz os atrasos chamados [[Wait States]]).

Aqui está como ela funciona estruturalmente e o papel crucial que desempenha no PC:

### 1. SRAM vs. DRAM (A diferença física)

- **DRAM (Dinâmica):** Armazena os bits em minúsculos capacitores elétricos. Como eles perdem carga com o tempo, o computador precisa constantemente interromper as atividades para recarregá-los (o processo de **refresh**). Isso torna a DRAM barata e compacta, mas limita fisicamente sua velocidade.
- **SRAM (Estática):** Utiliza circuitos digitais complexos chamados **flip-flops** para armazenar cada bit (0 ou 1). Ela **não precisa de ciclos de refresh**. Por não precisar parar para recarregar, ela é extremamente rápida e opera na mesma velocidade do processador, mas é muito mais cara, consome mais energia e ocupa muito mais espaço físico.

Como construir toda a RAM do computador com SRAM seria inviável financeiramente, os PCs adotam um **sistema híbrido**: uma RAM principal dinâmica (grande e barata) intermediada por uma pequena quantidade de SRAM estática (rápida e cara).

---

### 2. O funcionamento do Cache: "Hit" e "Miss"

Um circuito especial chamado controlador de cache monitora os acessos do processador e copia antecipadamente blocos de dados da RAM dinâmica para a memória cache (SRAM).

- **Cache Hit (Acerto):** Em pelo menos 80% das vezes, o dado que o processador procura já foi copiado para a SRAM. O processador lê a informação imediatamente na sua velocidade máxima, sem sofrer com wait states.
- **Cache Miss (Erro):** Se o dado não estiver na SRAM, o processador é obrigado a buscar o arquivo diretamente na RAM dinâmica, tendo de esperar alguns pulsos de clock (o que reduz temporariamente o desempenho).

---

### 3. Os Níveis de Cache (L1, L2 e L3)

Para otimizar o custo e o fluxo de dados, a memória cache é organizada em níveis:

- **L1 (Level 1):** Fica embutido dentro do núcleo do processador e é muito pequeno (geralmente dividido em dois blocos independentes: um exclusivo para instruções e outro para dados).
- **L2 (Level 2):** É maior que o L1. Nos computadores antigos (geração soquete 7), ele ficava na placa-mãe e era limitado pelo clock externo do barramento. A partir do Pentium Pro e Pentium II, passou a ser integrado ao processador, comunicando-se por um barramento exclusivo (chamado _backside bus_ ou barramento independente) que opera em frequências muito mais altas (no clock interno ou na metade dele).
- **L3 (Level 3):** Adotado originalmente por processadores como o K6-III (que usava o cache antigo da placa-mãe como L3) e por chips de servidores para evitar que o processador precise recorrer à RAM dinâmica em caso de falha no L2.

---

### 4. Como o cache atualiza a memória RAM?

Quando o processador altera um dado dentro do cache, o computador precisa salvar essa alteração na memória RAM dinâmica principal. Existem dois métodos para isso:

1. **Write Through (Escrita Direta):** O processador grava o dado no cache e, simultaneamente, na RAM. É um processo mais simples, porém obriga o processador a esperar a lenta RAM terminar a gravação.
2. **Write Back (Escrita Postergada):** O processador grava a alteração apenas no cache SRAM. O controlador de cache se organiza para atualizar a RAM dinâmica em segundo plano apenas quando o barramento de dados estiver livre. Esse é o método ideal usado nos PCs modernos, pois libera o processador instantaneamente.

---

