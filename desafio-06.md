# Entendendo sobre Segurança e Identidade na Azure

A segurança e o gerenciamento de identidade são pilares fundamentais na Azure. Este guia oferece um passo a passo para entender e configurar os principais recursos relacionados à segurança e identidade na plataforma.

## 1. Introdução ao Azure Active Directory (Azure AD)

O **Azure Active Directory (Azure AD)** é o serviço de identidade da Microsoft, utilizado para gerenciar usuários, grupos e permissões de acesso em todos os serviços da Azure.

- **Acesso ao Azure AD**: No portal do Azure, procure por **Azure Active Directory** na barra de pesquisa.
- **Usuários**: Crie e gerencie usuários no Azure AD. Esses usuários podem acessar serviços da Azure, como VMs e aplicativos SaaS.
  - Para criar um usuário, vá em **Usuários** e clique em **Novo usuário**.
  - Preencha os detalhes, como nome, nome de usuário e grupo de segurança.
- **Grupos**: Utilize grupos para gerenciar permissões em escala. Adicione usuários a grupos com permissões específicas.
  - Vá para **Grupos** e clique em **Novo grupo** para criar um grupo.
  - Defina o tipo de grupo e atribua membros.

## 2. Configurar Multi-Factor Authentication (MFA)

A **Autenticação Multifator (MFA)** adiciona uma camada extra de segurança, exigindo dois ou mais métodos de autenticação.

- No painel do **Azure AD**, vá até **Segurança** e selecione **Autenticação multifator**.
- Habilite MFA para usuários ou grupos específicos, exigindo que eles utilizem uma segunda forma de autenticação, como um SMS ou aplicativo de autenticação.

## 3. Gerenciamento de Funções e Atribuições (RBAC)

O **Controle de Acesso Baseado em Funções (RBAC)** permite que você controle quem tem acesso a quais recursos, atribuindo permissões específicas a usuários ou grupos.

- **Acesso a RBAC**: Vá até o recurso desejado (como uma VM ou banco de dados) e selecione **Controle de Acesso (IAM)**.
- **Atribuir Funções**: Clique em **Atribuir função** e selecione a função desejada (como **Colaborador**, **Leitor** ou **Proprietário**).
  - Atribua a função a um usuário ou grupo existente no Azure AD.

## 4. Implementar Políticas de Segurança com Azure Policy

O **Azure Policy** ajuda a garantir que todos os recursos na sua assinatura estejam em conformidade com as políticas de segurança e governança da organização.

- No portal do Azure, procure por **Política**.
- Clique em **Criar Política** para definir restrições ou requisitos, como criptografia obrigatória em discos de VMs ou a desativação de IPs públicos.
- Aplique a política em assinaturas, grupos de recursos ou diretamente nos recursos.

## 5. Configurar a Proteção de Identidade com Azure AD Identity Protection

O **Azure AD Identity Protection** automatiza a detecção de identidades comprometidas e responde a riscos de segurança.

- No painel do Azure AD, vá até **Segurança** e selecione **Proteção de Identidade**.
- Ative a detecção de riscos para contas de usuários e configure políticas de resposta automática.
  - Exemplo: bloqueio de login se um risco for detectado, exigindo a redefinição de senha.

## 6. Monitoramento de Acesso e Segurança com Azure Security Center

O **Azure Security Center** oferece uma visão abrangente da segurança dos seus recursos, com recomendações para fortalecer a postura de segurança.

- No portal, acesse **Security Center**.
- Configure **alertas de segurança** e monitore vulnerabilidades em tempo real.
- Ative a **proteção avançada** para servidores, bancos de dados e redes.

## 7. Criptografia de Dados em Repouso e em Trânsito

- **Criptografia em Repouso**: Todos os dados armazenados na Azure são automaticamente criptografados em repouso usando tecnologias como **Storage Service Encryption** (SSE).
  - Verifique a criptografia no painel do recurso de armazenamento ou VM.
- **Criptografia em Trânsito**: Certifique-se de que as comunicações entre seus recursos estão criptografadas com HTTPS, SSL/TLS ou IPsec.

## 8. Configurar Firewalls e Grupos de Segurança de Rede (NSG)

Firewalls e **Grupos de Segurança de Rede (NSG)** ajudam a proteger suas redes e VMs contra acessos não autorizados.

- Para configurar um NSG, vá até o painel da sua **Máquina Virtual** ou **Rede Virtual**.
- Em **Grupos de Segurança de Rede**, defina regras de entrada e saída, especificando portas, IPs e protocolos permitidos ou bloqueados.
- Utilize o **Firewall da Azure** para controlar o tráfego entre redes ou com a internet, criando regras de acesso mais abrangentes.

## 9. Auditar Acessos e Logins

O **Azure Monitor** e o **Log Analytics** permitem rastrear e registrar todas as tentativas de acesso e atividade de login nos recursos da Azure.

- Acesse o **Azure Monitor** e configure **diagnósticos** para acompanhar atividades como tentativas de login, alterações de configuração e eventos de segurança.
- Revise os **logs** regularmente para identificar comportamentos suspeitos.

## 10. Gerenciar Certificados e Chaves com Azure Key Vault

O **Azure Key Vault** permite armazenar e gerenciar segredos, certificados e chaves criptográficas de forma segura.

- No painel do Azure, busque por **Key Vault** e crie um novo cofre de chaves.
- Adicione segredos, chaves ou certificados, e defina permissões de acesso através de RBAC ou políticas de acesso.
- Utilize o Key Vault para armazenar credenciais de aplicativos ou certificados SSL, garantindo a proteção de informações sensíveis.

## Conclusão

Compreender e dominar a segurança e identidade na Azure é essencial para garantir a proteção dos seus recursos e dados. Através do Azure Active Directory, MFA, RBAC, políticas de segurança e criptografia, você pode fortalecer suas práticas de segurança e controlar o acesso aos seus serviços.
