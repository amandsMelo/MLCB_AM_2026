LAB 01: Troca do Algoritmo de Classificação (ML):
Carregando modelo Spacy...
Carregando GloVe...
Dataset carregado com 20 mensagens e 4 intenções.
Formato da matriz X: (20, 50)
Formato do vetor y: (20,)

Árvore de Decisão treinada!
Classes aprendidas pelo modelo:
['2via_boleto_contrato' 'alugar_imovel' 'comprar_imovel'
 'suporte_manutencao']
/tmp/ipykernel_3987/2808976701.py:449: UserWarning: The parameters have been moved from the Blocks constructor to the launch() method in Gradio 6.0: theme. Please pass these parameters to launch() instead.
  with gr.Blocks(
Colab notebook detected. This cell will run indefinitely so that you can see errors and logs. To turn off, set debug=False in launch().
* Running on public URL: https://f16e53bb6189705786.gradio.live

This share link is temporary and will last for up to 1 week (best effort). For free permanent hosting and GPU upgrades, run `gradio deploy` from the terminal in the working directory to deploy to Hugging Face Spaces (https://huggingface.co/spaces)

Keyboard interruption in main thread... closing server.
Killing tunnel 127.0.0.1:7860 <> https://f16e53bb6189705786.gradio.live

LAB 02: Ajuste de Governança e Regra de Fallback Dinâmica
Carregando modelo Spacy...
Carregando GloVe...
Dataset carregado com 20 mensagens e 4 intenções.
Modelo supervisionado treinado!
/tmp/ipykernel_3987/2310488669.py:343: UserWarning: The parameters have been moved from the Blocks constructor to the launch() method in Gradio 6.0: theme. Please pass these parameters to launch() instead.
  with gr.Blocks(
Colab notebook detected. This cell will run indefinitely so that you can see errors and logs. To turn off, set debug=False in launch().
* Running on public URL: https://d36eaa6f0b6ba99b46.gradio.live

This share link is temporary and will last for up to 1 week (best effort). For free permanent hosting and GPU upgrades, run `gradio deploy` from the terminal in the working directory to deploy to Hugging Face Spaces (https://huggingface.co/spaces)
Keyboard interruption in main thread... closing server.
Killing tunnel 127.0.0.1:7860 <> https://d36eaa6f0b6ba99b46.gradio.live

LAB 03: Expansão de Classe (Data Drift & Novas Intenções)
Carregando modelo morfológico Spacy...
Carregando GloVe...
Dataset carregado com 25 mensagens divididas em 5 intenções.

Quantidade de exemplos por intenção:
intencao
comprar_imovel          5
alugar_imovel           5
suporte_manutencao      5
2via_boleto_contrato    5
cancelar_contrato       5
Name: count, dtype: int64

Formato da matriz X: (25, 50)
Formato do vetor y: (25,)

Modelo supervisionado treinado!
Classes aprendidas pelo modelo:
['2via_boleto_contrato' 'alugar_imovel' 'cancelar_contrato'
 'comprar_imovel' 'suporte_manutencao']
