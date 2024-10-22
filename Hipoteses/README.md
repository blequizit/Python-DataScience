# Análise de Salários de Professores

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
