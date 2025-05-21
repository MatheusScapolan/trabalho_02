# Análise do Impacto do Imposto sobre Bebidas Açucaradas em Berkeley:

## Sobre o Projeto

Este repositório contém a análise empírica do impacto da implementação de um imposto sobre bebidas açucaradas na cidade de Berkeley, Califórnia, em 2014. O trabalho utiliza o método de diferença-em-diferenças para avaliar os efeitos da política tributária sobre preços e consumo, analisando dados de estabelecimentos comerciais antes e depois da implementação do imposto.

O estudo examina como diferentes tipos de estabelecimentos (supermercados grandes, supermercados pequenos, farmácias e postos de gasolina) responderam à política tributária, quantificando o repasse do imposto aos consumidores e avaliando mudanças nos padrões de consumo.

## Contexto

Em novembro de 2014, Berkeley tornou-se a primeira cidade dos Estados Unidos a implementar um imposto específico sobre bebidas açucaradas, estabelecendo uma tributação de um centavo de dólar por onça fluida (aproximadamente 30 ml) sobre distribuidores de bebidas com açúcar adicionado. Esta política pioneira representa um caso emblemático de utilização de instrumentos fiscais para a promoção de objetivos de saúde pública.

A análise desenvolvida neste trabalho fundamenta-se no arcabouço teórico da economia aplicada, particularmente nas teorias de incidência tributária e na metodologia de diferença-em-diferenças para avaliação de políticas públicas. O objetivo central é avaliar empiricamente duas questões fundamentais:

1. Em que medida os vendedores repassaram o imposto aos consumidores na forma de preços mais elevados?
2. Quais foram os efeitos desse repasse no comportamento de compra e consumo de bebidas açucaradas?

## Estrutura do Repositório

```
├── dados/
│   ├── doing-economics-Dataset Project 3.xlsx     # Conjunto de dados principal
│   └── doing-economics-project-3-2-datafile.xlsx  # Conjunto de dados secundário     
├── print_codigos/    
    ├── passo_1_2                                  # Passo da Instrução
│   ├── passo_3                                    # Passo da Instrução
│   ├── passo_4                                    # Passo da Instrução
│   ├── passo_5                                    # Passo da Instrução
│   └── passo_6                                    # Passo da Instrução
├── resultados/
│   ├── Frequency_Tables.xlsx                      # Tabelas de frequência geradas
│   ├── Mean_Price_Per_Oz_Filtered.xlsx            # Médias condicionais de preço
│   ├── Price_Change_Per_Store_Tax_Status.xlsx     # Mudanças de preço após imposto
│   ├── average_soda_prices_over_time_berkeley_comparison.png   # Gráfico de mudança de preço
│   ├── impact_sugar_tax_calories_volume_berkeley.png           # Gráfico de mudança de preço
│   └── price_change_per_ounce_by_store_type_post_tax.png       # Gráfico de tendência de preços
│                    
├── passos.ipynb                                   # Notebook com código de análise
├── Trabalho Prático 2 - Matheus Henrique Scapolan Silva - NºUSP 15479364.pdf  # Relatório final com análises
└── README.md                                      # Este arquivo
```

## Ferramentas e Dependências

Este projeto utiliza as seguintes ferramentas e bibliotecas:

### Linguagem de Programação
- Python 3.x

### Bibliotecas Principais
- **pandas**: Manipulação e análise de dados estruturados
- **matplotlib**: Visualização de dados e geração de gráficos
- **seaborn**: Visualização estatística avançada
- **numpy**: Computação numérica
- **tabulate**: Formatação de tabelas para exibição

### Ambiente de Desenvolvimento
- Jupyter Notebook: Ambiente interativo para execução de código Python

## Instalação e Configuração

