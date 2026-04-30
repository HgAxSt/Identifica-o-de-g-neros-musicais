# Classificação de Gêneros Musicais - Aprendizado de Máquina (TT004)

Este projeto foca na classificação automática de gêneros musicais utilizando sinais de áudio digitalizados, focando em características físicas como timbre e frequência.

## 🎵 Sobre o Projeto
O desafio consiste em identificar assinaturas sonoras a partir de atributos estatísticos extraídos da base de dados **GTZAN**. Diferente de metadados culturais, exploramos a matemática por trás das ondas sonoras.

### Integrantes:
- Davie Schimidt Fonseca
- Hugo Strassa
- Gabriel Sorensen M Traina

## 📊 Dataset
Utilizamos o **GTZAN Dataset** (versão de 3 segundos), que contém:
- **10.000 amostras** (aproximadamente 1.000 por gênero).
- **Atributos principais:** BPM, Spectral Centroid, Zero Crossing Rate e 20 Coeficientes MFCC.
- **Classes:** Blues, Classical, Country, Disco, Hiphop, Jazz, Metal, Pop, Reggae e Rock.

## ⚙️ Tecnologias e Clean Code
O desenvolvimento segue os princípios de **Clean Code** e utiliza as documentações oficiais das bibliotecas:
- `Pandas` e `Numpy`: Manipulação de dados.
- `Scikit-Learn`: Pré-processamento, Árvores de Decisão e Redes Neurais (MLP).
- `Matplotlib` & `Seaborn`: Visualização de matrizes de confusão.

## 🚀 Resultados Obtidos

Até o momento, comparamos dois modelos supervisionados:

| Modelo | Acurácia Geral | Observação Principal |
| :--- | :--- | :--- |
| **Decision Tree** | 65.7% | Sofre para distinguir gêneros similares como Rock e Country. |
| **Neural Network (MLP)** | **87.1%** | Excelente captura de padrões complexos e não-lineares. |

### Insights de Mineração
1. **Assinaturas Únicas:** Gêneros como *Classical* e *Metal* possuem características físicas muito distintas, facilitando a classificação.
2. **Padrões de Confusão:** A similaridade acústica (instrumentação e BPM) entre *Rock* e *Country* gera os maiores desafios para as fronteiras de decisão dos algoritmos.

## 🛠️ Como executar
1. Certifique-se de ter o `Python 3.x` instalado.
2. Instale as dependências: `pip install pandas numpy scikit-learn matplotlib seaborn`
3. Execute o script principal de treinamento.