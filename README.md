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
