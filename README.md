# Detecção de Faces de Personagens do The Big Bang Theory

Este projeto tem como objetivo detectar rostos dos personagens do *The Big Bang Theory* em imagens utilizando um modelo de aprendizado profundo treinado para identificar esses rostos. Ele utiliza o OpenCV para a detecção preliminar de rostos e um modelo de rede neural convolucional para classificar cada rosto detectado.

## Pré-requisitos

Antes de executar o código, certifique-se de que você tenha os seguintes pacotes instalados:

- **Keras**: Para carregar e usar o modelo de rede neural.
- **OpenCV**: Para realizar a detecção preliminar de rostos.
- **PIL (Pillow)**: Para manipulação de imagens.
- **NumPy**: Para operações de array.
- **Matplotlib**: Para visualização das imagens.
- **Google Colab** (opcional): Para download da imagem processada.

Você pode instalar essas dependências utilizando o seguinte comando:

```bash
pip install keras opencv-python pillow numpy matplotlib
```
## Como Usar

# Prepare os arquivos necessários:

- O arquivo do modelo (keras_model.h5) que contém o modelo de rede neural treinado.
- O arquivo de rótulos (labels.txt) que contém o nome dos personagens.
- A imagem (image1.jpg) na qual você deseja realizar a detecção.

# Execute o código:

-O código irá carregar a imagem fornecida e usar o OpenCV para detectar os rostos presentes nela.
- Para cada rosto detectado, o código utilizará o modelo de rede neural para classificar o rosto e atribuir a ele um rótulo correspondente a um personagem do The Big Bang Theory.
- O código desenhará um retângulo ao redor de cada rosto e exibirá o nome do personagem detectado com a confiança do modelo.

## Resultado:

- A imagem com as caixas de rosto e rótulos será exibida.
- A imagem processada será salva e você poderá fazer o download da imagem com as marcações.

# Estrutura do Código

- custom_load_model: Função que carrega o modelo de rede neural com uma camada customizada (DepthwiseConv2D).
- preprocess_face: Função que redimensiona e normaliza as imagens dos rostos para o formato adequado para o modelo.
- Detecção de Rostos: Utiliza o OpenCV com o classificador Haar Cascade para localizar rostos na imagem.
- Predição: Cada rosto detectado é pré-processado e passado para o modelo de rede neural para obter a classe do personagem e a confiança da previsão.

## Exemplo de Saída

- O código processará a imagem e exibirá um retângulo vermelho ao redor de cada rosto detectado.
- Em cima do retângulo, será exibido o nome do personagem e a confiança da detecção (por exemplo: Sheldon Cooper: 98.5%).

## Como Rodar o Código no Google Colab

- Carregue os arquivos necessários (modelo, rótulos e imagem) no Google Colab.
- Execute o código no ambiente do Google Colab.
- A imagem processada será exibida e você poderá baixá-la clicando no link gerado.

## Considerações Finais

Este código é um exemplo de como integrar detecção de rostos com classificação de imagens utilizando redes neurais.
A precisão da detecção depende de um modelo bem treinado e da qualidade das imagens fornecidas.
Se você deseja melhorar o modelo, pode treinar uma rede neural mais robusta ou utilizar técnicas mais avançadas de detecção de rostos, como MTCNN ou Dlib.

## Licença

Este projeto é licenciado sob a MIT License - veja o LICENSE para mais detalhes.
