# resumo-do-lab
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO

Aprendi a como criar uma conta no azure e um pouco sobre as ferramentas que ele tem para oferecer.

#Criação de máquinas virtuais

#Configuração banco de dados na Azure

Entre no Portal do Azure.
Criar uma Rede Virtual:
No menu à esquerda, clique em “Redes virtuais”.
Clique em “+ Criar”.
Configurações Básicas:
Assinatura: Selecione sua assinatura do Azure.
Grupo de Recursos: Escolha um grupo de recursos existente ou crie um novo.
Nome: Dê um nome para sua rede virtual.
Região: Selecione a região onde deseja criar a rede.
Configurações de Endereço IP:
Espaço de Endereço IPv4: Defina o intervalo de endereços IP (por exemplo, 10.0.0.0/16).
Sub-rede: Adicione uma sub-rede (por exemplo, 10.0.0.0/24).
Segurança e Tags (opcional):
Configure opções de segurança, como grupos de segurança de rede (NSG), se necessário.
Adicione tags para organizar seus recursos.
Revisar e Criar:
Revise todas as configurações.
Clique em “Criar” para iniciar a implantação.
Verificar a Rede Virtual:
Após a implantação, verifique os detalhes da rede virtual criada.

#Configurando recursos e dimensionamentos em máquinas virtuais

Escolha do Tipo de Máquina Virtual:
O Azure oferece várias séries de VMs, como:
Série A: Para cargas de trabalho de entrada de baixo custo.
Série D, E: Para aplicações de negócios e bancos de dados.
Série F: Alta performance focada em CPU.
Série G: Alta memória e desempenho em armazenamento.
Série N: Com GPU para processamento gráfico e machine learning1.
Dimensionamento de Recursos:
CPU e Memória: Selecione o número de vCPUs e a quantidade de memória RAM conforme a carga de trabalho.
Armazenamento: Escolha entre discos HDD (desempenho padrão) ou SSD Premium (alta performance).
Rede: Configure interfaces de rede, balanceamento de carga e segurança conforme necessário2.
Dimensionamento Vertical e Horizontal:
Vertical (Scaling Up/Down): Alteração dos recursos da VM (CPU/RAM) dentro da mesma instância.
Horizontal (Scaling Out/In): Adição ou remoção de instâncias de VMs para balanceamento de carga e alta disponibilidade2.
Configurações Avançadas:
Zonas de Disponibilidade: Para alta disponibilidade e recuperação de desastres.
Grupos de Dimensionamento: Para gerenciar múltiplas VMs de forma escalável e automatizada.
Extensões e Scripts: Adicionar softwares adicionais ou scripts de configuração2.
Automação e Monitoramento:
Auto Scaling: Regras de auto-escalabilidade para ajustar automaticamente o número de VMs baseado em métricas.
Azure Monitor: Para monitoramento de desempenho e ajuste proativo dos recursos

#Armazenamento no Azure

##Blobs do Azure:
Armazenamento de objetos para grandes quantidades de dados não estruturados, como documentos, imagens e vídeos.
Suporta análise de Big Data com o Data Lake Storage Gen21.
##Arquivos do Azure:
Compartilhamentos de arquivos gerenciados que podem ser acessados via SMB e NFS.
Ideal para migração lift-and-shift de aplicativos que usam APIs de sistema de arquivos nativo1.
##Discos Gerenciados do Azure:
Volumes de armazenamento no nível do bloco para VMs.
Oferece alta disponibilidade e durabilidade1.
##Filas do Azure:
Armazenamento de mensagens para comunicação entre componentes de aplicativos.
Útil para sistemas distribuídos e processamento assíncrono1.
##Tabelas do Azure:
Armazenamento NoSQL para dados estruturados sem esquema.
Bom para aplicativos web e dados de telemetria1.
##Azure NetApp Files:
Serviço de NAS gerenciado para cargas de trabalho de alto desempenho.
Suporta volumes NFS, SMB e protocolo duplo1.
Esses serviços são altamente escalonáveis, seguros e acessíveis globalmente, permitindo que você escolha a solução de armazenamento que melhor se adapta às suas necessidades.

#Segurança e integridade no Azure

