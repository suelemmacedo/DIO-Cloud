**Desafio - Cloud Computing**

**Resumo - Laboratório**

A computação em nuvem oferece recursos de TI, como armazenamento e servidores, através da internet de forma sob demanda, permitindo que empresas paguem apenas pelo que utilizam, sem precisar investir em infraestrutura própria. Existem três tipos de nuvens: a pública, que é compartilhada entre várias empresas e oferecida por provedores como AWS e Azure; a privada, dedicada a uma única organização, proporcionando mais controle sobre segurança e conformidade; e a híbrida, que combina as duas anteriores, oferecendo flexibilidade ao compartilhar dados e aplicações.

Nos modelos de despesas, o CAPEX (Capital Expenditure) envolve grandes investimentos em infraestrutura física, enquanto o OPEX (Operational Expenditure) está relacionado aos custos de operação e consumo dos serviços de nuvem. A computação em nuvem funciona em um modelo baseado em consumo, no qual as empresas pagam apenas pelos recursos utilizados, proporcionando escalabilidade, flexibilidade e melhor controle dos custos operacionais.

O **SLA (Service Level Agreement)** da Azure define o nível de garantia para a disponibilidade e desempenho dos serviços oferecidos pela Microsoft. Ele especifica o tempo de atividade garantido, que pode variar entre 99,9% e 99,99%, dependendo do serviço e da configuração utilizada. A alta disponibilidade pode ser alcançada usando zonas de disponibilidade e replicação geográfica. Caso o SLA não seja cumprido, o cliente pode receber **créditos** como compensação. A Azure oferece SLAs diferenciados para serviços essenciais, como máquinas virtuais, bancos de dados e serviços de aplicativo, recomendando sempre a configuração adequada para maximizar a resiliência e minimizar falhas.

### Tabela de SLA e Tempo de Inatividade

| **Disponibilidade (SLA)** | **Tempo de Inatividade Permitido por Mês** | **Tempo de Inatividade Permitido por Ano** |
|---------------------------|-------------------------------------------|-------------------------------------------|
| 99,9%                     | 43 minutos e 49 segundos                   | 8 horas e 45 minutos                      |
| 99,95%                    | 21 minutos e 54 segundos                   | 4 horas e 22 minutos                      |
| 99,99%                    | 4 minutos e 23 segundos                    | 52 minutos e 36 segundos                  |
| 99,999%                   | 26 segundos                                | 5 minutos e 15 segundos                   |

Essa tabela mostra os tempos de inatividade permitidos de acordo com o SLA de disponibilidade garantido para os serviços da Azure.

**Tipos de Serviços de Nuvem**

Aqui está uma tabela comparando IaaS, PaaS e SaaS:

| **Características**            | **IaaS (Infrastructure as a Service)**          | **PaaS (Platform as a Service)**             | **SaaS (Software as a Service)**              |
|---------------------------------|------------------------------------------------|---------------------------------------------|----------------------------------------------|
| **Definição**                   | Infraestrutura de TI fornecida via nuvem, como servidores e armazenamento. | Plataforma para desenvolver e gerenciar aplicações, sem se preocupar com a infraestrutura. | Software completo entregue via web, que o usuário acessa e utiliza diretamente. |
| **Controle do usuário**         | Controle sobre hardware, rede, armazenamento, sistemas operacionais, etc. | Controle sobre as aplicações e dados; a infraestrutura subjacente é gerenciada pelo provedor. | Controle apenas sobre os dados e configurações da aplicação. |
| **Exemplos de serviços**        | Amazon EC2, Microsoft Azure VMs, Google Compute Engine. | Google App Engine, Heroku, Microsoft Azure App Services. | Google Workspace, Salesforce, Microsoft 365. |
| **Gerenciamento pelo provedor** | Gerenciamento de servidores, rede e armazenamento. O sistema operacional e as aplicações são gerenciados pelo cliente. | Gerenciamento da infraestrutura e middleware. O cliente cuida apenas das aplicações. | Gerenciamento completo, incluindo software, infraestrutura e atualizações. |
| **Flexibilidade**               | Alta flexibilidade para configurar e gerenciar recursos de TI. | Flexibilidade moderada para desenvolver e implementar aplicações. | Flexibilidade limitada, o foco é na usabilidade e conveniência. |
| **Público-alvo**                | Equipes de TI, desenvolvedores que precisam de controle sobre a infraestrutura. | Desenvolvedores que querem focar no código sem se preocupar com a infraestrutura. | Usuários finais e empresas que precisam de soluções prontas. |
| **Custos**                      | Custo sob demanda, dependendo do uso da infraestrutura. | Custo baseado na utilização da plataforma e dos recursos de desenvolvimento. | Custo geralmente baseado em assinatura para o uso do software. |
| **Escalabilidade**              | Escalável conforme a necessidade do cliente.    | Escalável para o desenvolvimento e gestão de aplicações. | Escalável conforme o número de usuários e recursos. |

### **Responsabilidade Compartilhada**
O modelo de responsabilidade compartilhada é uma abordagem usada pelos provedores de serviços de nuvem para definir claramente quem é responsável por cada aspecto da segurança e gerenciamento dos serviços oferecidos.

- **Provedor de Nuvem**: Responsável pela segurança da **nuvem**, ou seja, pela infraestrutura subjacente que inclui servidores, armazenamento, rede, e data centers.
- **Cliente/Usuário**: Responsável pela segurança **na nuvem**, o que inclui o gerenciamento de acesso, configuração de aplicações, proteção de dados, e qualquer atividade realizada sobre os recursos fornecidos pelo provedor.

