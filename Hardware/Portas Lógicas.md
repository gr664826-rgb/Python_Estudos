==São os blocos de construção fundamentais de qualquer circuito digital (como processadores, chipsets e memórias)==, responsáveis por realizar operações matemáticas sob a Álgebra Booleana para variáveis binárias, traduzindo sinais elétricos em níveis lógicos **0** (baixo/falso) e **1** (alto/verdadeiro). Existem portas básicas (**AND**, **OR** e **NOT**), portas universais derivadas (**NAND** e **NOR**) e portas exclusivas de comparação (**XOR** e **XNOR**), cada uma operando conforme uma regra matemática estrita definida por sua respectiva **tabela verdade**.


1. **Fundamentos Booleanos**: ==Cada porta lógica realiza uma função booleana específica== (soma lógica para OR, multiplicação lógica para AND, inversão para NOT), que formam a base dos circuitos de controle e processamento de dados nos PCs.
   
- **NOT (Inversora):** Possui apenas 1 entrada. Se a entrada for `1`, a saída será `0`; se for `0`, a saída será `1`.

- **AND (E):** Exige que **todas** as entradas sejam `1` para que a saída seja `1`. Funciona como um circuito em série.

- **OR (OU):** A saída será `1` se **pelo menos uma** das entradas for `1`. Funciona como um circuito em paralelo.
  
2. **Universalidade das Portas NAND e NOR**: Estas portas derivadas conseguem, sozinhas ou em combinações simples, substituir qualquer outra porta lógica básica, permitindo que fabricantes simplifiquem drasticamente a complexidade da fabricação física dos chips de silício.
   
- **NAND (NÃO-E) e NOR (NÃO-OU):** São a inversão direta das portas AND e OR. São chamadas de _universais_ porque qualquer circuito digital complexo — até mesmo um processador inteiro — pode ser construído usando exclusivamente portas NAND ou NOR.

- **XOR (OU Exclusivo):** A saída será `1` **apenas** se as entradas forem diferentes entre si. É a base dos circuitos somadores de bits nos processadores.

- **XNOR (NÃO-OU Exclusivo):** Funciona como um comparador de igualdade: a saída será `1` se todas as entradas forem idênticas.
  
3. **Mapeamento de Estados por Tabela Verdade**: A tabela verdade descreve exatamente o estado elétrico de saída de um circuito para todas as possíveis combinações de sinais de entrada, seguindo a progressão binária de $2^N$ combinações possíveis (onde $N$ é o número de entradas).