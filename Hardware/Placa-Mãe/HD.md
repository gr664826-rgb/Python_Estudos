O **disco rígido** (também chamado de disco fixo, HD ou pelo antigo apelido de _Winchester_) é o principal meio de armazenamento de massa (memória secundária) do computador, onde os dados e programas são gravados de forma não-volátil (não se apagam ao desligar o micro).

De acordo com o livro de Gabriel Torres, estes são os principais fundamentos sobre o funcionamento e manutenção dos HDs:

### 1. Estrutura Física e Rotação

- **O sistema lacrado:** O HD é uma caixa preta hermeticamente fechada. Como ele gira em velocidades altíssimas (pelo menos 3.600 rpm, com modelos modernos de 4.800 rpm, 7.200 rpm ou mais), qualquer partícula de poeira causaria uma colisão catastrófica.
- **O colchão de ar:** Devido à alta rotação, cria-se um colchão de ar que faz com que as cabeças de leitura/gravação flutuem sobre a superfície magnética dos pratos de metal. Não há contato físico direto; se houver contato, os dados e a superfície são destruídos imediatamente.
- **Múltiplos discos:** Internamente, o HD é composto por um conjunto de pratos concêntricos, com cabeças de leitura dedicadas para cada face magnética.

### 2. O Atuador: Motor de Passo vs. Voice Coil

- Os HDs antigos (padrão ST-506) eram baseados em **motores de passo**. Eles se moviam de forma mecânica e rígida trilha por trilha, o que tornava o acesso lento (65 a 100 ms) e "burro".
- Os discos modernos (IDE e SCSI) usam atuadores do tipo **Voice Coil**. Eles utilizam uma única instrução direta para ir ao cilindro de destino, orientando-se por sinais analógicos gravados na fábrica chamados **servos**. Isso derrubou o tempo de acesso para uma faixa de 10 a 40 ms.

### 3. Formatação Física, Lógica e Setores Reserva

- **A farsa da formatação em baixo nível:** Usuários **nunca** devem tentar formatar um HD IDE ou SCSI em baixo nível por conta própria. Fazer isso apaga os sinais físicos de _servo_, inutilizando o disco permanentemente.
- **Sector Sparing (Setor Reserva):** Os HDs modernos reservam setores vazios em cada trilha. Quando softwares atuais de "formatação de baixo nível" (fornecidos pelos fabricantes) são executados, eles não reformatam o disco; eles apenas fazem uma varredura para identificar setores defeituosos (_bad sectors_) e remapeá-los para esses setores de reserva. Assim, os setores defeituosos "sumem" do Scandisk, embora continuem fisicamente lá.

### 4. Desempenho: PIO Mode vs. Bus Mastering (DMA)

- **Modo PIO:** Por padrão, o processador controla diretamente o tráfego de arquivos do HD para a RAM, o que sobrecarrega a máquina. Em testes de laboratório, essa comunicação usava até **92,7%** da capacidade do processador, limitando a transferência a apenas **8,2 MB/s**.
- **Bus Mastering:** Ao instalar os drivers do chipset e habilitar a função DMA no gerenciador de dispositivos do Windows, o chipset (Ponte Sul) assume o controle da transferência. O rendimento prático dispara para **46 MB/s** e a utilização da CPU desaba para meros **2,7%**, liberando o PC para outras tarefas.
- **Cabos de 80 Vias:** Modos Ultra DMA rápidos (como UDMA/66 e UDMA/100) transmitem múltiplos dados por pulso de clock, o que gera ruído eletromagnético capaz de corromper dados em fios adjacentes. Para evitar isso, essas tecnologias exigem cabos flat especiais de **80 fios** (onde as 40 vias adicionais são ligadas ao terra para blindar a interferência).

---

