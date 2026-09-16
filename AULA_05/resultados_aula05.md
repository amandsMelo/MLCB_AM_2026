# Exercício 1 — Construção da Esteira de Pré-processamento

Frase original:
Gostaria de saber se vocês estão DEVOLVENDO os valores das mesas compradas!!!

Frase processada:
gostar saber devolver valor meso comprada
============================================================
DIAGNÓSTICO DO PRÉ-PROCESSAMENTO
============================================================

Texto original:
MEU sofá!!! chegou quebrado e quero DEVOLVER!!!

Texto normalizado:
sofá chegar quebrar querer devolver

Quantidade de caracteres:
47

Quantidade de tokens antes:
7

Quantidade de tokens depois:
5

Tokens removidos:
['meu', 'e']

Tokens finais:
['sofá', 'chegar', 'quebrar', 'querer', 'devolver']

#Exercício 2 — Construção da Representação Semântica com FastText + Mean Pooling

Frase original:
quero devolver meu sofá

Frase processada:
querer devolver sofá

Dimensão do vetor:
(50,)
Formato X_treino: (80, 50)
Formato X_teste: (32, 50)
Formato X_ood: (20, 50)

Formato y_treino: (80,)
Formato y_teste: (32,)
Formato y_ood: (20,)

#Exercício 3 — Classificador de Intenções com Fallback

Formato dos dados:
X_treino_vec: (80, 50)
X_teste_vec : (32, 50)
y_treino    : (80,)
y_teste     : (32,)

Regressão Logística treinada com sucesso.

Classes aprendidas pelo modelo:
['logistica_entregas' 'suporte_tecnico' 'trocas_devolucoes'
 'vendas_orcamento']

Previsões realizadas com sucesso.

Primeiras previsões:
['suporte_tecnico' 'logistica_entregas' 'vendas_orcamento'
 'suporte_tecnico' 'logistica_entregas' 'logistica_entregas'
 'vendas_orcamento' 'logistica_entregas' 'logistica_entregas'
 'logistica_entregas']

======================================================================
RELATÓRIO DE CLASSIFICAÇÃO — REGRESSÃO LOGÍSTICA
======================================================================
                    precision    recall  f1-score   support

logistica_entregas       0.64      0.88      0.74         8
   suporte_tecnico       0.88      0.88      0.88         8
 trocas_devolucoes       1.00      0.75      0.86         8
  vendas_orcamento       0.71      0.62      0.67         8

          accuracy                           0.78        32
         macro avg       0.81      0.78      0.78        32
      weighted avg       0.81      0.78      0.78        32

Métricas:
Accuracy : 0.7812
Precision: 0.8064
Recall   : 0.7812
F1-Score : 0.7839


======================================================================
TESTES DO CHATBOT
======================================================================

Mensagem:
quero devolver meu sofá
Resultado:
FALLBACK_HUMANO
Confiança: 25.01%

Mensagem:
como faço para realizar a devolução?
Resultado:
FALLBACK_HUMANO
Confiança: 25.00%

Mensagem:
cadê meu pedido?
Resultado:
FALLBACK_HUMANO
Confiança: 25.01%

Mensagem:
meu pedido nao chego
Resultado:
FALLBACK_HUMANO
Confiança: 25.02%

Mensagem:
qual é a previsão do tempo?
Resultado:
FALLBACK_HUMANO
Confiança: 25.00%

======================================================================
ANÁLISE DA MENSAGEM
======================================================================

Mensagem original:
qual é a previsão do tempo?

Mensagem processada:
previsão tempo

Probabilidades:
logistica_entregas       : 25.00%
suporte_tecnico          : 25.00%
trocas_devolucoes        : 25.00%
vendas_orcamento         : 25.00%

Intenção mais provável:
suporte_tecnico

Confiança:
25.00%

Limiar utilizado:
50.00%

Decisão final:
FALLBACK_HUMANO

======================================================================
TESTES ADICIONAIS
======================================================================

Mensagem: quero trocar meu sofá
Resultado: FALLBACK_HUMANO
Confiança: 25.00%
----------------------------------------------------------------------

Mensagem: onde está minha mesa?
Resultado: FALLBACK_HUMANO
Confiança: 25.00%
----------------------------------------------------------------------

Mensagem: preciso do manual do rack
Resultado: FALLBACK_HUMANO
Confiança: 25.00%
----------------------------------------------------------------------

Mensagem: quanto custa uma poltrona?
Resultado: FALLBACK_HUMANO
Confiança: 25.00%
----------------------------------------------------------------------

Mensagem: qual é a capital da França?
Resultado: FALLBACK_HUMANO
Confiança: 25.00%
----------------------------------------------------------------------

