# Análise de Soja na Bahia


# Funcionalidades dos Scripts
Pipeline de ETL e EDA (a3_xavier_soja_v2.py)
Extração (Extract): Realiza requisições assíncronas HTTP GET à API do SIDRA e ingere arquivos tabulares locais estruturados.

Transformação (Transform): Limpa metadados e cabeçalhos poluídos, aplica expressões regulares (Regex) para conversão de tipos de dados regionais (Type Casting de padrão brasileiro para americano), unifica as bases por chaves temporárias de Inner Join, e resolve problemas de granularidade executando agrupamentos matemáticos (soma anual de chuvas e preço médio anual).

Análise Exploratória (EDA): Executa cálculos descritivos, análise de correlação linear de Pearson e exporta visualizações estatísticas estáticas utilizando matplotlib e seaborn.

# Dashboard Estratégico (app.py)
Interface interativa em Streamlit focada em gestores e stakeholders não tecnológicos.

Painel Dinâmico: Atualização reativa de eixos de gráficos e cartões de métricas (KPIs) com base no filtro temporal do usuário (via slider ou digitação).

Gráficos Combinados (Plotly): Cruzamento em tempo real de colunas de barras (precipitação) e linhas de tendência (preços reais).

Módulo Científico: Integração de matrizes de correlação e tabelas descritivas dinâmicas na mesma interface.

# Como Executar o Projeto

### Pré-requisitos
Certifique-se de possuir o Python instalado em sua máquina e as dependências estruturais do projeto:
```bash
pip install pandas requests streamlit plotly matplotlib seaborn
```

### Passo 1: Executar o Pipeline de Dados (ETL)
Para processar os dados brutos e gerar os arquivos consolidados na pasta `csv/`, execute:
```bash
python a3_xavier_soja_v2.py
```

### Passo 2: Inicializar o Dashboard Interativo
Para abrir o painel executivo e explorar os dados de forma visual através do seu navegador, utilize:
```bash
streamlit run app.py
```

# Respostas ao Negócio & Storytelling
O modelo integrado responde diretamente às hipóteses fundamentais formuladas pelo projeto:

Janela de Comercialização Ideal: O perfil mensal prova a existência de um ciclo sazonal rigoroso. Cooperativas rurais podem adotar táticas de estocagem inteligente em silos durante os meses de pico de oferta e programar as vendas nas janelas de entressafra, maximizando as margens de lucro.

Gatilho Climático: A forte correlação linear identificada valida que volumes de chuva acumulada abaixo do limiar histórico disparam quebras imediatas de produtividade por hectare, servindo como modelo preditivo para acionamento de seguros agrícolas.

Elasticidade Financeira: Em cenários de seca extrema regional, a escassez física de grãos atua como vetor inflacionário sobre a cotação balizada pelo indicador CEPEA.

# Ética, Governança e LGPD
O projeto opera exclusivamente com dados estatísticos e macroeconômicos públicos e governamentais. Não há ingestão, manipulação ou armazenamento de Informações Pessoalmente Identificáveis (PII) de pessoas físicas ou entidades privadas rurais. O pipeline está em total conformidade técnica com as diretrizes da Lei Geral de Proteção de Dados (LGPD).



# Link da apresentação em video :
https://youtu.be/nkhFirfU174


