# Relatório de Avaliação NLU - SAC Móveis Residenciais
## 1. Tabela Comparativa de Métricas (Dados de Teste)

KNN:
        precision    recall  f1-score   support

logistica_entregas       1.00      1.00      1.00         6
       reclamacoes       1.00      1.00      1.00         6
           suporte       1.00      1.00      1.00         6
 trocas_devolucoes       1.00      1.00      1.00         6
            vendas       1.00      1.00      1.00         6

          accuracy                           1.00        30
         macro avg       1.00      1.00      1.00        30
      weighted avg       1.00      1.00      1.00        30

Descreva quais classes se confundiram: 
suporte, logística, reclamações e vendas. Em alguns que deveriam ser 100% deu resultado de 66.67%, e vice versa.
---------------------------- // -----------------------------
Decision Tree:

          precision    recall  f1-score   support

logistica_entregas       0.80      0.67      0.73         6
       reclamacoes       1.00      0.67      0.80         6
           suporte       0.75      1.00      0.86         6
 trocas_devolucoes       0.83      0.83      0.83         6
            vendas       0.71      0.83      0.77         6

          accuracy                           0.80        30
         macro avg       0.82      0.80      0.80        30
      weighted avg       0.82      0.80      0.80        30

Descreva quais classes se confundiram:
suporte, reclamações, trocas, vendas. Foi identificado muitos erros, de frases que não tinham relação com as intenções.

## 2. Análise dos Testes de Entrada (`input()`)
- **Comportamento do KNN (10 testes):** Como o KNN reagiu às variações das frases digitadas e ao fallback?
Reagiu tentou encaixar as frases nas intenções do dataset, frases que não tinham muita relação com nenhuma das categorias, a confiança geralmente ficou em torno de 66%.
  
- **Comportamento da Decision Tree (8 testes):** Como a Árvore de Decisão se comportou em comparação ao KNN?
Péssimo, tentou encaixar todas as frases nas categorias disponíveis, mesmo quando não havia relação com nenhuma delas, e apresentou erros até mesmo em frases que tinham uma intenção claramente definida.

## 3. Veredito Final
- **Melhor modelo para este projeto:** KNN 
- **Justificativa técnica:** Explique a escolha com base nas métricas estatísticas e no comportamento do fallback:
O KNN foi escolhido como o melhor modelo porque apresentou 100% de acurácia, com precision, recall e F1-score de 100% em todas as classes no conjunto de teste. A Decision Tree alcançou apenas 80% de acurácia e apresentou mais erros nas classificações. Apesar de o KNN também ter dificuldade com frases fora do contexto e nem sempre acionar o fallback, seu desempenho geral foi superior ao da Decision Tree.