Mensagem: me ensine a fazer bolo
Resultado: FALLBACK_HUMANO
Confiança: 25.00%
----------------------------------------------------------------------

Mensagem: qual será o clima amanhã?
Resultado: FALLBACK_HUMANO
Confiança: 25.00%
----------------------------------------------------------------------

Mensagem: quero acompanhar meu pedido
Resultado: FALLBACK_HUMANO
Confiança: 25.01%
----------------------------------------------------------------------

======================================================================
AVALIAÇÃO OOD / FALLBACK
======================================================================

Total de mensagens OOD: 20
Total encaminhado para fallback: 20
Total classificado automaticamente: 0
Taxa de fallback: 100.00%

Resultados individuais:
mensagem	resultado	confianca
0	Qual é a previsão do tempo para amanhã?	FALLBACK_HUMANO	0.250051
1	Quero aprender a tocar violão	FALLBACK_HUMANO	0.250005
2	Me explique como funciona Bitcoin	FALLBACK_HUMANO	0.250040
3	Quem ganhou o campeonato brasileiro?	FALLBACK_HUMANO	0.250035
4	Qual será o clima no final de semana?	FALLBACK_HUMANO	0.250043
5	Quais filmes estão passando hoje?	FALLBACK_HUMANO	0.250048
6	Qual é a melhor linguagem de programação?	FALLBACK_HUMANO	0.250028
7	Me ensine a fazer um bolo de chocolate	FALLBACK_HUMANO	0.250011
8	Como faço uma receita de lasanha?	FALLBACK_HUMANO	0.250012
9	Qual é o melhor celular atualmente?	FALLBACK_HUMANO	0.250015
10	Quero reservar uma passagem aérea	FALLBACK_HUMANO	0.250007
11	Qual é o valor do dólar hoje?	FALLBACK_HUMANO	0.250043
12	Me conte uma piada	FALLBACK_HUMANO	0.250040
13	Qual será o resultado do próximo jogo?	FALLBACK_HUMANO	0.250039
14	Qual é a capital da França?	FALLBACK_HUMANO	0.250031
15	Quem inventou a internet?	FALLBACK_HUMANO	0.250021
16	Como faço para declarar meu imposto de renda?	FALLBACK_HUMANO	0.250012
17	Como aprender inglês rapidamente?	FALLBACK_HUMANO	0.250026
18	Qual restaurante você recomenda?	FALLBACK_HUMANO	0.250012
19	Preciso marcar uma consulta médica	FALLBACK_HUMANO	0.250037

#Exercício 4 — Laboratório Comparativo: Regressão Logística × KNN

Modelos treinados com sucesso.
RELATÓRIO — KNN
                    precision    recall  f1-score   support

logistica_entregas       0.67      0.75      0.71         8
   suporte_tecnico       0.75      0.75      0.75         8
 trocas_devolucoes       0.78      0.88      0.82         8
  vendas_orcamento       0.67      0.50      0.57         8

          accuracy                           0.72        32
         macro avg       0.72      0.72      0.71        32
      weighted avg       0.72      0.72      0.71        32

======================================================================
COMPARAÇÃO — REGRESSÃO LOGÍSTICA × KNN
======================================================================
                Modelo Accuracy Precision  Recall      F1
0  Regressão Logística   78.12%    80.64%  78.12%  78.39%
1                  KNN   71.88%    71.53%  71.88%  71.27%



Questão 1 — Qual modelo apresentou melhor desempenho?
A Regressão Logística apresentou métricas superiores às do KNN, com 78,12% de Accuracy e 78,39% de F1-Score.

Questão 2 — Por que os resultados podem ser diferentes mesmo utilizando os mesmos embeddings?
Os resultados podem ser diferentes porque cada algoritmo analisa os mesmos vetores de uma maneira diferente.

Questão 3 — O KNN utiliza distância. Por que a qualidade dos embeddings é particularmente importante para esse algoritmo?
Porque o KNN utiliza a distância entre os vetores para realizar a classificação. Embeddings bem representados permitem identificar melhor a semelhança entre as mensagens.

Questão 4 — Se o sistema tivesse 100 mil mensagens e centenas de intenções, você escolheria KNN? Justifique.
Não. Com muitas mensagens e intenções, o KNN pode apresentar maior custo computacional e aumentar o tempo necessário para realizar as classificações.

Questão 5 — Qual modelo você escolheria para colocar em produção neste cenário?
Para este cenário, a Regressão Logística seria escolhida, pois apresentou melhores resultados nas métricas avaliadas e possui boa eficiência para classificação de mensagens.



