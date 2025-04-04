# 📊 Projeto de Análise de Rentabilidade de Clientes

Este projeto tem como objetivo analisar uma base de dados financeira de clientes, com foco em indicadores como **margem operacional**, **carga tributária proporcional** e **rentabilidade líquida**.

## 📁 Arquivo de entrada

- `Base de Dados - PSel Analista de Dados.xlsx`
  - **Aba:** `Base de Dados`
  - **Colunas Originais:**
    - Cliente
    - Faturamento Mensal (R$)
    - Custo Operacional (R$)
    - Impostos Pagos (R$)

## 🧪 Etapas da Análise

1. **Limpeza dos dados financeiros**
   - Conversão de strings monetárias para float (`R$`, pontos e vírgulas removidos).

2. **Cálculo de Métricas**
   - `lucro_operacional = faturamento - custo_operacional`
   - `lucro_liquido = lucro_operacional - impostos`
   - `margem_operacional = (lucro_operacional / faturamento) * 100`
   - `carga_tributaria = (impostos / faturamento) * 100`
   - `rentabilidade = (lucro_liquido / faturamento) * 100`

3. **Geração de Rankings**
   - Top 5 clientes por maior margem operacional.
   - Top 5 clientes que mais pagam impostos proporcionalmente.
   - Ranking completo dos clientes mais rentáveis.

## 📅 Sugestão de Rotina Mensal

- Importação e validação automática dos dados.
  
- Recalcular os indicadores e identificar:
  - Clientes em prejuízo.
  - Clientes com impostos excessivos.
  - Clientes mais lucrativos.
    
- Geração de relatórios automáticos (Excel/PDF).
  
- Opcional: criação de dashboards interativos com Streamlit ou Power BI.

## 🛠 Tecnologias utilizadas

- Python 3
- Pandas
- OpenPyXL (para leitura de arquivos Excel)

## 📂 Como executar

1. Instale as bibliotecas necessárias:
   ```bash
   pip install pandas openpyxl
