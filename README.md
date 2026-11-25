# Exposição ao Finame e resultados do PSI

O projeto usa diferenças em diferenças com tratamento contínuo para estudar como o emprego formal e a massa salarial real evoluíram após o PSI conforme a exposição histórica dos municípios ao Finame. Os estudos de eventos, os testes de pré-tendências e as análises de robustez documentam os limites da interpretação causal.

## Notebooks

1. [Montagem do painel municipal](objetivos/1.painel/Script_PSI_Painel.ipynb)
2. [Construção da exposição pré-PSI](objetivos/2.pr%C3%A9-exposi%C3%A7%C3%A3o/Script_PSI_Pr%C3%A9_exposicao.ipynb)
3. [Diagnóstico de tendências paralelas](objetivos/3.tendencias_paralelas/Script_PSI_tendencias_paralelas.ipynb)
4. [Regressões, robustez e tabelas do artigo](objetivos/4.regression_did/Script_PSI_did.ipynb)

Para reproduzir os resultados do artigo, abra o quarto notebook. Ele lê as bases originais e monta o painel e a exposição antes de estimar os modelos. Os três primeiros documentam etapas do estudo e também podem ser executados separadamente.

## Ambiente

Em um terminal na raiz do clone, usando Python 3.13:

```powershell
python -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
```

No VS Code, abra a pasta do repositório e escolha o Python de `.venv` como kernel do notebook. Execute as células de cima para baixo. Os caminhos são relativos à raiz do projeto e funcionam com o kernel iniciado na raiz ou na pasta do notebook.

## Bases de entrada

O notebook final lê os arquivos abaixo na pasta `dados_base's/`, mantendo os nomes e as abas originais.

| Arquivo | Aba |
| --- | --- |
| `desembolsos-mensais_Finame.xlsx` | `sheet_1` |
| `desembolsos-mensais_PSI.xlsx` | `desembolsos-mensais_PSI` |
| `IBGE_pop_municipios.xlsx` | `IBGE_pop_municipios` |
| `IPCA_STP-20261019203512642.xlsx` | `IPCA` |
| `PIB dos Municípios - base de dados 2002-2009.xlsx` | `PIB_dos_Municípios` |
| `PIB dos Municípios - base de dados 2010-2023.xlsx` | `PIB dos Municípios` |
| `rais_empr_remuner_2000_2014.xlsx` | `RAIS` |

Para o primeiro notebook, mantenha também a base de estimativas de população de 2026 em `dados_base's/Originais/IBGE_pop_estimativa_dou_2026.xlsx` (aba `sheet_1`).

O notebook de regressão contém as tabelas e os gráficos do artigo. A seção **Exportação das tabelas de regressão** recria as imagens em PNG, o ZIP e a planilha Excel em `outputs/tabelas_psi/`. O notebook de montagem do painel grava sua planilha em `outputs/painel/`.
