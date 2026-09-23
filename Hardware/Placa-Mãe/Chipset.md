O **chipset** (que significa literalmente "conjunto de circuitos") ==é o principal componente da placa-mãe.== Ele é um conjunto de circuitos de apoio responsável por **auxiliar o processador no gerenciamento do computador**.

Como o processador não consegue fazer tudo sozinho, o chipset atua como o sistema nervoso da placa, ==controlando o fluxo de dados entre a CPU, a memória e todos os periféricos.== Por controlar esses caminhos, é o chipset que define os limites físicos do seu computador — como o tipo e a quantidade máxima de memória RAM suportada, os [[Barramentos]] disponíveis (PCI, AGP, USB) e a velocidade máxima de comunicação.

A evolução do hardware dividiu o chipset em duas arquiteturas principais:

### 1. Arquitetura de Pontes (Clássica)

Tradicionalmente, os chipsets são divididos em dois chips principais soldados na placa-mãe:

- **Ponte Norte (_North Bridge_):** ==É o chip mais importante e fica mais próximo do processador. Ele gerencia os componentes que exigem altíssima velocidade: o controlador de memória RAM, o barramento local (comunicação com a CPU) e a interface gráfica (AGP ou PCI Express).== Por trabalhar sob forte estresse e em alta frequência, a Ponte Norte costuma necessitar de um dissipador de calor (e às vezes até de uma ventoinha).
- **Ponte Sul (_South Bridge_):** Controla os componentes mais lentos do computador. Ela abriga as controladoras de disco (portas IDE/SATA), portas USB, barramento ISA/PCI e gerencia recursos essenciais de sistema como o controlador de interrupções, canais de DMA, o relógio de tempo real (RTC) e a memória de configuração (**CMOS**).
- **Super I/O:** É um chip auxiliar ligado à Ponte Sul que cuida das portas seriais, paralela, teclado, mouse PS/2 e unidade de disquete (embora em chipsets mais novos ele tenha sido embutido diretamente na própria Ponte Sul).

### 2. Arquitetura Hub (Moderna)

Introduzida pela Intel em chipsets como o Intel 810 e 820, essa arquitetura eliminou o modelo clássico de pontes. Em vez de se comunicarem através do barramento PCI (o que gerava um gargalo de desempenho), ela utiliza um barramento elétrico exclusivo de alta velocidade para conectar dois chips principais:

- **MCH (_Memory Controller Hub_):** O equivalente direto à Ponte Norte.
- **ICH (_I/O Controller Hub_):** O equivalente à Ponte Sul, que removeu definitivamente o suporte ao antigo barramento ISA.

---

### ⚠️ Curiosidade: Os Chipsets "Pro" (Remarcados)

O livro traz um alerta muito comum para técnicos da época: fabricantes de placas-mãe de baixo custo (especialmente a **PCChips**) tinham o hábito de pedir que marcas de chipsets famosas (como SiS, VIA e ALi) decalcassem nomes falsos sobre o chip. Surgiram assim os famosos chipsets **VX Pro, TX Pro, TX Pro II e Super TX**. Para o sistema operacional, eles não passavam de chips comuns remarcados (por exemplo, o TX Pro II era na verdade um chipset SiS 5598), exigindo que o técnico descobrisse o fabricante real para conseguir instalar os drivers de funcionamento adequados.

---
