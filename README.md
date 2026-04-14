# Abordagem Baseada em Visão Computacional e Análise Multivariada para Segurança Patrimonial

Este repositório apresenta o artefato computacional desenvolvido no Trabalho de Conclusão de Curso (TCC) de Rogério de Carvalho Cordovil, no âmbito da Especialização em Computação Aplicada na Indústria 4.0 da Universidade Federal de Roraima (UFRR).

## 📌 Objetivo

Desenvolver e avaliar um sistema de vigilância inteligente capaz de identificar padrões comportamentais associados a situações de risco em ambientes acadêmicos, utilizando a integração entre:

- Visão Computacional
- Análise Multivariada
- Modelagem baseada em funções de risco

## 🧠 Abordagem Proposta

A solução é estruturada como um pipeline de processamento de vídeo composto por:

1. **Detecção de objetos (YOLOv8)**
2. **Agregação temporal das detecções**
3. **Extração de variáveis multivariadas**
4. **Inferência de risco baseada em regras heurísticas**

Diferentemente de abordagens tradicionais, o sistema não se limita à detecção de objetos, mas realiza uma **interpretação comportamental** baseada na combinação de variáveis espaciais, temporais e dinâmicas.

## 🎯 Modelagem Multicenário

A proposta considera três cenários principais:

### 1. Objeto Abandonado
- Tempo de permanência
- Distância a pessoas
- Frequência de interação

### 2. Furto de Bicicleta
- Tempo de interação pessoa-objeto
- Deslocamento do objeto
- Velocidade do indivíduo

### 3. Detecção de Violência
- Variação de centróide
- Entropia da trajetória
- Sobreposição (IoU)
- Divergência de movimento

Cada cenário possui uma **função de risco específica**, permitindo maior interpretabilidade e redução de falsos positivos.

## 📊 Análise Multivariada

O sistema utiliza técnicas estatísticas para análise dos dados:

- **Z-score** → detecção de desvios individuais
- **PCA (Análise de Componentes Principais)** → redução de dimensionalidade
- **Score de risco (R)** → combinação de múltiplas variáveis

Essas técnicas permitem identificar padrões complexos que não seriam detectados por análise univariada.

## 📁 Conteúdo do Repositório

- `17-Analise_Multivariada.ipynb`  
  Notebook principal contendo:
  - processamento dos vídeos
  - extração de variáveis
  - análise estatística
  - geração de gráficos

- `README.md`  
  Documentação do projeto

- `LICENSE`  
  Licença de uso

- `requirements.txt` *(opcional, mas recomendado)*  
  Lista de dependências

## 📦 Dataset

O experimento foi realizado com:

- 30 vídeos (10 por cenário)
- Mais de **120.000 detecções** analisadas :contentReference[oaicite:0]{index=0}

Os datasets incluem cenários simulados e/ou públicos organizados por:

- Objeto abandonado  
- Furto de bicicleta  
- Detecção de violência  

## ⚙️ Tecnologias Utilizadas

- Python
- YOLOv8 (Ultralytics)
- OpenCV
- Pandas
- NumPy
- Matplotlib
- Scikit-learn (PCA, normalização)

## ▶️ Como Executar

1. Clone o repositório:

```bash
git clone https://github.com/SEU-USUARIO/NOME-DO-REPOSITORIO.git

## 🔗 Repositório

Disponível em: https://github.com/rogercordovil-pixel/tcc-vigilancia-multivariada-yolo
