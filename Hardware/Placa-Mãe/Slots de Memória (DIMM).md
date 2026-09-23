Complementando o tópico sobre os **Slots de Memória RAM (DIMM)**, estes soquetes presentes na placa-mãe são projetados para garantir a comunicação paralela de alta velocidade (64 bits por canal) entre os módulos de memória e o controlador de memória do processador.

**1. O que significa DIMM?**

- **DIMM (_Dual In-line Memory Module_):** Significa que os contatos elétricos de cada lado da placa do módulo de memória são totalmente independentes entre si, permitindo um caminho de dados de 64 bits por módulo (ao contrário do antigo padrão SIMM, que unificava os contatos).

- **SO-DIMM (_Small Outline DIMM_):** Versão fisicamente menor (com cerca de metade do tamanho do DIMM padrão), usada em notebooks, mini PCs e placas-mãe Mini-ITX compactas.

---

**2. A Chave do Rasgo (_Notch_) e Incompatibilidade Física**

Cada geração de memória RAM possui um corte físico em uma posição específica da sua base de pinos:

- Esse rasgo impede que um módulo incompatível seja encaixado no slot incorreto (por exemplo, tentar encaixar uma memória DDR4 em um slot DDR5).

- Impede também que a memória seja instalada ao contrário, evitando curtos-circuitos no barramento de alimentação.

---

**3. Tecnologia Dual-Channel e Quad-Channel**

Os slots de memória na placa-mãe geralmente vêm dispostos em pares organizados por cores ou numeração (ex: A1, A2, B1, B2):

- **Lógica:** Ao instalar os módulos nos slots corretos (ex: A2 e B2), o controlador de memória ativa o modo **Dual-Channel**, dobrando a largura do barramento de dados de **64 bits para 128 bits**.

- **Impacto:** Isso dobra a taxa de transferência teórica da memória RAM sem precisar aumentar a frequência de operação do relógio (_clock_).

---

**4. Evolução dos Slots de Memória para Desktop**

|**Padrão**|**Quantidade de Pinos**|**Tensão Nominal (V)**|**Recurso Destacado**|
|---|---|---|---|
|**DDR**|184 pinos|2,5 V|2 transferências por ciclo de clock|
|**DDR2**|240 pinos|1,8 V|Frequência interna reduzida com pré-fetch maior|
|**DDR3**|240 pinos|1,5 V / 1,35 V (L)|Baixo consumo elétrico e maiores frequências|
|**DDR4**|288 pinos|1,2 V|Formato ligeiramente curvo na base para facilitar o encaixe|
|**DDR5**|288 pinos|1,1 V|Gerenciamento de energia (PMIC) na própria régua de RAM|