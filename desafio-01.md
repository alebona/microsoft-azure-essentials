# Criação de Máquina Virtual no Azure - Redundância/SLA

## 1. Acesse o Portal do Azure
Primeiro, [entre no portal do Azure](https://portal.azure.com). É onde você vai gerenciar todos os seus recursos.

## 2. Iniciando a Criação da Máquina Virtual
No painel principal do Azure, digite **Máquinas Virtuais** na barra de pesquisa. Clique em **Criar** para começar o processo de configuração.

## 3. Preencha as Informações Básicas
- **Nome da máquina virtual**: Escolha um nome que facilite a identificação da sua máquina virtual.
- **Localização**: Selecione a **região** onde a máquina virtual será criada. Escolha uma região próxima aos usuários ou à sua base de operação.
- **Imagem**: Selecione o sistema operacional desejado, como **Linux** ou **Windows**.
- **Tamanho**: Defina o **tamanho** da máquina virtual com base nas suas necessidades de processamento, memória e armazenamento.

## 4. Configuração da Rede
- **Rede Virtual**: Crie ou escolha uma **rede virtual** já existente.
- **Sub-rede**: Defina a **sub-rede** para a qual a máquina virtual estará conectada.
- **Grupo de Segurança de Rede (NSG)**: Configure as regras de acesso e segurança para a máquina virtual.

## 5. Configure as Credenciais de Acesso
- **Nome de Usuário e Senha**: Defina o **nome de usuário** e uma **senha forte** para garantir a segurança de login na máquina virtual.

## 6. Revisão e Criação
Revise todas as opções configuradas para garantir que estejam corretas. Clique em **Criar** e aguarde a criação da sua máquina virtual.

## 7. Conexão com a máquina virtual
Após a criação da máquina virtual, você pode se conectar a ela:
- Para máquina virtual **Windows**, utilize o **Remote Desktop (RDP)**.
- Para máquina virtual **Linux**, utilize o **SSH**.
