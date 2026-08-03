# Enciclopédia Regional do Brasil (br-counties)

Bem-vindo à documentação oficial do projeto **br-counties**. Esta Wiki atua como um atlas aberto e enciclopédia de inteligência territorial, estruturando o território brasileiro a partir do conceito de **Condados Funcionais**.

---

## O Conceito de Condado Funcional

A divisão estritamente municipal costuma mascarar as reais dinâmicas urbanas e econômicas do Brasil. Na prática, diversos municípios operam de forma integrada a um polo urbano vizinho para suprir necessidades diárias de saúde, educação, mercado de trabalho e serviços públicos.

Para mapear essas interações, o Instituto Brasileiro de Geografia e Estatística (IBGE) estabeleceu a divisão regional por **Regiões Geográficas Imediatas (RGIs)**. No projeto `br-counties`, cada RGI é modelada e analisada como um **Condado Funcional**, permitindo uma leitura mais precisa da organização do espaço e do planejamento regional.

### Hierarquia Territorial Utilizada

* **Região Intermediária (RGInt):** Agrupa múltiplos condados ao redor de metrópoles ou capitais regionais, representando a macroestrutura econômica.
* **Condado (RGI):** Agrupamento funcional de municípios articulados em torno de um centro urbano de referência direta.
* **Município:** A unidade federativa básica de coleta de dados.

---

## Indicadores Consolidados

Nas páginas de cada estado e condado, os seguintes indicadores são apresentados e agregados:

| Indicador | Descrição e Metodologia |
| :--- | :--- |
| **Cód. IBGE** | Identificador único oficial de 7 dígitos atribuído ao município. |
| **População** | Contagem populacional total obtida a partir do Censo Demográfico e estimativas oficiais do IBGE. |
| **Área (km²)** | Extensão territorial oficial da unidade em quilômetros quadrados. |
| **Densidade (hab/km²)** | Razão direta entre a população total e a área territorial (População ÷ Área). |
| **IDHM** | Índice de Desenvolvimento Humano Municipal do PNUD/IPEA. Para o valor consolidado do Condado, é utilizada a média ponderada pela população. |

---

## Como Utilizar os Dados Brutos

Se você precisa dos dados brutos para processamento em GIS, Python, PowerBI ou planilhas, os arquivos padronizados em formato `.csv` estão disponíveis no diretório `data/` do repositório principal:

* [Acessar Repositório do Projeto no GitHub](https://github.com/NexaRift/br-counties)
* [Download do Arquivo PR_Counties.csv](https://raw.githubusercontent.com/NexaRift/br-counties/main/data/PR_Counties.csv)