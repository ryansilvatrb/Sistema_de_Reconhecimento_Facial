# 🧑‍💻 Projeto de Reconhecimento Facial — Big Bang Theory

Este projeto implementa um sistema simples de reconhecimento facial supervisionado usando Python, TensorFlow/Keras e OpenCV. Foram utilizadas imagens de personagens da série The Big Bang Theory (Sheldon, Penny, Leonard, Raj, Amy e Bernadette), organizadas em pastas de dataset, para treinar uma rede neural convolucional (CNN) capaz de identificar cada pessoa.  

## 📂 Estrutura do Projeto
dataset/  
│── Sheldon/  
│    ├── img1.jpg  
│    ├── img2.jpg  
│── Penny/  
│    ├── img1.jpg  
│    ├── img2.jpg  
│── Leonard/  
│── Raj/  
│── Amy/  
│── Bernadette/  

Cada pasta representa uma classe (personagem). Dentro de cada pasta, devem estar as imagens de treino.  

## 🚀 Tecnologias Utilizadas
- Python 3.12+  
- TensorFlow / Keras → rede neural convolucional (CNN)  
- OpenCV → detecção de rostos  
- NumPy / Scikit-learn → manipulação dos dados  

## ⚙️ Como Funciona
1. Pré-processamento: As imagens são convertidas para tons de cinza, redimensionadas para 100x100 pixels e normalizadas entre 0 e 1.  
2. Treinamento do Modelo: É usada uma CNN com duas camadas de convolução e pooling, classificando em 6 classes (personagens).  
3. Detecção Facial: Um classificador HaarCascade do OpenCV localiza rostos em novas imagens, cada rosto é passado para a rede treinada e o sistema retorna o nome da pessoa e a confiança da predição.  

## 📊 Resultados
- O modelo funciona melhor quando o dataset contém várias imagens por pessoa.  
- Com poucas imagens (ex: 2 por classe), ocorre overfitting e a acurácia no teste fica baixa.  
- Recomenda-se usar 20+ imagens por pessoa e aplicar Data Augmentation para melhorar o desempenho.  
