#Resultado Lab 01:
1 - --- RESULTADOS DO LAB 01 ---
Mensagem: 'Quero consultar quanto dinheiro tenho' ==> Intenção Predita: [fazer_pix]
Mensagem: 'Pode me ajudar a fazer um pix?' ==> Intenção Predita: [fazer_pix]
Mensagem: 'Gostaria de cancelar meu cartão de crédito' ==> Intenção Predita: [cancelar_conta]

2 - Como melhorar o resultado?
Adicionei mais frases ao dataset para o modelo aprender melhor. 
--- RESULTADOS DO LAB 01 ---
Mensagem: 'Quero consultar quanto dinheiro tenho' ==> Intenção Predita: [consultar_saldo]
Mensagem: 'Pode me ajudar a fazer um pix?' ==> Intenção Predita: [fazer_pix]
Mensagem: 'Gostaria de cancelar meu cartão de crédito' ==> Intenção Predita: [cancelar_conta]

3 - Função do LogisticRegression
O LogisticRegression aprende os padrões das frases e tenta identificar a intenção de cada mensagem. O CountVectorizer transforma as palavras em números e o modelo usa esses dados para fazer as classificações.

#comentário: 
Entendi que o resultado depende bastante da quantidade e da qualidade dos exemplos. Como o dataset era pequeno, o modelo acabou errando uma previsão.

#Resultado Lab 02:
1 - --- RESULTADOS DO LAB 02 ---
Mensagem de Teste: 'Gostaria de devolver o produto que comprei'
Intenção Predita: troca_devolucao

--- Distribuição de Probabilidades por Classe ---
Classe [duvida_frete]: 27.99%
Classe [rastrear_pedido]: 24.54%
Classe [troca_devolucao]: 47.46%

2 - Como melhorar o resultado?
Adicionei mais frases ao dataset e usei exemplos mais variados para cada intenção. Isso ajuda o modelo a classificar melhor novas mensagens:
--- RESULTADOS DO LAB 02 ---
Mensagem de Teste: 'Gostaria de devolver o produto que comprei'
Intenção Predita: troca_devolucao

--- Distribuição de Probabilidades por Classe ---
Classe [duvida_frete]: 26.77%
Classe [rastrear_pedido]: 22.11%
Classe [troca_devolucao]: 51.12%


3 - Função do Naive Bayes
O Naive Bayes analisa as palavras da mensagem e calcula a probabilidade de ela pertencer a cada intenção. Como troca_devolucao teve a maior probabilidade, essa foi a classificação escolhida.

#comentário: 
Entendi como o Naive Bayes usa probabilidades para classificar mensagens. O resultado mostrou que o modelo conseguiu identificar corretamente a intenção da frase.

#Resultado Lab 03:
1 - Acurácia do modelo

Acurácia do Modelo: 33.33%

Como o dataset possui apenas 9 exemplos, o conjunto de teste fica muito pequeno. Por isso, um único erro pode alterar bastante a porcentagem e deixar o resultado pouco confiável.

2 - Como a Árvore de Decisão toma a decisão?

A Árvore de Decisão analisa as características das frases e cria divisões para separar as intenções. O CountVectorizer transforma as palavras em números, que são usados pela árvore para fazer a classificação.

3 - Risco de não utilizar max_depth

Sem um limite de profundidade, a árvore pode ficar muito grande e aprender demais os exemplos do treinamento. Isso pode causar overfitting, fazendo o modelo ter dificuldade com frases novas.

#comentário:
Entendi como uma Árvore de Decisão pode classificar mensagens. Também percebi que uma acurácia baixa ou alta pode não representar bem o modelo quando temos poucos dados.

#Resultado Lab 04:
--- RESULTADOS DO LAB 04 ---
Mensagem: 'Gostaria de adquirir um voo para Recife' ==> Intenção Predita: [comprar_passagem]
Mensagem: 'Não quero mais minha reserva' ==> Intenção Predita: [cancelar_reserva]
Mensagem: 'Preciso conversar com alguém da agência' ==> Intenção Predita: [falar_atendente]


Foi utilizado o TfidfVectorizer para transformar as frases em números e o LogisticRegression para classificar as intenções.

Foram adicionadas mais 3 frases sobre atendimento, o que ajudou o modelo a identificar melhor essa intenção.

#comentário:
Consegui criar um classificador de intenções para uma agência de viagens e testar frases novas. O modelo acertou todas as previsões, mostrando que adicionar mais exemplos pode ajudar a melhorar os resultados.
