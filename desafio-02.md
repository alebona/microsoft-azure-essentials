# Configuração de Instância de Banco de Dados no Azure

## 1. Acesse o Portal do Azure
- Abra o [Portal do Azure](https://portal.azure.com) e faça login com sua conta.

## 2. Iniciar a Criação do Banco de Dados
- No painel do Azure, vá até a barra de pesquisa e digite **Banco de Dados SQL** ou **SQL Database**.
- Clique em **Criar** para iniciar o processo de configuração de um novo banco de dados.

## 3. Preencher as Informações Básicas
- **Nome do Banco de Dados**: Defina um nome único e fácil de identificar.
- **Assinatura**: Escolha a assinatura do Azure que será utilizada.
- **Grupo de Recursos**: Selecione um grupo de recursos existente ou crie um novo.
- **Servidor**: Selecione um servidor SQL existente ou crie um novo servidor.
  - Se for criar um novo servidor, você precisará definir:
    - **Nome do Servidor**: Escolha um nome exclusivo para o servidor SQL.
    - **Localização**: Selecione a região para hospedar o servidor.
    - **Autenticação**: Defina o **Nome de Usuário do Administrador** e a **Senha**.

## 4. Definir o Plano de Serviço do Banco de Dados
- Escolha o plano de serviço que melhor atenda às suas necessidades. As opções incluem:
  - **Uso Baseado em Consumo** (Paga pelo uso que fizer).
  - **Uso Preditivo (Camadas Provisionadas)**: Oferece melhor desempenho com custo fixo mensal.

## 5. Configuração de Backup e Redundância
- Selecione a opção de **Redundância Geográfica** para backups automáticos e recuperação de desastres.
  - **Redundância Local**: Para backups dentro da mesma região.
  - **Redundância Geográfica**: Para backups entre regiões, aumentando a resiliência.

## 6. Configuração de Segurança
- **Camadas de Segurança**: Habilite **Azure Defender for SQL** para monitoramento avançado e detecção de ameaças.
- **Firewall do Servidor**: Defina as regras de acesso ao banco de dados. 
  - Adicione seu IP para permitir acesso.
  - Habilite a opção para permitir **Acesso a Serviços do Azure**.

## 7. Revisar e Criar
- Verifique todas as opções configuradas, incluindo o tamanho, o plano de serviço, a segurança e as opções de backup.
- Clique em **Criar** e aguarde o provisionamento do banco de dados.

## 8. Conectar ao Banco de Dados
Após a criação do banco de dados:
- Utilize uma ferramenta como o **Azure Data Studio** ou **SQL Server Management Studio (SSMS)** para se conectar ao banco de dados.
- Use o **Nome do Servidor**, **Nome de Usuário** e **Senha** que você configurou para autenticar sua conexão.

