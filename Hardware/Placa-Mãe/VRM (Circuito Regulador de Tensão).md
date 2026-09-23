O **VRM (Voltage Regulator Module — Módulo Regulador de Voltagem)**, no contexto de hardware abordado em seu livro, refere-se a um módulo ou circuito regulador de tensão projetado para adequar a energia fornecida ao processador.
### 1. Qual é a função do VRM?

O VRM tem como papel principal **ajustar e estabilizar a tensão de alimentação (voltagem) do processador**. Ele é de extrema importância quando a placa-mãe não consegue fornecer nativamente a tensão exata exigida por um determinado modelo de chip.

### 2. O clássico problema elétrico da Era Socket 7

Durante a transição dos processadores Pentium clássicos para o **Pentium MMX**, o mercado de hardware enfrentou um grande desafio elétrico:

- As placas-mãe mais antigas do padrão Socket 7 trabalhavam fornecendo uma tensão única padrão de **3,3 V**.
- Os novos processadores Pentium MMX passaram a exigir uma **tensão dupla**: **2,8 V** para alimentar o núcleo interno do processador (_core_) e **3,3 V** para a comunicação externa no barramento local (_I/O_).
- Se você tentasse instalar um processador Pentium MMX de 2,8 V em uma placa-mãe antiga de 3,3 V, **o chip queimaria** por excesso de calor e tensão.

### 3. Como o módulo VRM resolvia isso?

Se a placa-mãe antiga possuísse o conector físico adequado, o técnico poderia instalar um **módulo VRM de 2,8 V** diretamente nesse encaixe. Esse circuito independente recebia a energia do barramento e a rebaixava com precisão para os 2,8 V requeridos pelo núcleo do processador, permitindo o upgrade seguro sem danificar a peça.

O uso de módulos VRM também era a alternativa para instalar outros processadores concorrentes que operavam em voltagens variadas na mesma placa-mãe, como o AMD K6 (alimentado com 2,2 V ou 2,8 V) ou o Cyrix 6x86L.

### 4. A alternativa: Os processadores "Overdrive"

Para os usuários que tinham placas-mãe sem o conector físico de VRM, a Intel criou a linha de processadores **Pentium Overdrive MMX**. Esses chips já vinham equipados de fábrica com um regulador de tensão físico acoplado diretamente sob o seu próprio dissipador e ventoinha, convertendo a tensão de forma interna sem depender da placa-mãe.

---