Azure Active Directory (Azure AD):
Gerenciamento de Identidade: Centraliza a gestão de identidades e permite o logon único (SSO) para acessar múltiplos aplicativos.
Autenticação Multifator (MFA): Adiciona uma camada extra de segurança exigindo mais de uma forma de verificação1.
Controle de Acesso Baseado em Função (RBAC):
Permissões Granulares: Define permissões específicas para usuários e grupos, garantindo que eles tenham apenas o acesso necessário2.
Acesso Condicional:
Políticas de Segurança: Cria políticas que controlam o acesso com base em condições específicas, como localização e dispositivo1.
Microsoft Defender para Nuvem:
Proteção Contínua: Monitora e protege suas cargas de trabalho no Azure, fornecendo insights detalhados e recomendações de segurança3.
Privileged Identity Management (PIM):
Gerenciamento de Acesso Privilegiado: Controla e monitora o acesso a recursos críticos, reduzindo o risco de acesso não autorizado2.
Esses componentes ajudam a garantir que suas identidades e dados estejam protegidos contra ameaças, mantendo a conformidade e a segurança operacional.

#Custos no Azure

Modelo de Pagamento:
Pague pelo que usar: Você paga apenas pelos recursos que consumir, sem custos iniciais.
Preços por hora ou mensal: Os custos podem ser calculados com base no uso por hora ou mensal1.
Calculadora de Preços do Azure:
Ferramenta de Estimativa: Permite calcular os custos estimados para diferentes serviços e configurações no Azure. Você pode acessar a Calculadora de Preços do Azure para planejar seu orçamento1.
Opções de Economia:
Reservas do Azure: Economize até 72% ao reservar recursos por um ou três anos.
Benefício Híbrido do Azure: Use suas licenças existentes do Windows Server e SQL Server para economizar em VMs2.
Gerenciamento de Custos:
Microsoft Cost Management: Monitore e analise seus gastos, defina orçamentos e aloque custos para diferentes equipes e projetos3.
Relatórios e Alertas: Receba relatórios detalhados e configure alertas para manter o controle dos seus gastos3.
Serviços Gratuitos:
Camada Gratuita do Azure: Oferece serviços gratuitos por 12 meses e mais de 25 serviços sempre gratuitos, como máquinas virtuais, armazenamento e bancos de dados2.
Essas ferramentas e opções ajudam a gerenciar e otimizar seus custos no Azure, garantindo que você obtenha o melhor valor para seus investimentos em nuvem.

#Gerenciamento em políticas de acesso no Azure

Controle de Acesso Baseado em Função (RBAC):
RBAC do Azure: Permite gerenciar quem tem acesso aos recursos do Azure, o que eles podem fazer e em que escopo. Você pode atribuir funções específicas a usuários, grupos ou aplicativos, como Owner, Contributor e Reader1.
Políticas do Azure:
Definição de Regras: As políticas ajudam a impor regras e garantir que os recursos estejam em conformidade com os padrões da organização. Por exemplo, você pode criar políticas para garantir que apenas tipos específicos de VMs sejam criados2.
Azure Active Directory (Azure AD):
Gerenciamento de Identidade: Centraliza a gestão de identidades e permite o controle de acesso a recursos. Inclui funcionalidades como Autenticação Multifator (MFA) e Acesso Condicional3.
Políticas de Condição de Acesso:
Regras Baseadas em Condições: Permitem aplicar regras específicas baseadas em condições como localização, dispositivo ou aplicativo utilizado. Isso ajuda a reforçar a segurança com base em contextos específicos3.
Monitoramento e Auditoria:
Azure Monitor e Logs de Auditoria: Ferramentas para monitorar e auditar atividades de acesso e alterações em políticas de segurança. Isso ajuda a identificar e responder rapidamente a anomalias2.
Esses componentes trabalham juntos para fornecer um gerenciamento robusto e seguro de políticas de acesso no Azure.

#Ferramentas de implementação na Azure

Azure DevOps:
Pipelines de CI/CD: Automatiza a construção, teste e implantação de aplicativos. Integra-se com GitHub, Bitbucket e outros repositórios de código1.
Azure Resource Manager (ARM):
Modelos ARM: Permite definir a infraestrutura como código, facilitando a criação, atualização e exclusão de recursos de forma consistente2.
Terraform:
Infraestrutura como Código: Utiliza a linguagem HCL para definir e provisionar a infraestrutura do Azure de maneira declarativa e repetível2.
Ansible, Chef e Puppet:
Automação de Configuração: Ferramentas para gerenciar a configuração e o estado desejado das máquinas virtuais e outros recursos2.
Azure Automation:
Runbooks e DSC: Automatiza tarefas repetitivas e gerencia a configuração de VMs usando runbooks e Desired State Configuration (DSC)2.
Bicep:
DSL para ARM: Uma linguagem específica de domínio que simplifica a escrita de modelos ARM, tornando-os mais legíveis e fáceis de gerenciar2.
Essas ferramentas ajudam a simplificar e automatizar o processo de implementação, garantindo consistência, eficiência e segurança na gestão dos recursos do Azure.

