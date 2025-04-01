# AgentAI-RealEstate-Consulting

## Sobre o Projeto

Este projeto implementa um sistema de consultoria imobiliária completa utilizando agentes de IA com CrewAI. O sistema simula uma equipe de profissionais do setor imobiliário que trabalham em conjunto para fornecer recomendações personalizadas de imóveis, análises de mercado, informações sobre financiamento e relatórios detalhados.

## Funcionalidades

- Busca de imóveis baseada nas preferências do cliente
- Análise de tendências de preços em diferentes regiões
- Monitoramento de notícias relevantes do mercado imobiliário
- Simulação de opções de financiamento
- Geração de relatórios detalhados e personalizados

## Estrutura do Sistema

O sistema é composto por cinco agentes especializados que trabalham em conjunto:

### 1. Corretor de Imóveis

- **Descrição:** Obtém as preferências do cliente e busca imóveis compatíveis no banco de dados.
- **Objetivo:** Encontrar as melhores opções de imóveis com base nas preferências do cliente.
- **Ferramenta:** `CSVSearchTool` para consultar a base de dados de imóveis (arquivo CSV).

### 2. Analista de Mercado Imobiliário

- **Descrição:** Analisa as tendências de preços em diferentes cidades e prevê valorização ou desvalorização.
- **Objetivo:** Fornecer insights sobre o potencial de valorização dos imóveis selecionados.
- **Ferramenta:** `TendenciaPrecosImoveisTool` para analisar tendências de preços por cidade.

### 3. Analista de Notícias Imobiliárias

- **Descrição:** Busca e analisa notícias recentes sobre o mercado imobiliário.
- **Objetivo:** Identificar fatores externos que podem impactar os preços dos imóveis.
- **Ferramenta:** `DuckDuckGoSearchResults` para buscar notícias relevantes.

### 4. Consultor Financeiro

- **Descrição:** Analisa o perfil financeiro do cliente e sugere opções de financiamento.
- **Objetivo:** Recomendar as melhores condições de financiamento disponíveis.
- **Ferramenta:** Utiliza conhecimento especializado para realizar simulações.

### 5. Redator de Relatórios

- **Descrição:** Integra todas as informações e gera relatórios detalhados.
- **Objetivo:** Criar um documento final completo e persuasivo para o cliente.
- **Ferramenta:** Integra dados dos outros agentes para produzir o relatório.

## Fluxo de Trabalho

1. O cliente fornece suas preferências (tipo de imóvel, localização, faixa de preço)
2. O Corretor de Imóveis busca opções compatíveis no banco de dados
3. O Analista de Mercado avalia as tendências de preços na região selecionada
4. O Analista de Notícias busca informações relevantes sobre o mercado
5. O Consultor Financeiro simula opções de financiamento
6. O Redator de Relatórios compila todas as informações em um documento final

## Requisitos

- Python 3.8+
- CrewAI
- LangChain
- OpenAI API Key

## Instalação

```bash
# Clone o repositório
git clone https://github.com/ericklyl/AgentAI-RealEstate-Consulting.git
cd AgentAI-RealEstate-Consulting/CrewAI_imobiliaria

# Instale as dependências
pip install -r requirements.txt

# Configure sua API key da OpenAI
# Crie um arquivo .env com o seguinte conteúdo:
# OPENAI_API_KEY=sua_chave_api_aqui
```

## Uso

1. Execute o script para gerar dados simulados de imóveis:
```bash
python imoveis.py
```

2. Execute o notebook Jupyter ou script principal:
```bash
jupyter notebook recomendacao_imoveis.ipynb
# ou
python recomendacao_imoveis.py
```

3. Insira os parâmetros de busca (cidade, tipo de imóvel, faixa de preço)

4. Aguarde enquanto os agentes realizam suas análises

5. Receba o relatório final com as recomendações personalizadas

## Tecnologias Utilizadas

- **CrewAI**: Framework para orquestração de múltiplos agentes de IA
- **LangChain**: Framework para desenvolvimento de aplicações baseadas em LLMs
- **OpenAI**: Modelos de linguagem para processamento de linguagem natural
- **ChromaDB**: Banco de dados vetorial para busca semântica

## Estrutura do Projeto

```
CrewAI_imobiliaria/
├── files/
│   └── imoveis.csv           # Banco de dados de imóveis
├── imoveis.py                # Script para geração de dados simulados
├── recomendacao_imoveis.ipynb  # Notebook principal
├── requirements.txt          # Dependências do projeto
└── README.md                 # Este arquivo
```

## Contribuição

Contribuições são bem-vindas! Por favor, sinta-se à vontade para abrir issues ou enviar pull requests.

## Licença

Este projeto está licenciado sob a licença MIT - veja o arquivo LICENSE para detalhes.

## Contato

- GitHub: [ericklyl](https://github.com/ericklyl)
