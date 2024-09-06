# Gerenciando Políticas de Acessos no Azure

A gestão de acessos no Azure envolve a aplicação de políticas e controle de permissões para garantir que os usuários tenham o nível de acesso correto. Vamos detalhar como criar, gerenciar e aplicar políticas de acesso no Azure.

## 1. Entendendo o Controle de Acesso Baseado em Funções (RBAC)

O **RBAC (Role-Based Access Control)** é o modelo de gerenciamento de permissões no Azure. Ele permite atribuir funções específicas a usuários, grupos ou aplicativos, restringindo ou concedendo permissões.

- No **RBAC**, as permissões são definidas por **funções**.
  - Exemplos de funções:
    - **Owner**: Acesso total para gerenciar recursos.
    - **Contributor**: Pode criar e gerenciar recursos, mas não alterar permissões.
    - **Reader**: Pode visualizar recursos, mas não modificar.

## 2. Atribuindo Funções a Usuários e Grupos

Você pode atribuir funções diretamente a usuários, grupos ou identidades gerenciadas.

- No portal do Azure, navegue até o **Recurso** ou **Grupo de Recursos** que deseja gerenciar.
- Clique em **Controle de Acesso (IAM)**.
- Selecione **Adicionar Atribuição de Função**.
  - Escolha uma função, como **Leitor** ou **Contribuidor**.
  - Selecione o usuário ou grupo ao qual deseja conceder a função.
- Confirme a atribuição clicando em **Salvar**.

### Dica:
- Ao atribuir funções em níveis mais altos, como em uma **Assinatura**, os usuários herdarão essas permissões em todos os recursos dentro dessa assinatura.

## 3. Utilizando Políticas do Azure (Azure Policy)

As **políticas do Azure** ajudam a impor regras e garantir a conformidade em toda a sua organização. Com as políticas, você pode restringir determinadas ações ou exigir que certas condições sejam atendidas.

- No portal do Azure, procure por **Políticas**.
- Clique em **Atribuições de Política**.
- Selecione **Atribuir Política** e escolha o **escopo** da política, como uma assinatura ou grupo de recursos.
  - Exemplo de política: **Exigir tag em recursos** ou **Restringir o tipo de máquina virtual**.
- Defina os parâmetros da política, se aplicável, e clique em **Revisar e Criar**.

### Exemplo:
- Você pode criar uma política que force a aplicação de tags a todos os recursos, facilitando a organização e monitoramento de custos.

## 4. Monitorando o Acesso com Azure Active Directory (Azure AD)

O **Azure Active Directory** (Azure AD) é o serviço de gerenciamento de identidade e acesso do Azure. Ele permite gerenciar quem tem acesso a quais recursos e monitorar atividades.

### Adicionando Usuários:
- No portal do Azure, vá até **Azure Active Directory** > **Usuários**.
- Selecione **Novo Usuário** para adicionar um novo usuário à sua organização.
- Preencha as informações necessárias, como nome, email e função inicial.

### Gerenciando Grupos:
- Em **Azure AD**, vá até **Grupos**.
- Crie um novo grupo para organizar usuários com permissões semelhantes.
- Atribua funções de acesso a esses grupos para simplificar o gerenciamento.

## 5. Configurando Políticas de Condição de Acesso

As **políticas de condição de acesso** permitem aplicar regras específicas baseadas em condições, como local, dispositivo ou aplicativo utilizado.

- No portal do Azure, vá para **Azure Active Directory** > **Segurança** > **Condições de Acesso**.
- Crie uma nova política clicando em **Nova Política**.
- Defina **Usuários e Grupos** aos quais a política será aplicada.
- Configure as condições, como o local do usuário (Ex: restringir o acesso fora do escritório) ou o aplicativo utilizado.
- Configure os controles de acesso: exija autenticação multifator (MFA) ou bloquear acesso.
- Salve e ative a política.

### Dica:
- **MFA** (autenticação multifator) é uma medida de segurança eficaz para proteger contas com mais de um fator de autenticação.

## 6. Revisando Logs de Auditoria e Acessos

O **Azure Monitor** e os **Logs de Auditoria** permitem que você monitore a atividade de acesso e faça auditoria de alterações em políticas de segurança.

- No portal do Azure, vá para **Monitor** > **Logs de Auditoria**.
- Visualize as atividades relacionadas a acessos e permissões, como:
  - Quem atribuiu uma função a determinado usuário.
  - Quais políticas foram aplicadas ou alteradas.

Você também pode configurar alertas para ser notificado sobre eventos específicos, como a atribuição de uma função crítica.

## 7. Aplicando a Prática de Privilégio Mínimo

Para garantir a segurança, siga a prática de **privilégio mínimo** ao atribuir acessos.

- Atribua apenas as permissões necessárias para que os usuários executem suas funções.
- Evite conceder permissões de **Owner** ou **Contributor** se o acesso de leitura for suficiente.

## 8. Revisando Periodicamente as Políticas de Acesso

Realize revisões periódicas das atribuições de acesso e políticas para garantir que os usuários continuem tendo apenas as permissões necessárias.

- No portal do Azure, em **Controle de Acesso (IAM)**, revise todas as atribuições de função.
- Use o **Azure AD Access Reviews** para identificar e remover acessos desnecessários automaticamente.

## Conclusão

O gerenciamento eficaz de políticas de acesso no Azure é fundamental para manter a segurança e conformidade em sua organização. Com o uso do RBAC, políticas do Azure e o monitoramento contínuo, você pode garantir que os usuários tenham acesso adequado, sem comprometer a integridade dos sistemas.
