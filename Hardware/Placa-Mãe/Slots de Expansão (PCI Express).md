Aqui está o que encontrei sobre a evolução e funcionamento do **PCI Express (PCIe)**:

O PCIe é o padrão de conexão ponto a ponto que substituiu os barramentos paralelos clássicos (PCI e AGP) a partir de 2003. Ele opera por meio de pistas (_lanes_) seriais e independentes (x1, x4, x8, x16) que fornecem um canal de comunicação dedicado para cada componente. Seguindo a regra do consórcio industrial PCI-SIG, cada nova geração do barramento dobra a largura de banda da versão anterior, alcançando velocidades impressionantes no PCIe 4.0 e PCIe 5.0.

**Principais temas que notei:**

1. **Arquitetura Serial Ponto a Ponto**: Ao contrário do barramento PCI clássico compartilhado, onde vários periféricos disputavam o mesmo tráfego elétrico, o PCIe conecta o dispositivo diretamente ao processador ou chipset por canais exclusivos elétricos denominados pistas. Cada pista operando de forma bidirecional simultânea (_dual-simplex_).
2. **Dobra de Desempenho Físico**: O PCIe 4.0 (lançado em 2017) opera com taxa de transferência de 16 GT/s por pista (atingindo até 32 GB/s em slots de vídeo x16). Já o PCIe 5.0 (2019) dobra essa velocidade para 32 GT/s por pista, permitindo taxas de transferência de até 64 GB/s em slots x16 (ou 128 GB/s full duplex).
3. **Gargalo Térmico e Impacto Prático**: Na prática, o impacto do PCIe 5.0 sobre placas de vídeo topo de linha atuais (como a RTX 4090) é mínimo — em torno de 1% comparado ao PCIe 4.0 —, pois as GPUs ainda não saturam a largura de banda do padrão 4.0. No entanto, para os SSDs M.2 NVMe, o ganho é massivo (passando de 7.000 MB/s para mais de 10.000 MB/s), embora essas unidades Gen 5 exijam dissipadores ou coolers ativos porque esquentam muito.


**1. Codificação de Linha (A "Mágica" da Eficiência Gen 3/4/5)**

Para garantir que a transmissão serial em altíssima frequência não perca o sincronismo dos dados, o PCIe utiliza esquemas de codificação para embutir o sinal de clock no próprio fluxo de dados:

- **PCIe 1.0 e 2.0 (8b/10b):** Para cada 8 bits de dados reais, 2 bits adicionais de controle eram enviados. Isso gerava um _overhead_ (perda de eficiência) de **20%**.

- **PCIe 3.0, 4.0 e 5.0 (128b/130b):** A partir do Gen 3, mudou-se para 128 bits de dados a cada 130 bits transmitidos, reduzindo o _overhead_ para apenas **1,53%**. É essa mudança matemática de codificação que permitiu ao PCIe 3.0 quase dobrar a taxa útil de transferência do PCIe 2.0 sem precisar dobrar a frequência de clock do barramento.

---

**2. Pistas (Lanes) e Flexibilidade de Encaixe**

As conexões PCIe são agrupadas em conjuntos de pistas chamados de **Lanes** (representados pela letra **x**):

- **Formatos Comuns:** x1, x4, x8 e x16.

- **Compatibilidade Física e Lógica:** Qualquer placa PCIe funcionará em um slot do mesmo tamanho ou maior (uma placa x4 funciona em um slot x16). Além disso, a comunicação negocia automaticamente a velocidade suportada pelo menor elo: uma placa PCIe 3.0 instalada em um slot PCIe 5.0 operará perfeitamente nas velocidades limite do Gen 3.
---

**3. Comparativo de Gerações (Largura de Banda por Pista e Slot x16)**

  
|**Geração**|**Taxa de Transmissão por Pista**|**Largura de Banda (x1 Lane)**|**Largura de Banda (x16 Slot)**|**Codificação**|
|---|---|---|---|---|
|**PCIe 1.0**|2,5 GT/s|~250 MB/s|~4,0 GB/s|8b/10b|
|**PCIe 2.0**|5,0 GT/s|~500 MB/s|~8,0 GB/s|8b/10b|
|**PCIe 3.0**|8,0 GT/s|~985 MB/s|~15,75 GB/s|128b/130b|
|**PCIe 4.0**|16,0 GT/s|~1,97 GB/s|~31,5 GB/s|128b/130b|
|**PCIe 5.0**|32,0 GT/s|~3,94 GB/s|~63,0 GB/s|128b/130b|

---

**4. Diretamente no Processador vs. No Chipset**

Na arquitetura do PC, nem todos os slots PCIe são iguais:


- **Pistas da CPU:** Os slots x16 principais de vídeo e o primeiro slot M.2 NVMe conectam-se diretamente às pistas PCIe internas da CPU, garantindo a **menor latência possível**.

- **Pistas do Chipset:** Os slots secundários e portas adicionais passam primeiro pelo Chipset para depois trafegar pelo barramento DMI (que interliga o Chipset ao Processador), adicionando uma pequena latência intermediária.