O nível de responsabilidade varia dependendo do serviço:
- **IaaS**: O cliente tem mais responsabilidades (gerenciamento de sistemas operacionais, dados e aplicações).
- **PaaS**: O provedor assume mais controle da infraestrutura, enquanto o cliente gerencia as aplicações e dados.
- **SaaS**: O provedor é responsável pela maior parte da infraestrutura e segurança, restando ao cliente cuidar dos dados e configurações de usuário.

**Componentes de Arquitetura do Azure**

A arquitetura do Azure é construída sobre uma infraestrutura global que inclui **regiões**, **zonas de disponibilidade**, **pares de região** e **regiões soberanas**, além de diversos **recursos** que garantem alta disponibilidade, resiliência e segurança para as aplicações e serviços.

**Regiões do Azure** são áreas geográficas que contêm um ou mais data centers, projetadas para proporcionar proximidade com os usuários e conformidade com regulamentações locais. Cada região oferece um conjunto completo de serviços do Azure, permitindo que os usuários escolham a melhor localização para hospedar suas aplicações, otimizando latência e desempenho. Exemplos incluem regiões como "Leste dos EUA", "Europa Ocidental" e "Sudeste Asiático".

Dentro de cada região, o Azure disponibiliza as **zonas de disponibilidade**, que são locais físicos separados com suas próprias fontes de energia, refrigeração e rede, garantindo resiliência em caso de falhas de data centers. Cada zona é independente e, ao implantar recursos em várias zonas, as aplicações podem alcançar alta disponibilidade e tolerância a falhas.

Um conceito chave da infraestrutura global do Azure é o de **pares de região**, que são duas regiões dentro da mesma área geográfica emparelhadas entre si para garantir recuperação de desastres e replicação de dados. Um dos principais benefícios dos pares de região é que, em caso de manutenção ou interrupção planejada em uma região, a outra permanece disponível, minimizando o impacto sobre os serviços. Um exemplo clássico é o par de regiões "Leste dos EUA" e "Oeste dos EUA".

Além disso, o Azure oferece **regiões soberanas**, projetadas especificamente para atender a requisitos de soberania de dados e conformidade em determinados países. Essas regiões são operadas de forma independente das outras regiões globais e incluem o **Azure China** e o **Azure Government** (nos EUA), que seguem regulamentações rigorosas quanto à localização e acesso aos dados.

Os **recursos do Azure** incluem uma vasta gama de serviços e produtos que podem ser usados para construir, gerenciar e escalar soluções na nuvem. Entre esses recursos, destacam-se o **Azure Compute**, que abrange máquinas virtuais, contêineres e serviços de computação serverless; o **Azure Storage**, que oferece armazenamento de arquivos, discos e objetos (como Blob Storage); e os bancos de dados gerenciados, como o **Azure SQL Database** e o **Cosmos DB**. Há também recursos de rede, como o **Azure Virtual Network (VNet)** e o **Azure Load Balancer**, que garantem conectividade e distribuição de tráfego, além de ferramentas de segurança, como o **Azure Active Directory** e o **Azure Security Center**.

Essa arquitetura robusta e distribuída globalmente do Azure oferece flexibilidade para atender a diversas necessidades de negócios e conformidade, permitindo que organizações escolham onde e como implantar seus serviços com alta disponibilidade, segurança e resiliência.

Os **serviços de computação e máquinas virtuais** do **Azure** oferecem uma infraestrutura flexível para rodar aplicações, gerenciar cargas de trabalho e escalonar recursos de acordo com a demanda. As **máquinas virtuais (VMs) do Azure** são instâncias de servidores que podem ser configuradas com diferentes sistemas operacionais, tamanhos e funcionalidades, permitindo que as organizações hospedem desde pequenas aplicações até ambientes corporativos complexos. Com o **Conjunto de Dimensionamento de VMs**, é possível criar e gerenciar um grupo de VMs idênticas, facilitando o aumento automático de recursos conforme a demanda aumenta, garantindo alta disponibilidade e desempenho. O **Conjunto de Disponibilidade de VMs** oferece redundância e resiliência, distribuindo máquinas virtuais em diferentes domínios de falha e atualização, garantindo que as aplicações permaneçam online mesmo em situações de manutenção ou falhas físicas.

A **Área de Trabalho Virtual do Azure (Azure Virtual Desktop)** permite que usuários acessem remotamente um ambiente Windows completo e virtualizado. Esse serviço é muito útil para empresas que precisam fornecer desktops seguros e escaláveis para seus funcionários, com gerenciamento simplificado e integração com outros serviços do Azure.

Os **serviços de contêineres** do Azure, como o **Azure Container Instances (ACI)**, permitem que contêineres sejam executados de forma isolada e sem a necessidade de gerenciar a infraestrutura subjacente. Já o **Azure Kubernetes Service (AKS)** é uma solução gerenciada para orquestrar contêineres usando o Kubernetes, oferecendo escalabilidade e automação para implantações em contêineres.

O **Azure Functions** é um serviço de computação serverless, que permite executar pequenas peças de código em resposta a eventos, eliminando a necessidade de gerenciar servidores. É ideal para automação de tarefas e processamento de eventos em tempo real.

Por fim, os **serviços de rede do Azure** garantem conectividade e segurança robustas para as infraestruturas. Com o **Azure Virtual Network (VNet)**, é possível criar redes virtuais isoladas, conectar diferentes VMs e integrar ambientes on-premises com a nuvem. Além disso, há serviços como o **Azure Load Balancer**, que distribui o tráfego de rede de maneira eficiente, e o **Azure Application Gateway**, que oferece balanceamento de carga com inspeção de nível de aplicação.
