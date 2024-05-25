# Atividade: Classificação de Imagens (CIFAR-10) - Semana 6 CC Módulo 10

# Instruções de Execução

Para executar esse notebook, copie e execute o notebook `app.ipynb` partir do link do Google Colab no topo desse arquivo e siga as instruções abaixo.

Essencialmente, será necessário:

1. Baixar os arquivos `model.py`e `cifar_net.pth` desse repositório;
2. Subir os arquivos baixados para a instância Google Colab que rodará o servidor Flask a partir do arquivo àpp.ipynb`;
3. Criar uma conta no site ngrok.com e obter um token de autenticação;
4. Baixar uma imagem CIFAR-10 de exemplo (disponível nesse [link](https://www.kaggle.com/datasets/swaroopkml/cifar10-pngs-in-folders));
5. Usar seu cliente preferido para realizar uma requisição POST a `<sua_url_ngrok>/predict` com a imagem anexada no corpo do request.

O arquivo de treinamento `train_model.ipynb` não é necessário para a execução da aplicação, mas foi inserido no repositório para demonstrar como o arquivo do modelo foi gerado, com as otimizações descritas no relatório a seguir.

# Relatório de Implementação do Modelo de Visão Computacional

## Introdução

Este relatório documenta a implementação de um modelo de visão computacional baseado em CNN para classificação de imagens da base CIFAR-10. A API desenvolvida recebe uma imagem e retorna a categoria inferida pelo modelo.

## Técnicas de Otimização

- **Data Augmentation:** Utilização de transformações aleatórias nas imagens de treinamento.
- **Dropout:** Aplicado para prevenir overfitting.
- **Regularização L2:** Adicionada para reduzir a complexidade do modelo.
- **Early Stopping:** Implementado para interromper o treinamento antes que o overfitting ocorra.

## Resultados dos Testes

### Caso 1
- Imagem: `test/cat/0001.png`
- Categoria Inferida: `cat`

### Caso 2
- Imagem: `test/truck/0012.png`
- Categoria Inferida: `automobile`

### Caso 3
- Imagem: `test/automobile/0005.png`
- Categoria Inferida: `Carro`

## Conclusão

A implementação foi bem-sucedida, e o modelo apresentou boas capacidades de generalização, apesar de alguns erros durante a inferência com as imagens de teste (por exemplo, previsão de carro ao invés de caminhão no Caso 2).
