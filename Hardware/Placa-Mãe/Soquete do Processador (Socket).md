O **soquete do processador (socket)** é o conector físico localizado na placa-mãe onde o processador é instalado. ==Ele atua como uma ponte que conecta o barramento local do processador ao chipset e ao restante dos componentes do computador.==

Antes do processador 486, os processadores costumavam vir soldados diretamente na placa-mãe, o que impedia qualquer possibilidade de upgrade. A partir do 486, a Intel padronizou o uso de soquetes, permitindo que o usuário fizesse atualizações futuras apenas substituindo o chip do processador por um modelo compatível com o mesmo padrão de pinagem.

Para organizar seus estudos, o livro do Gabriel Torres divide os soquetes e slots em quatro grandes eras:

### 1. A Era 486 (Início da padronização)

Os primeiros conectores evoluíram à medida que novos recursos eram lançados:

- **Soquete 0** (168 pinos) e **Soquete 1** (169 pinos): Criados para os primeiros chips 486DX e 486SX.
- **Soquete 2** (238 pinos): Lançado para suportar o 486DX2 e os processadores de atualização Pentium Overdrive.
- **Soquete 3 (237 pinos):** Tornou-se o **conector definitivo para a família 486**. Ele introduziu pinos específicos para fornecer a alimentação elétrica de 3,3 V exigida pelos chips mais modernos (como o 486DX4), além de aceitar os antigos processadores de 5 V.
- **Soquete 6** (235 pinos): Um soquete menor de 3,3 V projetado para o 486DX4, mas menos comum que o Soquete 3.

### 2. A Era Pentium Clássico e o Soquete Unificado

Nesta fase, a tensão elétrica de operação caiu e a quantidade de pinos aumentou para lidar com barramentos mais largos:

- **Soquete 4 (273 pinos):** Alimentava os primeiros processadores Pentium (de 60 MHz e 66 MHz) com 5 V.
- **Soquete 5 (320 pinos):** Operava a 3,3 V e dava suporte a processadores Pentium de até 133 MHz, mas possuía limitações de multiplicação de clock.
- **Soquete 7 (321 pinos):** O **soquete definitivo da 5ª geração**. Tornou-se um padrão altamente popular porque era compatível pino a pino tanto com os processadores Pentium e Pentium MMX da Intel quanto com chips de fabricantes concorrentes (AMD K5, AMD K6, Cyrix 6x86 e Cyrix MII).
- **Super 7:** Uma evolução do Soquete 7 criada por outros fabricantes para competir com a Intel. Essas placas permitiam que o barramento externo operasse a 100 MHz e davam suporte às placas de vídeo AGP.

### 3. A Guerra dos "Slots" (Cartuchos) vs. Soquete 370

Na 6ª geração de processadores (arquitetura P6), a Intel adotou temporariamente o formato de cartucho para abrigar o chip de processamento e a memória cache L2:

- **Slot 1 (conector de 242 contatos):** Usado pelo Pentium II, Pentium III (SECC-2) e Celeron (SEPP). A Intel patenteou esse conector para impedir que concorrentes fabricassem processadores compatíveis sem pagar direitos autorais.
- **Slot 2 (conector de 330 contatos):** Destinado estritamente a servidores de alto desempenho, utilizado pelos processadores Pentium II Xeon e Pentium III Xeon.
- **Slot A (242 contatos):** Desenvolvido pela AMD para o processador Athlon em cartucho. Embora fosse mecanicamente idêntico ao Slot 1 da Intel, ele era eletronicamente incompatível.
- **Soquete 8 (387 pinos):** Soquete exclusivo para o processador corporativo Pentium Pro.
- **Soquete 370 (370 pinos):** Devido ao alto custo de fabricação dos cartuchos, a Intel retornou ao modelo tradicional de soquete para os chips Celeron e Pentium III (FC-PGA).
- **Soquete A ou 462 (462 pinos):** Criado pela AMD para substituir o Slot A, utilizado pelos processadores Athlon em soquete e Duron.

### 4. A Era Pentium 4 e IA-64

- **Soquete 423 (423 pinos):** O primeiro padrão utilizado pelos processadores Pentium 4 de 7ª geração.
- **Soquete 478 (478 pinos):** Desenvolvido para as revisões e futuros modelos do Pentium 4 que exigiam maior fornecimento de corrente elétrica.
- **Cartucho Itanium:** Utilizado pela linha IA-64 de 64 bits para servidores, misturando um contato de borda de slot (para energia) com os pinos de um soquete (para dados).

---

