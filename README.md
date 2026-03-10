
# 📈 Neuroevolution – Predição de Séries Temporais de Energia Renovável nos EUA

Este repositório apresenta um estudo completo de **predição de séries temporais** baseado no consumo de **energia renovável dos Estados Unidos**, integrando:

- **Modelos estatísticos** (SARIMA)  
- **Redes neurais** (LSTM e MLP)  
- **Algoritmos genéticos** para otimização de hiperparâmetros via **neuroevolução**

O objetivo principal é comparar performances e demonstrar como técnicas de *machine learning* podem ser combinadas com inteligência evolucionária.

---

## 📌 Objetivo

O projeto busca:

- Analisar e prever a evolução do consumo de energia renovável nos EUA  
- Comparar métodos estatísticos e modelos de deep learning  
- Utilizar algoritmos genéticos para otimizar hiperparâmetros de redes neurais  
- Identificar qual abordagem apresenta melhor desempenho preditivo  

---

# 📁 Estrutura do Repositório

```
├── genetic_algorithm/      # Algoritmos genéticos (neuroevolução)
├── neural_network/         # Modelos LSTM e MLP
├── time_series/            # Modelos estatísticos SARIMA
├── datasets/               # Conjunto de dados utilizado
├── requirements.txt        # Dependências do projeto
└── README.md               # Documentação
```

---

# 🔍 Metodologia

## 1️⃣ Modelos Estatísticos — SARIMA  
**Local:** `/time_series`

Inclui:

- Testes de estacionariedade (ADF)
- Identificação de parâmetros (p,d,q)(P,D,Q)
- Análise de resíduos
- Comparação de AIC/BIC
- Métricas: RMSE e MAPE

---

## 2️⃣ Redes Neurais — LSTM e MLP  
**Local:** `/neural_network`

### LSTM
- Modelagem sequencial
- Normalização MinMaxScaler
- Preparação com janelas deslizantes (sliding window)
- Aprendizado de dependências de longo prazo

### MLP
- Arquiteturas densas
- Funções de ativação variadas
- Dropout opcional
- Treinamento supervisionado com janelas fixas

---

## 3️⃣ Neuroevolução — Algoritmo Genético  
**Local:** `/genetic_algorithm`

O algoritmo genético realiza otimização de:

- Número de neurônios
- Funções de ativação
- Taxa de aprendizado
- Número de camadas
- Parâmetros de treinamento

Mecanismos evolutivos:

- Seleção por aptidão (fitness = RMSE)
- Crossover
- Mutação
- Evolução de populações

---

# ▶️ Como Executar

## 1. Clonar repositório
```bash
git clone https://github.com/heitilo/neuroevolution.git
cd neuroevolution
```

## 2. Instalar dependências
```bash
pip install -r requirements.txt
```

## 3. Executar modelos

### SARIMA
```bash
python time_series/sarima_model.py
```

### LSTM
```bash
python neural_network/lstm_model.py
```

### MLP
```bash
python neural_network/mlp_model.py
```

### Neuroevolução (Genetic Algorithm)
```bash
python genetic_algorithm/neuroevolution.py
```

---

# 📊 Resultados Esperados

Cada modelo gera:

- Gráficos comparando previsão x valores reais  
- Curvas de erro (loss)  
- Métricas numéricas:  
  - **RMSE**  
  - **MAE**  
  - **R2**  

O algoritmo genético retorna:

- Melhor indivíduo da população  
- Arquitetura neural otimizada  
- Histórico da evolução  

---

# 📚 Tecnologias Utilizadas

- Python 3.9+  
- NumPy, Pandas  
- Scikit-learn  
- TensorFlow / Keras  
- Statsmodels  
- Matplotlib / Seaborn  

---

# 📖 Referências

- Makridakis et al., *Forecasting Methods*  
- Goodfellow et al., *Deep Learning*  
- Goldberg, *Genetic Algorithms in Search*  
- Documentação Statsmodels  
- Documentação TensorFlow  

---

# 📜 Licença

Este projeto está licenciado sob a **MIT License**.

