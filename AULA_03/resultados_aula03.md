#Resultado Lab 01: 
1 --- RESULTADOS DO LAB 01 (AULA 03) ---
Mensagem: 'Preciso urgente da segunda via da fatura'
Intenção Predita: [segunda_via]
Vocabulário Filtrado (sem stopwords): ['2a', '2a via', 'aberto', 'acordo', 'acordo pagar', 'alterar', 'alterar endereço', 'app', 'atrasada', 'atualizo', 'atualizo dados', 'boleto', 'cadastramento', 'dados', 'dados residenciais', 'débito', 'débito aberto', 'dívida', 'emitir', 'emitir segunda', 'endereço', 'endereço cadastramento', 'fatura', 'fatura atrasada', 'fazer', 'fazer um', 'gostaria', 'gostaria alterar', 'negociar', 'negociar pagamento', 'no', 'no app', 'onde', 'onde atualizo', 'pagamento', 'pagamento dívida', 'pagar', 'pagar débito', 'posso', 'posso emitir', 'residenciais', 'residenciais no', 'segunda', 'segunda via', 'um', 'um acordo', 'via', 'via boleto', 'via fatura']

A remoção das stopwords diminui o vocabulário, tirando palavras comuns que não ajudam muito na classificação. Assim, o modelo foca mais nas palavras importantes.

2 - O que significa ngram_range=(1, 2)?
Significa que o modelo considera palavras sozinhas e também combinações de duas palavras, como segunda, via e segunda via. Isso ajuda a entender melhor as frases.

3 - Como a remoção de palavras genéricas ajuda?
Palavras como "de", "da" e "para" aparecem em várias frases e não ajudam muito. Removê-las faz o modelo focar nas palavras mais importantes.

#comentário: 
Entendi que o pré-processamento ajuda o modelo a trabalhar melhor com os textos. Nesse caso, ele conseguiu identificar corretamente a intenção segunda_via.

#Resultado Lab 02: 
1 - 
--- RESULTADOS DO LAB 02 (AULA 03) ---

--- Relatório de Classificação ---
                     precision    recall  f1-score   support

horario_atendimento       0.50      1.00      0.67         1
        localizacao       0.00      0.00      0.00         1
    troca_devolucao       0.00      0.00      0.00         1

           accuracy                           0.33         3
          macro avg       0.17      0.33      0.22         3
       weighted avg       0.17      0.33      0.22         3

--- Matriz de Confusão ---
[[1 0 0]
 [1 0 0]
 [0 1 0]]
 
O que representam Precision, Recall e F1-Score?
Precision mostra os acertos nas previsões, Recall mostra quantos exemplos o modelo conseguiu identificar e F1-Score combina os dois resultados.

2 - Como interpretar a diagonal principal?
A diagonal mostra as classificações que o modelo acertou. Neste caso, ele acertou apenas uma das três previsões.

3 - Por que a acurácia pode ser enganosa?
Quando existem poucos dados ou classes desbalanceadas, a acurácia sozinha pode não mostrar o desempenho real do modelo. Por isso, também é importante analisar outras métricas.

#comentário: 
Entendi melhor como avaliar um modelo usando métricas e a matriz de confusão. Como o dataset era pequeno, o resultado de 33,33% precisa ser analisado com cuidado.

#Resultado Lab 3: 
1 - Acuracia via Pipeline: 0.00%

A acurácia foi de 0,00%. Isso aconteceu porque o dataset e o conjunto de teste eram muito pequenos e o modelo errou as previsões do teste.

2 - Vantagem do Pipeline
O Pipeline junta as etapas de preparação dos dados e treinamento em um único fluxo, deixando o código mais organizado.

3 - Como o Pipeline evita erros?
Ele garante que o mesmo processo seja aplicado aos dados de treino e teste, evitando diferenças no pré-processamento.

#comentário: 
Entendi que o Pipeline facilita o treinamento e deixa o código mais organizado. O resultado de 0% também mostrou como datasets muito pequenos podem prejudicar a avaliação do modelo.
