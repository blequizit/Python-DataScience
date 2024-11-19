# Teste de Hipóteses Estatísticas

Este documento descreve as etapas para realizar um **teste de hipóteses** estatísticas, além de conter um exemplo em **Python**. O objetivo é testar uma suposição sobre um parâmetro populacional com base em dados amostrais.

## Etapas para Realizar um Teste de Hipóteses

### 1. Definir a Hipótese Nula (H₀) e Hipótese Alternativa (H₁)

- **Hipótese Nula (H₀):** A hipótese nula sempre deve expressar uma **igualdade** (ou uma condição de "não diferença"). Exemplos de hipóteses nulas incluem:
  - \( H₀: µ = 0 \) (a média da população é igual a 0),
  - \( H₀: µ ≥ 0 \) (a média da população é maior ou igual a 0),
  - \( H₀: µ ≤ 0 \) (a média da população é menor ou igual a 0).
  
  A hipótese nula representa a situação em que não há efeito, diferença ou mudança.

- **Hipótese Alternativa (H₁):** A hipótese alternativa é o oposto da hipótese nula e expressa o que se deseja testar. Exemplos de hipóteses alternativas incluem:
  - \( H₁: µ ≠ 0 \) (a média da população é diferente de 0),
  - \( H₁: µ > 0 \) (a média da população é maior que 0),
  - \( H₁: µ < 0 \) (a média da população é menor que 0).

### 2. Escolher a Estatística de Interesse

- Dependendo do tipo de variável:
  - **Média:** Para variáveis quantitativas.
  - **Proporção:** Para variáveis qualitativas.

### 3. Definir o Nível de Significância (α)

- O nível de confiança usualmente é **95%**, o que implica um **nível de significância (α)** de **5%** (0,05). Este é o limite que estamos dispostos a aceitar para cometer um erro Tipo I (rejeitar a hipótese nula quando ela é verdadeira).

### 4. Escolher o Tipo de Teste Estatístico

- O tipo de teste depende dos dados e das hipóteses formuladas:
  - **Teste t:** Para comparar médias de duas amostras ou uma amostra com um valor conhecido.
  - **Teste Qui-Quadrado:** Para testar a associação ou independência entre variáveis categóricas.
  - **Teste F:** Usado principalmente na **Análise de Variância (ANOVA)** para comparar médias de mais de duas amostras.
  - **Análise de Correlação:** Para avaliar a relação entre duas variáveis quantitativas.

### 5. Realizar o Cálculo e Obter o Valor-p (p-value)

- Após calcular a estatística de teste, obtém-se o **valor-p**, que representa a probabilidade de observar os dados amostrais (ou algo mais extremo) sob a hipótese nula.

### 6. Decisão

- **Verificar se o valor da estatística de teste está contido ou não na região de rejeição**:
  - Caso o valor da estatística de teste caia na **região de rejeição**, rejeita-se a hipótese nula (H₀).
  - Caso contrário, **não se rejeita a hipótese nula**.

### 7. Conclusão

- Com base na decisão anterior, formulamos a conclusão em termos do problema original. Se rejeitamos a hipótese nula, podemos concluir que há evidências para apoiar a hipótese alternativa.

---

## Exemplo

Suponha que estamos testando se a média de salários de um grupo de funcionários é maior que 5000 reais.

1. **Hipótese Nula (H₀):** A média dos salários é 5000 reais.
   - \( H_0: \mu = 5000 \)
2. **Hipótese Alternativa (H₁):** A média dos salários é maior que 5000 reais.
   - \( H_1: \mu > 5000 \)
3. **Nível de Significância (α):** 5% (0,05).
4. **Teste Estatístico:** Teste t para uma amostra (para comparar a média amostral com um valor conhecido).
5. **Cálculo do Valor-p:** Calculamos o valor-p e, se for menor que 0,05, rejeitamos H₀.
6. **Decisão:** Se o valor da estatística de teste estiver na região de rejeição (por exemplo, maior que o valor crítico para um teste unilateral), rejeitamos H₀.
7. **Conclusão:** Se rejeitarmos a hipótese nula, podemos concluir que há evidências de que a média dos salários é superior a 5000 reais.

---

## Contribuições

Professor Alcides Carlos de Araujo FIAP


# PYTHON - Análise de Salários de Professores

Este repositório contém uma análise de dados sobre os salários de professores de diferentes unidades da USP, usando ferramentas de Data Science com Python. A análise inclui testes de hipóteses para comparar salários entre as unidades e verificar diferenças estatisticamente significativas.

---

## Estrutura do Repositório

- **`Hipoteses_221024.ipynb`**: Jupyter notebook contendo o código para a análise e os testes de hipóteses realizados.
- **`salarios_profs.csv`**: Arquivo de dados com informações sobre os salários dos professores de várias unidades da USP.
- **`README.md`**: Arquivo que você está lendo agora, com informações sobre o projeto.

---

## Dados

O arquivo `salarios_profs.csv` contém as seguintes colunas:

- **NOME**: Nome do professor.
- **UNID_ORGAO**: Unidade de trabalho.
- **DEPTO_SETOR**: Departamento ou setor de trabalho.
- **JORNADA**: Carga horária de trabalho.
- **CATEGORIA**: Tipo de contrato (Celetista, RDIDP, etc.).
- **CLASSE**: Nível de carreira (Superior 1, Superior 2, etc.).
- **REF_MS**: Referência de mérito.
- **FUNCAO**: Função desempenhada.
- **FUNCAO_ESTRUTURA**: Estrutura funcional.
- **TEMPO_USP**: Tempo de serviço na USP (em anos).
- **PARCELAS_EVENTUAIS**: Valor de parcelas eventuais.
- **SALARIO_MENSAL**: Salário bruto mensal.
- **SALARIO_MENSAL_LIQUIDO**: Salário líquido mensal.

### Exemplo de linha do arquivo:

```csv
NOME;UNID_ORGAO;DEPTO_SETOR;JORNADA;CATEGORIA;CLASSE;REF_MS;FUNCAO;FUNCAO_ESTRUTURA;TEMPO_USP;PARCELAS_EVENTUAIS;SALARIO_MENSAL;SALARIO_MENSAL_LIQUIDO
Abel Elias Rahal;PUSP-RP;Seção Técnica de Práticas Esportivas;30 Horas;Celetista;Superior 2;A;Educador Em Praticas Desportivas;;46;18432,97;12967,38;17584,07
```

## Análise de Salários de Professores

---

## Análises Realizadas

O código no arquivo `.ipynb` inclui:

- **Leitura e pré-processamento dos dados**: Os dados são lidos e organizados usando `pandas`.
- **Filtragem por unidade e função**: Filtros são aplicados para selecionar as unidades FEA, ICMC, e IME, além de funções específicas.
- **Testes de Hipóteses**:
    - **Teste 1**: Comparação do salário médio dos professores do IME com um valor hipotético de R$20.000.
    - **Teste 2**: Comparação entre os salários médios do IME e do ICMC para verificar se há diferença significativa entre as duas unidades.

---

### Pré-requisitos

- Python 3.x
- Bibliotecas necessárias:
    ```bash
    pip install numpy pandas scipy
    ```
---

## Contato

Autor: Eduardo Ferreira  
Email: eduds1010@gmail.com

## Agradecimento

Agradecimento ao professor Alcides Carlos de Araújo que auxilou as análises.
