# 📄 Relatório Técnico - Previsão de Enchentes com Machine Learning

## 🧩 Descrição do Problema

Enchentes são um dos eventos extremos da natureza que mais causam prejuízos sociais e econômicos, principalmente em regiões urbanizadas e vulneráveis. Este projeto tem como objetivo prever a ocorrência de enchentes com base em variáveis ambientais, estruturais e socioeconômicas.

Utilizamos dados públicos contendo fatores como intensidade da monção, desmatamento, urbanização, drenagem, qualidade de barragens, entre outros.

---

## 🎯 Objetivo do Projeto

Desenvolver um modelo de machine learning capaz de prever, com base em dados históricos, se determinada região possui **risco elevado de enchente**, auxiliando gestores públicos na **antecipação de desastres naturais**.

---

## 🔬 Metodologia

1. **Exploração dos dados (EDA)**:
   - Análise de histogramas e matriz de correlação
   - Verificação de variáveis críticas e outliers
   - Tratamento e limpeza usando intervalo interquartil (IQR)

2. **Levantamento de hipóteses**:
   - Variáveis como `MonsoonIntensity`, `Urbanization` e `Deforestation` têm impacto direto na ocorrência de enchentes.

3. **Pré-processamento**:
   - Criação do rótulo binário `FloodLabel`
   - Normalização com `StandardScaler`
   - Separação em treino (70%) e teste (30%)

4. **Modelagem**:
   - Treinamento de modelo **KNN (k=5)**
   - Avaliação com `accuracy`, `precision`, `recall`, `f1-score`
   - Aplicação de **validação cruzada (5-fold)**

5. **Justificativa do modelo**:
   - KNN foi escolhido por sua simplicidade, eficiência em conjuntos menores e boa interpretabilidade. Serviu como **baseline** para comparar com modelos futuros.

---

## 📊 Resultados Obtidos

- **Acurácia do modelo KNN:** ~52%
- **Validação cruzada:** resultados estáveis entre os folds (variação entre 50% e 56%)
- **Relatório de classificação:** equilíbrio razoável entre precision e recall, apesar da baixa separabilidade.

---

## ✅ Conclusão

O modelo KNN mostrou-se eficaz como ponto de partida, mas **possui limitações na captura de padrões complexos** em dados ambientais. A acurácia de 52% sugere que **outros modelos devem ser considerados**, como:

- Random Forest
- Regressão Logística
- XGBoost
- Redes Neurais (para versões futuras com mais dados)

---

## 📌 Recomendação

- Incorporar modelos mais sofisticados e comparar métricas
- Avaliar importância das variáveis (feature importance)
- Aplicar tuning de hiperparâmetros
- Explorar dados em tempo real e séries temporais
- Gerar alertas automáticos integrados a sistemas de gestão pública

---

## 👨‍💻 Autores

- Rafael Rodrigues de Almeida - RM: 557837  
- Lucas Kenji Miyahira - RM: 555368

---

## 🏁 Conclusão Geral

Este projeto demonstrou a **viabilidade do uso de inteligência artificial para prever enchentes**, servindo como uma base sólida para soluções mais complexas no futuro. O modelo desenvolvido já entrega valor social e técnico, mesmo em sua forma inicial, e está pronto para evoluir com mais dados e técnicas avançadas.
