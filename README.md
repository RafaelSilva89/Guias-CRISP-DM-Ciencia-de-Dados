# 🧭 Guias CRISP-DM para projetos de Ciência de Dados

Guias passo a passo e estruturas prontas para projetos de Ciência de Dados, no roteiro **CRISP-DM** usado em todos os projetos do meu portfólio. Há um par de arquivos para cada tipo de problema:

- **Guia:** explica cada etapa em linguagem simples, com exemplos numéricos, figuras, checklists, erros comuns e um glossário. Serve para tirar dúvidas.
- **Estrutura:** só os títulos do roteiro, com as adaptações do tipo de problema. Serve para começar um projeto novo.

| Tipo de problema | Guia | Estrutura | Exemplos no portfólio |
|---|---|---|---|
| 🎯 Classificação | [Guia_Classificacao](Guia_Classificacao.ipynb) | [Estrutura_Classificacao](Estrutura_Classificacao.ipynb) | Sentimento, Fraudes, Rotatividade |
| 📈 Regressão (incluindo a temporal) | [Guia_Regressao](Guia_Regressao.ipynb) | [Estrutura_Regressao](Estrutura_Regressao.ipynb) | Eleição 2020, Aluguel, Rossmann |
| 🧩 Clusterização | [Guia_Clusterizacao](Guia_Clusterizacao.ipynb) | [Estrutura_Clusterizacao](Estrutura_Clusterizacao.ipynb) | Segmentação de clientes, Segmentação do cartão |
| 📚 Recomendação | [Guia_Recomendacao](Guia_Recomendacao.ipynb) | [Estrutura_Recomendacao](Estrutura_Recomendacao.ipynb) | Sistema de Recomendação de Livros |
| 📊 Análise sem modelo | [Guia_Sem_modelo](Guia_Sem_modelo.ipynb) | [Estrutura_Sem_modelo](Estrutura_Sem_modelo.ipynb) | Carteira de Ações, Risco das Ações |
| 🧪 Teste A/B (A/B, A/B/n, Bayesiano e MAB) | [Guia_Teste_AB](Guia_Teste_AB.ipynb) | [Estrutura_Teste_AB](Estrutura_Teste_AB.ipynb) | Segmentação de clientes (Teste A-B da campanha) |

## 🗺️ O roteiro

```
FASE 01: ENTENDIMENTO DO NEGÓCIO   contexto, objetivo, formato da solução, planejamento
FASE 02: PREPARAÇÃO DOS DADOS      coleta, limpeza, vazamento, EDA com testes estatísticos,
                                   feature engineering, correlações
FASE 03: MODELAGEM DOS DADOS       transformação, separação, algoritmos, validação cruzada,
                                   comparação, ajuste fino (Grid, Random e Bayesiana),
                                   limiar, teste anti-vazamento
FASE 04: AVALIAÇÃO                 desempenho, previsto x observado, variáveis importantes (SHAP)
FASE 05: IMPLANTAÇÃO               modelo salvo, simulação, monitoramento
Resposta à pergunta de negócio, insights, limites, próximos passos e app Streamlit
```

## 🧠 O que os guias explicam

- **Estatística descritiva:** média, mediana, moda, desvio, quartis, assimetria, curtose, como ler um histograma e um boxplot.
- **Outliers** pela regra do IQR.
- **Testes estatísticos:** H0, p-valor, erros tipo I e II, tamanho do efeito e qual teste usar (qui-quadrado, Mann-Whitney, Kruskal-Wallis, Spearman, Wilcoxon, binomial, odds ratio).
- **Vazamento de dados** e Pipeline.
- **Escalas e encoders.**
- **Separação treino/validação/teste e validação cruzada** (K-Fold, Stratified K-Fold, Leave-One-Out, Repeated K-Fold) e **backtest walk-forward** (janela crescente e fixa).
- **Ensembles:** bagging, boosting e stacking.
- **Ajuste fino de hiperparâmetros:** Grid Search, Random Search e otimização Bayesiana (Optuna, pruning, early stopping), hiperparâmetros por algoritmo, boas práticas e qual método usar.
- **Métricas:**
  - classificação: matriz de confusão, precisão, recall, F1, ROC e PR, limiar, curva de custo, calibração;
  - regressão: MAE, MSE, RMSE, MAPE, MPE, R², faixa de erro;
  - clusterização: silhouette, cotovelo, ARI, margem de atribuição;
  - recomendação: acerto@N, NDCG, cobertura.
- **Interpretabilidade com SHAP** (classificação e regressão; na clusterização, por um classificador substituto): valores de Shapley e suas propriedades, explainers, force plot, waterfall, beeswarm, dependence, SHAP × LIME, comunicação por público e auditoria de viés.
- **Monitoramento em produção:** data drift e concept drift, PSI, teste K-S, SLA, estratégias de retreino, teste A/B, shadow mode, canary e o ciclo de MLOps (classificação e regressão); tamanho e estabilidade dos segmentos com reetiquetagem (clusterização); métricas online, cobertura, cold start e ciclo de realimentação (recomendação); acompanhamento dos indicadores com janela móvel e mudança de regime (análise sem modelo).

- **Teste A/B** (guia próprio, com os 5 passos do curso de Teste A/B): hipóteses uni e bicaudais, nível de confiança, α, poder e erros tipo I e II, tamanho do efeito (d, Glass, Hedges, h e w de Cohen), tamanho da amostra, sorteio e SRM, o mapa de escolha do teste estatístico (Z, qui-quadrado, Fisher, t, Welch, Mann-Whitney, Wilcoxon, ANOVA, Kruskal-Wallis) com 10 exercícios, erro α acumulado e correções (Bonferroni, Šidák, FDR, Tukey, Dunn), o perigo de "espiar" o p-valor, Bayesiano (Beta, P(B > A), perda esperada e regra de parada), Multi-Armed Bandit (Aleatório, Onisciente, Guloso, ε-Guloso, UCB e Thompson), **como escolher o método ideal** e o teste em produção (bandit com grupo de controle).

As figuras ficam em [`imagens/`](imagens/), em SVG (as do Teste A/B começam com `ab_`).

## 📁 Versões anteriores

`Modelo_1.ipynb` (guia com notas, 2023) e `Modelo_2.ipynb` (estrutura, 2023) são as versões originais, mantidas para mostrar a evolução. Os guias novos corrigem algumas explicações delas: assimetria, nomes das escalas, Boruta, p-valor e busca de hiperparâmetros.

---

Autor: **Rafael R. Silva** · [github.com/RafaelSilva89](https://github.com/RafaelSilva89)