Para executar os códigos deste projeto, siga os passos abaixo:

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/seu-usuario/trabalho_02.git
   cd analise-imposto-berkeley
   ```

2. **Crie um ambiente virtual** (opcional, mas recomendado):
   ```bash
   python -m venv venv
   
   # No Windows
   venv\Scripts\activate
   
   # No macOS/Linux
   source venv/bin/activate
   ```

3. **Instale as dependências**:
   ```bash
   pip install pandas matplotlib seaborn numpy tabulate jupyter openpyxl
   ```

4. **Inicie o Jupyter Notebook**:
   ```bash
   jupyter notebook
   ```

5. **Abra o notebook `passos.ipynb`** no navegador que será automaticamente aberto.

## Executando a Análise

O notebook `passos.ipynb` contém todo o código necessário para reproduzir a análise, organizado em células sequenciais que correspondem aos passos descritos no relatório final. Para executar a análise completa:

1. Certifique-se de que os arquivos de dados estão no diretório correto (conforme referenciado no código).
2. Execute as células do notebook em ordem, usando o botão "Run" ou o atalho Shift+Enter.
3. Os resultados serão exibidos abaixo de cada célula e os arquivos de saída serão salvos nos diretórios especificados.

### Passos da Análise

O notebook está organizado nos seguintes passos:

1. **Passo 1 e 2**: Construção de tabelas de frequência
   - Tabela por tipo de loja e período
   - Tabela por tipo de produto e período
   - Tabela de produtos taxados por tipo de loja e período

2. **Passo 3**: Cálculo de médias condicionais de preço por onça
   - Filtro para períodos específicos (DEC2014 e JUN2015)
   - Cálculo de médias por tipo de loja e status de taxação

3. **Passo 4**: Análise de mudanças de preço após o imposto
   - Cálculo da diferença de preço entre períodos
   - Visualização gráfica das mudanças por tipo de loja e status de taxação

4. **Passo 5**: Análise de grupo de controle alternativo
   - Comparação entre Berkeley e localidades vizinhas
   - Visualização da evolução temporal dos preços
   - Análise de diferença-em-diferenças

5. **Passo 6**: Análise do impacto no consumo
   - Visualização das mudanças percentuais no consumo
   - Comparação entre Berkeley e áreas de controle

## Modificando os Caminhos de Arquivo

Antes de executar o código, você precisará ajustar os caminhos de arquivo para corresponder à sua estrutura de diretórios local. Procure pelas seguintes linhas no notebook e atualize conforme necessário:

```python
# Caminho para encontrar o arquivo Excel
file_path = 'C:/Users/Inteli/Desktop/doing-economics-Dataset Project 3.xlsx'

# Caminhos para salvar os resultados
output_file_path = 'C:/Users/Inteli/Desktop/Frequency_Tables.xlsx'
```

Substitua esses caminhos pelos caminhos absolutos ou relativos correspondentes em seu sistema.

## Resultados e Interpretação

Os principais resultados da análise incluem:

1. **Repasse do Imposto**: Evidência de repasse parcial do imposto aos consumidores, com variação significativa entre tipos de estabelecimento. Supermercados pequenos apresentaram um repasse de aproximadamente 78% do valor do imposto.

2. **Efeito Causal**: A análise de diferença-em-diferenças estima que o imposto causou um aumento de aproximadamente 0,53 centavos por onça nos preços de bebidas açucaradas em Berkeley.

3. **Impacto no Consumo**: Redução estimada de 16,5% nas vendas de bebidas açucaradas, com aumento simultâneo nas vendas de água, sugerindo um padrão de substituição favorável do ponto de vista de saúde pública.

Para uma interpretação detalhada dos resultados, consulte o relatório completo no arquivo `Trabalho Prático 2 - Matheus Henrique Scapolan Silva - NºUSP 15479364`.

## Contribuição

Este projeto foi desenvolvido como parte de um trabalho acadêmico. Contribuições, sugestões e melhorias são bem-vindas através de issues e pull requests.

## Contato

Para questões ou esclarecimentos sobre este projeto, entre em contato através de [matheus18scapolan@usp.br].

## Agradecimentos

- Aos autores dos conjuntos de dados originais utilizados nesta análise (CORECON)
- Ao professor Dr. Pedro Forquesato por ter proposto a atividade
- Aos desenvolvedores das bibliotecas Python que tornaram esta análise possível
- À comunidade acadêmica por fornecer o arcabouço teórico e metodológico para este estudo.