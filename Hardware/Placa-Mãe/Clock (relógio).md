O sinal de clock é o "metrônomo" ou o "maestro" do computador. Ele é um sinal presente no barramento de controle de qualquer barramento que utilize comunicação paralela.

Aqui está o funcionamento detalhado desse sinal com base no material do livro:

### 1. Sincronização da Transmissão de Dados

Em uma transmissão de dados paralela, os bits são enviados simultaneamente por vários fios (por exemplo, 64 bits por vez entre o processador e a RAM). Sem um sinal regulador, o dispositivo receptor não saberia o momento exato em que os dados estão disponíveis nas trilhas da placa-mãe.

O **clock serve para sincronizar o transmissor com o receptor**, avisando que um dado está sendo transmitido. Como você pode observar nos diagramas (especialmente na transição da Figura 1.2 para a 1.3), o sinal elétrico do clock oscila continuamente entre 0 e 1. Por padrão:

- Os dados são transmitidos na **subida do pulso de clock** (o momento exato em que o sinal passa de 0 para 1).
- Em condições normais, **somente um dado pode ser transmitido por pulso de clock**. Algumas tecnologias especiais (como os processadores Athlon e Pentium 4, e memórias DDR-SDRAM) conseguem transmitir mais de um dado por pulso.

### 2. Clock Interno vs. Clock Externo (Multiplicação)

Muitas vezes as pessoas confundem a velocidade estampada no anúncio do processador com a velocidade real de transmissão da placa-mãe. A partir dos processadores 486DX2, o PC passou a adotar a **multiplicação de clock**:

- **Clock Interno:** É a velocidade com que o processador trabalha internamente (por exemplo, um Pentium III de 700 MHz processa dados internamente a 700 MHz).
- **Clock Externo (ou de Barramento):** É a frequência do barramento local usado na transmissão de dados entre o processador e a memória RAM. No exemplo do Pentium III de 700 MHz, o clock externo é de apenas 100 MHz.

Essa divisão existe porque **é muito difícil e caro construir placas-mãe e chipsets de apoio que consigam operar em frequências tão altas** quanto as que os processadores alcançam internamente. Na placa-mãe, existe um componente físico chamado **Gerador de Clock** (um circuito integrado perto de um cristal de quartzo) responsável por ditar esse clock externo.

### 3. Sistemas de Clock Independentes

O computador não usa um único sinal de clock para todos os componentes. O sinal usado entre o processador e a RAM é completamente independente dos demais barramentos:

- O barramento local (CPU-RAM) opera em frequências altas (como 66 MHz, 100 MHz ou 133 MHz).
- Os barramentos de expansão (onde conectamos periféricos) operam em clocks menores e padronizados para garantir compatibilidade: o barramento **PCI** geralmente trabalha a 33 MHz, o **AGP** a 66 MHz, e o antigo **ISA** trabalha fixo a apenas 8 MHz.

### 4. Por que Clock não é sinônimo de Desempenho?

==O desempenho geral do computador depende do conjunto (placa-mãe, RAM, disco rígido, placa de vídeo)== e não apenas do clock do processador. Além disso, **processadores de arquiteturas diferentes realizam trabalhos diferentes no mesmo intervalo de tempo**.

Por exemplo: o processador 486 é capaz de executar algumas instruções usando apenas **um pulso de clock**, enquanto o antigo 386 demorava, no mínimo, **três pulsos de clock** para executar a mesma instrução. Por isso, um 486 de 25 MHz é muito mais rápido que um 386 de 40 MHz.

---





