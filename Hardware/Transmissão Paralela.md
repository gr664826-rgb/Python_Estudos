
**Transmissão paralela** é um método de comunicação em que **vários bits são enviados simultaneamente**, cada um por uma linha de comunicação diferente.

A interferência ocorre quando os sinais de fios próximos influenciam uns aos outros, causando erros nos bits e perda na qualidade do sinal.

Cabo de 80 vias oferece mais canais de transmissão, funcionando com o alternamento/separação entre os fios de sinal, reduzindo a interferência.

Os bits são enviados um após o outro → menos fio, menos interferência → envia e recebe.


**Clock** => É um sinal que define o ritmo da transmissão e do processamento dos dados.

Funciona como uma batida: “tic → envia/processa um bit → tic → envia/processa outro bit”.

Quanto maior a frequência do clock, medida em Hz, mais operações ou bits podem ser processados p/ segundo.

Por exemplo, para transmitir o byte `10110100`, podem ser usados **8 fios**, com cada fio transportando um bit:

`1 | 0 | 1 | 1 | 0 | 1 | 0 | 0`

### Características

- **Vários bits ao mesmo tempo:** aumenta a quantidade de dados transmitidos em cada instante.
- **Vários condutores:** normalmente são necessários vários fios ou trilhas.
- **Curta distância:** é mais adequada para distâncias pequenas, pois diferenças de tempo entre os sinais podem causar erros.
- **Maior complexidade física:** utiliza mais conexões que a transmissão serial.
- **Exemplo clássico:** antigas interfaces de impressoras, como a **porta paralela (LPT)**.
  
  Transmissor                         Receptor

   1 ────────────────────────────────> 1
   0 ────────────────────────────────> 0
   1 ────────────────────────────────> 1
   1 ────────────────────────────────> 1
   0 ────────────────────────────────> 0
   1 ────────────────────────────────> 1
   0 ────────────────────────────────> 0
   0 ────────────────────────────────> 0

             10110100






