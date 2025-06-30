# 📦 Modelos de Exemplo - QuickML Creator

Este diretório contém **modelos de aprendizado de máquina já treinados**, prontos para uso nas aplicações web criadas com o **QuickML Creator**. Eles foram desenvolvidos para demonstrar as principais combinações de:

- Tipos de entrada: **números**, **texto** ou **imagens**
- Tipo de modelo treinado: **Keras (.h5)**, **PyTorch (.pt)** e interfaces com simulações baseadas em **ResNet**

Esses modelos são simples e têm como objetivo **mostrar como estruturar um pipeline completo**, da entrada de dados até a predição visível na interface Streamlit ou Gradio.

---

## 🔢 Modelos Numéricos

Esses modelos recebem como entrada um número digitado pelo usuário e retornam outro número como resposta, simulando um processo de **regressão**.

### 1. `SimpleRegressor.h5` (Keras)
- **Entrada esperada:** um valor numérico (por exemplo, `5.2`)
- **Tarefa realizada:** o modelo foi treinado para prever `x²`, ou seja, o quadrado do valor inserido.
- **Uso típico:** ao inserir `5`, o modelo retornará algo próximo de `25`.
- **Formato do modelo:** arquivo `.h5` (Keras)

### 2. `LinearRegressor.pt` (PyTorch)
- **Entrada esperada:** um valor numérico
- **Tarefa realizada:** modelo simula uma regressão linear simples (`y = 2x + 3`)
- **Uso típico:** ao inserir `2.5`, a predição será próxima de `8.0`
- **Formato do modelo:** arquivo `.pt` (PyTorch)

---

## 📝 Modelos de Texto

Modelos capazes de interpretar **frases curtas** e classificar o sentimento como positivo ou negativo. Essas aplicações demonstram tarefas básicas de **processamento de linguagem natural (NLP)**.

### 3. `TextSentimentLSTM.h5` (Keras)
- **Entrada esperada:** uma frase curta (em inglês), como “I love this”
- **Tarefa realizada:** classifica o sentimento da frase como **positivo (1)** ou **negativo (0)**
- **Rede utilizada:** LSTM (Long Short-Term Memory), ideal para sequências de texto
- **Formato do modelo:** arquivo `.h5` (Keras)

### 4. `TorchTextClassifier.pt` (PyTorch)
- **Entrada esperada:** uma frase curta (em inglês)
- **Tarefa realizada:** também realiza classificação de sentimento (positivo/negativo)
- **Rede utilizada:** uma camada linear simples aplicada sobre vetores gerados via `CountVectorizer`
- **Formato do modelo:** arquivo `.pt` (PyTorch)

---

## 🖼️ Modelos de Imagem - Classificação de Gatos vs Cachorros

Esses modelos recebem uma **imagem (JPG ou PNG)** como entrada e retornam se o conteúdo é um **gato** (0) ou um **cachorro** (1). São ótimos para demonstrar aplicações de **classificação de imagem com redes neurais convolucionais (CNNs)**.

### 5. `CatsVsDogs_CNN.h5` (Keras)
- **Entrada esperada:** imagem de um gato ou cachorro
- **Tarefa realizada:** identifica o animal na imagem
- **Rede utilizada:** CNN com camadas convolucionais + pooling
- **Formato do modelo:** arquivo `.h5` (Keras)

### 6. `CatsVsDogs_CNN.pt` (PyTorch)
- **Entrada esperada:** imagem de um gato ou cachorro
- **Tarefa realizada:** mesmo objetivo da versão Keras, mas implementada em PyTorch
- **Formato do modelo:** arquivo `.pt` (PyTorch)

---

## 🧠 Modelos “ResNet” – Simulados ou Pré-Treinados

As aplicações com “ResNet” no QuickML Creator funcionam como **simuladores de interface**, onde o botão "Predict" retorna um valor padrão (ex: `Prediction: 0.75`) apenas para testar o fluxo da aplicação.

Se desejar, você pode substituir esses valores simulados por **modelos reais baseados em ResNet**, como:

- `resnet18` ou `resnet50` da biblioteca `torchvision` para imagens
- `DistilBERT` ou `BERT` para texto
- MLPs simples para entradas numéricas
