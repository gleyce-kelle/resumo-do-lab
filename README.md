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
