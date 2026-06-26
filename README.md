# Dashboard de Custos do Setor de TI

## Sobre o projeto

Um pipeline completo de dados que transforma informações brutas de custos de TI em um dashboard interativo no Power BI, cobrindo despesas com materiais, licenças de software, profissionais e manutenção ao longo de 2024.

## O Pipeline

Arquivo Excel Bruto  →  Script Python  →  Excel Tratado  →  Dashboard Power BI

## Script de Limpeza de Dados

Antes de carregar qualquer coisa no Power BI, os dados passam por um script de tratamento que:

- Carrega o arquivo Excel bruto
- Verifica valores nulos e registros incompletos
- Corrige os tipos de dados — datas como datas, números como números
- Padroniza os campos de texto — remove espaços, corrige capitalização
- Valida os valores financeiros — remove registros negativos
- Remove registros duplicados pelo ID do lançamento
- Exporta um arquivo limpo e pronto para análise
- Exibe um resumo completo no terminal

## Power BI — Dashboard

O dashboard responde quatro perguntas que considerei mais úteis:

| Pergunta | Visual |
|----------|--------|
| Quanto foi gasto no total? | Cartões KPI |
| Como os gastos se distribuem por categoria? | Gráfico de Rosca |
| Como os gastos evoluíram mês a mês? | Gráfico de Barras |
| Qual departamento gasta mais? | Gráfico de Barras |

Medidas criadas com DAX:
- `Total Gasto` — SOMA de todas as transações
- `Total Lançamentos` — CONTAGEM de todos os registros
- `Ticket Médio` — DIVIDE(Total Gasto, Total Lançamentos)

## Tecnologias Utilizadas

| Tecnologia | Uso |
|------------|-----|
| Python | Limpeza e validação dos dados |
| Pandas | Manipulação dos dados |
| openpyxl | Leitura e escrita de arquivos Excel |
| Power BI | Dashboard interativo |
| DAX | Medidas calculadas |

---

## Como executar

Você vai precisar de: Python 3.x e Power BI Desktop instalados.

```bash
# Instalar dependências
pip install pandas openpyxl

# Rodar o script de limpeza
python tratamento_de_dados.py
```

Depois abra o arquivo `Custos TI 2024.pbix` no Power BI Desktop.

---

## O que aprendi

Este projeto conectou conhecimentos de Python, Excel e Power BI em um 
fluxo de trabalho único, reforçando a importância do tratamento de dados 
como etapa anterior à análise, dados não tratados podem distorcer 
completamente os resultados visualizados.

---

## Entre em contato

Se tiver alguma dúvida sobre o projeto ou quiser conversar:

- 💼 [LinkedIn](https://www.linkedin.com/in/stefania-silva-aa84983a5)
- 🐙 [GitHub](https://github.com/Stefaniasgs)
- 📧 stefaniasilva0000@gmail.com
