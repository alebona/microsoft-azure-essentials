# Configurando Recursos e Dimensionamentos em Máquinas Virtuais no Azure

## 1. Acessar o Portal do Azure

Primeiro, faça login no [Portal do Azure](https://portal.azure.com). Certifique-se de que você tem as permissões necessárias para criar e gerenciar máquinas virtuais (VMs) na sua assinatura.

## 2. Criar uma Máquina Virtual

- No painel do Azure, procure por **Máquinas Virtuais** ou clique em **Criar Recurso**.
- Selecione **Máquina Virtual** e inicie o processo de criação.
- Escolha uma **assinatura** e um **grupo de recursos** existente ou crie um novo.
- Defina o **nome da VM** e escolha a **região** onde ela será hospedada.

## 3. Escolher o Tamanho da VM

- Durante a criação, você será solicitado a escolher o **tamanho da VM**. O tamanho define a quantidade de CPU, memória e armazenamento que sua VM terá.
- Selecione um tamanho que atenda às suas necessidades de processamento, considerando a carga de trabalho que será executada na VM.
  - **Tamanhos gerais** são indicados para aplicações comuns.
  - **Tamanhos otimizados para memória** são indicados para bancos de dados e aplicações que exigem mais RAM.
  - **Tamanhos otimizados para computação** são recomendados para cargas de trabalho com alta demanda de CPU.

## 4. Configurar o Sistema Operacional

- Escolha a **imagem do sistema operacional** para a VM, como Windows ou Linux. O Azure oferece diversas distribuições, incluindo versões otimizadas para o ambiente de nuvem.
- Defina as **credenciais de login**, seja através de **senha** ou **chave SSH** para Linux, ou **usuário e senha** para Windows.

## 5. Configurar Opções de Armazenamento

- Na aba de **Discos**, selecione o tipo de disco que será utilizado pela VM:
  - **SSD Premium**: ideal para cargas de trabalho de produção com alta performance de I/O.
  - **SSD Padrão**: adequado para aplicações que não exigem alta taxa de I/O.
  - **HDD Padrão**: utilizado para cargas de trabalho com baixo custo e menores demandas de desempenho.
- Adicione discos de dados adicionais, se necessário, para armazenamento separado dos dados da aplicação.

## 6. Configurar a Rede

- Na aba de **Rede**, associe a VM a uma **Rede Virtual (VNet)** já existente ou crie uma nova. A VNet define o ambiente de rede no qual sua VM será conectada.
- Configure uma **Sub-rede** para isolar a VM em um segmento específico da VNet.
- Defina as **regras de segurança de rede (NSG)**, que atuam como firewall, limitando o tráfego de entrada e saída da máquina virtual.
  - Habilite portas como **RDP** (para Windows) ou **SSH** (para Linux) se desejar acesso remoto à VM.

## 7. Definir Dimensionamento Automático (Autoescala)

- Para aplicações que variam em demanda, é possível configurar a **Autoescala**. Isso permite que o Azure ajuste automaticamente o número de instâncias da VM com base no uso de CPU, memória ou outros critérios.
- Configure as regras de escalabilidade baseadas em **métricas de desempenho** da VM.
  - Por exemplo, você pode definir que o número de instâncias aumente quando a utilização da CPU ultrapassar 70% por um determinado período de tempo.

## 8. Configurar Backups e Recuperação

- Habilite **backup automático** na aba de **Backup**. Isso permitirá que você configure políticas de backup para garantir a recuperação dos dados em caso de falhas.
- Defina a **retenção** de backups e o **agendamento** de acordo com as necessidades da sua aplicação.

## 9. Configurar o Dimensionamento Manual

- Para ambientes que precisam de ajustes manuais, você pode alterar o tamanho da VM ou adicionar novos recursos manualmente após a criação.
- No menu da máquina virtual, vá até **Dimensionar** para alterar o tipo de instância (mais memória, CPU ou armazenamento) de acordo com as mudanças na carga de trabalho.

## 10. Monitorar e Ajustar Desempenho

- Depois que a VM estiver funcionando, é importante monitorar o uso de recursos. No painel da VM, acesse **Métricas** para visualizar o consumo de CPU, memória e rede.
- Utilize **Alertas** para receber notificações quando os limites definidos forem atingidos, permitindo ajustes rápidos e evitando gargalos.

## 11. Revisar Configurações e Criar a VM

- Revise todas as configurações para garantir que estão corretas. Verifique os detalhes da rede, discos e dimensionamento.
- Clique em **Criar** e aguarde alguns minutos enquanto o Azure provisiona a máquina virtual.

## 12. Conectar-se à Máquina Virtual

- Após a criação da VM, use **RDP** para acessar VMs Windows ou **SSH** para acessar VMs Linux.
- No menu da VM, clique em **Conectar** para obter as instruções de conexão e iniciar o gerenciamento da VM.

## 13. Gerenciar e Dimensionar Após a Criação

- Você pode ajustar os recursos da VM a qualquer momento, acessando a aba de **Dimensionamento** no painel de configurações.
- Para ampliar a capacidade, considere **adicionar novas VMs** à sua rede ou usar um **Balanceador de Carga** para distribuir o tráfego entre múltiplas instâncias.

## Conclusão

Seguindo esses passos, você conseguirá configurar, ajustar e dimensionar uma máquina virtual no Azure, garantindo que ela atenda às suas necessidades de desempenho e custos.
