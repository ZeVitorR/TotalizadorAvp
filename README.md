# Totalizador AVP (Ajuste a Valor Presente)

## 📝 Descrição
A rotina **TOTALIZADORAVP** foi desenvolvida para calcular a posição financeira dos clientes de filiais selecionadas, aplicando regras de Ajuste a Valor Presente (AVP). O sistema processa títulos do Contas a Receber, calcula juros para valores vencidos e descontos para valores a vencer, exportando o resultado final para um arquivo Excel detalhado.

## 🚀 Informações Técnicas
- **Função:** `U_TOTALIZADORAVP` 
- **Namespace:** `FIN` 
- **Autor:** José Vitor Rodrigues 
- **Data de Criação:** 19/05/2025 
- **Linguagem:** TLPP / AdvPL 

## 🛠️ Funcionalidades
- **Seleção de Filiais:** Interface visual (`FWMarkBrowse`) que permite selecionar múltiplas filiais para o processamento.
- **Cálculos Financeiros:**
    - **Títulos Vencidos:** Aplica multa e juros compostos baseados na taxa informada.
    - **Títulos a Vencer:** Aplica cálculo de desconto para trazer o título ao valor presente.
    - **IGPM:** Possibilidade de aplicar alíquota de acréscimo baseada no IGPM.
- **Exportação:** Geração de arquivo `.xlsx` automatizada, organizada por abas para cada filial[cite: 24,.

## 📋 Parâmetros (ParamBox)
Ao executar a rotina, os seguintes parâmetros devem ser preenchidos:
1. **Inclui Despesas (S/N):** Define se o prefixo 'ZZZ' será considerado.
2. **Taxa de Juros (a.m. %):** Taxa mensal para cálculos de atraso.
3. **Taxa de Desconto (a.m. %):** Taxa mensal para antecipação.
4. **Multa:** Percentual de multa sobre títulos vencidos.
5. **Data Base:** Data de referência para o cálculo de dias.
6. **Aliq. IGPM:** Alíquota para correção monetária.

## 🗂️ Tabelas Relacionadas
- **SE1:** Contas a Receber (Principal fonte de dados).
- **SM0:** Cadastro de Filiais (Para seleção no browse).
- **ZA2:** Tabela de suporte para filtragem de filiais autorizadas.
- **Tabela Temporária:** Utilizada para consolidar os dados antes da exportação.

## 📂 Localização do Arquivo Gerado
O relatório é salvo automaticamente no diretório de spool do servidor:
`C:\spool\Totalizador AVP[HHMMSS].xlsx` 
