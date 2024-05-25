# Atividade: Classificação de Imagens (CIFAR-10) - Semana 6 CC Módulo 10

Para executar esse notebook, copie e execute o notebook `app.ipynb` partir do link do Google Colab no topo desse arquivo e siga as instruções abaixo.

Essencialmente, será necessário:

1. Baixar os arquivos `model.py`e `cifar_net.pth` desse repositório;
2. Subir os arquivos baixados para a instância Google Colab que rodará o servidor Flask a partir do arquivo àpp.ipynb`;
3. Criar uma conta no site ngrok.com e obter um token de autenticação;
4. Baixar uma imagem CIFAR-10 de exemplo (disponível nesse [link](https://www.kaggle.com/datasets/swaroopkml/cifar10-pngs-in-folders));
5. Usar seu cliente preferido para realizar uma requisição POST a `<sua_url_ngrok>/predict` com a imagem anexada no corpo do request.

O arquivo de treinamento `train_model.ipynb` não é necessário para a execução da aplicação, mas foi inserido no repositório para demonstrar como o arquivo do modelo foi gerado.
