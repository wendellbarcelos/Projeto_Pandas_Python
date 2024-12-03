# Projeto de Análise e Enriquecimento de Dados Imobiliários

Fui contratado como **Cientista de Dados** por uma empresa do setor imobiliário. Meu papel é dar suporte tanto ao **time de Machine Learning (ML)** quanto ao **time de Desenvolvimento**, atendendo às demandas específicas de ambos os grupos. O objetivo principal do projeto é transformar os dados disponíveis em informações valiosas, auxiliando no desenvolvimento de um modelo de precificação de imóveis e em funcionalidades para o site da empresa.

A base de dados utilizada contém informações detalhadas sobre diferentes tipos de imóveis no Rio de Janeiro, incluindo apartamentos, casas e estabelecimentos comerciais. Nela, estão presentes os valores de aluguel, condomínio, IPTU e características como número de quartos, suítes, vagas de garagem, entre outros.


## Etapas do Projeto

### 1. **Preparação Inicial**
Iniciamos o projeto importando e explorando a base de dados. As principais ações incluem:
- Verificar o tamanho da base (número de linhas e colunas);
- Identificar as colunas existentes e seus tipos de dados;
- Analisar a estrutura dos dados para identificar valores inconsistentes ou nulos.

Esse processo inicial faz parte da **Análise Exploratória de Dados (EDA)**, onde buscamos:
- Compreender a natureza dos dados (qualitativos ou quantitativos);
- Identificar padrões, valores faltantes e outliers;
- Formular perguntas para direcionar a análise.

### 2. **Questões Investigativas**
Durante o EDA, levantamos perguntas-chave que ajudam a estruturar nossa análise:
1. Quais os valores médios de aluguel por tipo de imóvel?
2. Qual o percentual de cada tipo de imóvel na base de dados?

Essas perguntas nos guiarão na identificação de tendências e na segmentação de dados, apoiando diretamente o trabalho do time de ML.

### 3. **Tratamento de Dados**
O time de ML utilizará os dados para treinar modelos de precificação. Portanto, realizaremos as seguintes ações:
- **Remoção de Dados Inconsistentes**: 
  - Registros com valores de aluguel ou condomínio iguais a 0 serão eliminados.
- **Tratamento de Dados Nulos**:
  - Dados ausentes serão tratados ou removidos, conforme apropriado.

Adicionalmente, aplicaremos filtros para atender a demandas específicas do time de ML:
- Imóveis com **1 quarto** e aluguel inferior a **R$ 1200**.
- Imóveis com **pelo menos 2 quartos**, aluguel inferior a **R$ 3000** e área maior que **70 m²**.

### 4. **Criação de Novas Colunas**
Atendendo ao time de Desenvolvimento, adicionaremos as seguintes colunas à base de dados:

#### **Colunas Numéricas**
1. **`valor_por_mes`**: Soma dos gastos mensais do imóvel, incluindo aluguel e condomínio.
2. **`valor_por_ano`**: Cálculo anual dos gastos com aluguel, condomínio e IPTU.

#### **Colunas Categóricas**
1. **`descricao`**: Uma descrição sumarizada do imóvel, incluindo:
   - Tipo de imóvel;
   - Bairro;
   - Quantidade de quartos;
   - Quantidade de vagas de garagem.
2. **`possui_suite`**: Indicação binária informando se o imóvel possui ou não suítes.


## Objetivos do Projeto

### **Suporte ao Time de Machine Learning**
- Garantir a qualidade e consistência dos dados para o treinamento de modelos de precificação de imóveis.
- Fornecer segmentações específicas para cenários desejados, como imóveis de 1 quarto com aluguel acessível ou de alto padrão com múltiplos quartos e grande área.

### **Apoio ao Time de Desenvolvimento**
- Enriquecer a base de dados com informações resumidas e categorizadas.
- Facilitar a apresentação de dados no site, criando colunas que agreguem valor ao usuário final.


## Ferramentas e Tecnologias
- **Python**: Para manipulação e tratamento de dados, com bibliotecas como Pandas e NumPy.
- **Pandas**: Principal ferramenta para EDA e criação de novas colunas.
- **Jupyter Notebooks**: Documentação e análise interativa dos dados.


## Resultados Esperados
Ao final do projeto, entregaremos:
1. Uma base de dados limpa, enriquecida e pronta para uso pelos times de ML e Desenvolvimento.
2. Insights acionáveis sobre o mercado imobiliário do Rio de Janeiro, incluindo:
   - Segmentação de imóveis por características relevantes;
   - Informações financeiras consolidadas.
3. Colunas adicionais para atender às demandas específicas do site.

Com essas entregas, esperamos potencializar o impacto dos dados na estratégia de negócio da empresa, criando soluções que melhorem tanto o modelo de precificação quanto a experiência do usuário final no site.