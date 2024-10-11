# Resumo do Laboratório da DIO
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO.

## Microsoft Azure - Localizando Serviços por Categoria
- A interface do portal do Microsoft Azure é a mesma para todos os usuários, independente se você está utilizando uma conta de teste ou paga. 
- No ícone de configurações é possível alterar o idioma e a região do portal. Também é possível definir a aparência e exibições de inicialização para personalizar o ambiente da forma que melhor lhe agrada.
- Ao clicar no botão "Todos os Serviços", um menu lateral será aberto mostrando todos os produtos do Azure, separados por categorias. Ao clicar em cada categoria você pode navegar por todos os serviços relacionados.

### Observações:
Todo produto disponível em versão prévia ainda não tem SLA (Service Level Agreements), logo, não há nenhuma garantia de que aquele produto continuará sendo oferecido. 
- Se você desenvolver algo utilizando um serviço em versão prévia e, em algum momento, essa aplicação parar de funcionar, não é possível recorrer com a Microsoft. 

## Criando Máquinas Virtuais na Azure
Cada SLA possui um tempo de inatividade aceitável por semana, mês e ano. 
| SLA | Tempo de inatividade por semana | Tempo de inatividade por mês | Tempo de inatividade por ano |
|-----|---------------------------------|------------------------------|------------------------------|
| 99% |           1,68 hora             |         7,2 horas            |           3,65 dias          |
| 99,9% |         10,1 minutos          |        43,2 minutos          |       8,76 horas             |
| 99,95% |          5 minutos           |        21,6 minutos          |          4,38 horas          |
| 99,99% |          1,01 minuto         |         4,32 minutos         |          52,56 minutos       |
| 99,999% |         6 segundos          |         25,9 segundos        |          5,26 minutos        |

### Observações:
- Ao criar uma máquina virtual, é possível definir as opções de disponibilidade e zona de disponibilidade.
- Ao criar uma conta de armazenamento, é possível definir o modelo de redundância (LRS, GRS, ZRS, GZRS).

## Configurando uma instância de Banco de Dados na Azure

### Criar máquina virtual
Ao selecionar a imagem da máquina virtual que será criada na Azure, a plataforma apresenta uma prévia de valor a pagar por aquela máquina por mês. 

### Criar Banco de Dados SQL
Ao criar um banco de dados, é necessário selecionar um servidor ou criar um servidor simbólico para ter acesso ao banco de dados. 
- Com base nas configurações, o portal irá apresentar uma previsão de custos por mês. 

## Construindo Arquiteturas no Azure
Neste laboratório, aprendemos a criar um grupo de recursos no Microsoft Azure, assim como inserir recursos dentro do grupo; 

### Como criar um grupo de recursos
- Selecionar "Grupo de Recursos" no menu do Azure (ou buscar utilizando a ferramenta de pesquisa)
- Selecionar assinatura;
- Definir nome do grupo de recursos;
- Selecionar região;
- Clicar em Revisar + Criar.

