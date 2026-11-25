# Inferência causal com DiD - Efeitos do Programa de Sustentação do Investimento (PSI) sobre o mercado de trabalho formal: uma abordagem de diferença em diferenças por intensidade de exposição

O projeto é um estudo piloto para a avaliação acadêmica utilizando o metódo de diferenças em diferenças da econometria aplicada pautando-se da busca de inferência causal do estudo, o desenho do estudo detém um tratamento contínuo para estudar como o emprego formal e a massa salarial real evoluíram após o Programa de Sustentação do Investimento (PSI/2009) conforme a exposição histórica dos municípios ao Finame. Os estudos de eventos, os testes de pré-tendências e as análises de robustez documentam os limites da interpretação causal.

## Notebooks

1. [Montagem do painel municipal](objetivos/1.painel/Script_PSI_Painel.ipynb)
2. [Construção da exposição pré-PSI](objetivos/2.pr%C3%A9-exposi%C3%A7%C3%A3o/Script_PSI_Pr%C3%A9_exposicao.ipynb)
3. [Diagnóstico de tendências paralelas](objetivos/3.tendencias_paralelas/Script_PSI_tendencias_paralelas.ipynb)
4. [Regressão DiD (tendências paralelas e estudo de evento), robustez e tabelas](objetivos/4.regression_did/Script_PSI_did.ipynb)

Para reproduzir os resultados do artigo, **abra o quarto notebook**. Ele lê as bases originais e monta o painel e a exposição antes de estimar os modelos. Os três primeiros documentam etapas do estudo e também podem ser executados separadamente.

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


Por fim, esse estudo é um piloto-base para futuros estudos mais robustos e fundamentados. Ele serve apenas como pontapé, pois buscará se adequar as críticas dos pares (acadêmicos, entusiastas de econometria e de linguagens de programação) e melhorarando a contextualização em cima do metódo causal usado e do diagnóstico inferindo no texto do artigo realizado. Nada até a última atualização dessa página foi publicado numa revista acadêmica, logo a validade pode (e deve ser questionada).

## Att.

**Alexandre Albuquerque**

* [Meu LinkedIn](https://www.linkedin.com/in/alexandre-albuquerque-1814852a7/)
* [Meu GitHub](https://github.com/alexandre-albuquerque17?tab=repositories)
* [Gmail](alexandre00012317@gmail.com)
* [Contato] (82 9 9366-1560)