### Links úteis: 
- [Infraestruturada global do Azure](https://azure.microsoft.com/pt-br/explore/global-infrastructure)
- [Explore the Globe](https://datacenters.microsoft.com/)

## Configurando Recursos e Dimensionamento em Máquinas Virtuais na Azure
**Máquina virtual do Azure:** Cria uma VM hospedada pelo Azure.

**Máquina virtual do Azure com uma configuração predefinida:** Cria uma VM com predefinições com base em suas cargas de trabalho. Ex.: Modelo de teste, modelo de produção. 

### Criando uma máquina virtual
- Assinatura
- Grupo de recursos
- Região
- Opções de disponibilidade
- Zona de disponibilidade
- Definir disco, rede, gerenciamento, monitoramento, extensões, marcas
- Revisar + criar

Ao final, será apresentado uma previsão de custos para a VM configurada.

#### Condições de escala:
- Limite de instâncias - definir mínimo e máximo;
- Escalar horizontalmente - quando o limite de CPU atingir o valor x, aumentar a contagem de instâncias em y;
- Reduzir horizontalmente - quando o limite de CPU diminuir para o valor x, diminuir a contagem de instâncias em y;
- Duração da consulta em minutos.

### Criando uma Área de Trabalho Virtual do Azure

Tipos de pool de hosts:
- **Pessoal:** quando a máquina será destinada à alguém em específico, ninguém mais irá utilizar aquela máquina.
- **Pool:** quando a máquina será compartilhada por outras pessoas.

### Criando um Aplicativo de Funções
**Pilha de runtime:** .NET, Node.js, Python, Java, PowerShell Core, Custom Handler
- .NET: Windows e Linux
- Python: Linux
- Node.js: Windows e Linux
- Java: Windows e Linux

## Dominando o Armazenamento na Azure

Sobre o Storage Account (Conta de Armazenamento)

- Pode receber dados de diferentes tipos;
- O nome do Storage Account deve ser exclusivo globalmente;
- Aceita apenas letras minúsculas e números no nome de 3 a 24 caracteres.

É possível se conectar ao compartilhamento de arquivo do Azure por meio do Windows, Linux e macOS.
- Essa conexão irá acontecer em cima de um **SMB** (protocolo) e a porta **445**.

#### Desempenho:
| Tipo       | Recomendação                                                    |
|------------|-----------------------------------------------------------------|
|**Standard**| Recomendado para a maioria dos cenários – conta de uso geral v2.|
|**Premium:**| Recomendado para cenários que exigem baixa latência.|

##### Redundância:
| Modelo | Redundância |
|--------|-------------|
| LRS | Armazenamento com redundância local |
| ZRS | Armazenamento com redundância de zona |
| GRS | Armazenamento com redundância geográfica |
|GZRS | Armazenamento com redundância de zona geográfica |

### Migrações para Azure
Objetivos da migração:
- Servidores, banco de dados e aplicativos web;
- Banco de dados (somente);
- Aplicativos Web;
- Data Box.

##### Data Box:
- Data Box Disk: 35TB
- Data Box: 80TB
- Data Box Heavy: 800TB

### Modelos de sincronização de arquivos

#### AzCopy

É um utilitário de linha de comando que pode ser usado para copiar blobs ou arquivos de ou para uma conta de armazenamento. 

#### Storage Explorer

É um gerenciador de armazenamento do Azure. Oferece uma interface para realização das cópias a partir da área de trabalho. Realiza o mesmo procedimento do AzCopy, mas apresenta uma interface mais amigável para quem não quer utilizar linha de comando. 

## Entendendo sobre Segurança e Identidade na Azure

**Microsoft Entra ID:** é uma solução de gerenciamento de identidades e acesso na nuvem que conecta os usuários aos aplicativos, dispositivos e dados.
- Em um modelo de sincronização, os usuário do modelo on premise são copiados para a nuvem. Obs.: Se for criado um usuário na nuvem, não é possível replicar o usuário no modelo on premise. Apenas é possível trazer da nuvem as senhas de usuários que foram sincronizados. 

*Roles and Administrators*: se refere ao permissionamento em relação a outras contas. Ex.: meu usuário tem permissão para alterar a senha de outra pessoa. 
- O que conseguimos criar, excluir, remover, que diz respeito ao permissionamento para com a criação de recurso, está relacionado ao RBAC. O RBAC ajuda a gerenciar quem tem acesso aos recursos do Azure.

Os usuários do Microsoft Entra ID são permanentemente deletados autocaticamente após 30 dias em que foram deletados. 

**Self-Service Password Reset:** Pode ser programado para que quando o usuário não recordar a senha, ele ou ela possa trocar. 

**Microsoft Defender for Cloud:** é uma plataforma de CNAPP (proteção de aplicativo nativo de nuvem) composta de medidas e práticas de segurança projetadas para proteger os aplicativos baseados em nuvem contra ameaças e vulnerabilidades cibernéticas. 
- Multicloud (Azure, AWS, GCP)
- Híbrido

**DevOps Security:** a segurança DevOps dentro do Defender usa um console central para capacitar equipes de seguirança com a capacidade de proteger aplicativos e recursos do código para a nuvem em ambientes multi-pipeline, onde é possível conectar a conta do Azure DevOps, GitHub e GitLab. 

## Otimizando Custos no Azure

**Calculadora do TCO:** Estima a economia de custos gerada pela migração de cargas de trabalho para o Azure.

Modelos de carga de trabalho:
- Servidores
- Banco de Dados
- Armazenamento
- Rede

**Calculadora de preços:** Calcula os custos estimados por hora ou mensais para usar o Azure.  
Obs.: O login da página da calculadora de preços é um acesso fechado para grandes empresas que fecharam um contrato diretamente com a Microsoft. 

**Cost Management + Billing:** um serviço que ajuda a analisar, monitor e otimizar seus custos do Microsoft Cloud; entender e pagar sua fatura; e gerenciar sua conta de cobranças e assinaturas. 

### Links úteis:
- [Calculadora do TCO (Custo Total de Propriedade)](https://azure.microsoft.com/pt-br/pricing/tco/calculator/)
- [Calculadora de Preços](https://azure.microsoft.com/pt-br/pricing/calculator/)

## Gerenciando Políticas em Acessos Azure

O lock, ao contrário das TAGs (marcas) é herdado. Logo, ao aplicar um lock delete em um grupo de recursos, todas as aplicados do grupo são afetadas. 

### Microsoft Purview
É um conjunto de soluções que ajudam a organização a governar, proteger e gerenciar dados, onde quer que eles estejam. O Microsoft Purview combina soluções de governança de dados e soluções e serviços de conformidade do Microsoft 365 em uma plataforma unificada para ajudar a organização a:
- Obtenha visibilidade dos dados em toda a sua organização;
- Proteja e gerencie dados confidenciais durante todo o seu ciclo de vida, onde quer que estejam;
- Governe os dados perfeitamente de maneiras novas e abrangentes;
- Gerencie riscos de dados críticos e requisitos regulatórios.

### Azure Policy
Ajuda a impor padrões organizacionais e a avaliar a conformidade em escala. Fornece uma exibição agregada para avaliar o estado geral do ambiente, com a capacidade de drill down para a granularidade por recurso, por política.As políticas do Azure são aplicadas a nível de management group, assinatura, resource group etc.

#### Azure Policy x Azure RBAC
**Azure Policy:** garante que o estado do recurso esteja em conformidade com as regras de negócio sem levar em conta quem fez a alteração ou quem tem permissão para fazer uma alteração. 

**Azure RBAC:** concentra-se em gerenciar as ações do usuário em escopos diferentes. Mesmo que um indivíduo tenha acesso para executar uma ação, se o resultado do recurso não estiver em conformidade com as políticas do negócio, o Azure Policy irá bloquear a ação ou atualização. 

### Links Úteis
- [Portal de Confiança do Serviço](https://servicetrust.microsoft.com/)
- [O que é o Azure Policy?](https://learn.microsoft.com/pt-br/azure/governance/policy/overview)

