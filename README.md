# FIAP - Faculdade de Informática e Administração Paulista
[![FIAP Logo](images/logo-fiap.png)](https://www.fiap.com.br)

---
**Integrantes**:
- [Fabio Marcos Pedroso Filho](https://www.linkedin.com/in/pedrosof/) - RM560665

**Professores**:

**Tutor(a)**:
- [Leonardo Ruiz Orabona](https://www.linkedin.com/in/leonardoorabona/)

**Coordenador(a)**:
- [Andre Godoi, PhD](https://www.linkedin.com/in/profandregodoi/)

---
## Links Importantes

**Demonstração** [YouTube](https://youtu.be/AvIl6RQgpFg)

**Arquivos** [Google Drive](https://drive.google.com/drive/folders/16HJyrHcMU68Vvz9WaBrzN-K2rNMlxkUc?usp=share_link)

---
# CardioAI – Classificação e Diagnóstico Automatizado

Este repositório contém dois notebooks principais desenvolvidos como parte do projeto **CardioAI**, cujo objetivo é aplicar técnicas de **aprendizado de máquina** e **processamento de linguagem natural (NLP)** para análise de sintomas e diagnóstico automatizado de risco clínico cardiovascular.

---
## 1. `classificador_risco.ipynb`

### Objetivo
Este notebook é responsável por **classificar o risco clínico de pacientes** com base em sintomas descritos em linguagem natural.  
Ele utiliza um conjunto de dados (`mapa_risco.csv`) com frases e classificações (“alto risco”, “baixo risco”, etc.) para **treinar um modelo de aprendizado supervisionado**.

### Principais etapas
1. **Leitura dos dados** a partir de `/content/drive/MyDrive/CardioAI/Classificador/data/mapa_risco.csv`
2. **Pré-processamento textual**: limpeza de acentos, remoção de stopwords e normalização.
3. **Vetorização** dos textos (TF-IDF).
4. **Treinamento de modelo** (Logistic Regression, Naive Bayes ou similar).
5. **Avaliação do desempenho** com métricas de acurácia, precisão e recall.
6. **Geração de relatórios e gráficos** salvos em `/content/drive/MyDrive/CardioAI/Classificador/reports`.

### Estrutura esperada no Google Drive
```
My Drive/
└── CardioAI/
    └── Classificador/
        ├── data/
        │   └── mapa_risco.csv
        └── reports/
```

---
## 2. `diagnostico_nlp.ipynb`

### Objetivo
Este notebook utiliza **Processamento de Linguagem Natural (NLP)** para identificar sintomas e inferir diagnósticos a partir de frases clínicas.  
O modelo analisa textos livres, detecta padrões linguísticos e gera **predições automáticas de doenças ou condições**.

### Principais etapas
1. **Leitura de arquivos** contendo frases sintomáticas e mapeamentos (`sintomas_10frases.txt`, `mapa_sintomas.csv`).
2. **Tokenização e lematização** para preparação textual.
3. **Mapeamento sintoma → diagnóstico** com base no dataset.
4. **Criação de CSV final** com diagnósticos previstos.
5. **Visualização de resultados** e estatísticas de frequência.

### Estrutura esperada no Google Drive
```
My Drive/
└── CardioAI/
    └── Classificador/
        ├── data/
        │   ├── sintomas_10frases.txt
        │   └── mapa_sintomas.csv
        └── reports/
            └── diagnosticos_preditos.csv
```

---
## Tecnologias Utilizadas
- Python 3.x  
- Google Colab  
- Pandas, NumPy, Scikit-learn  
- NLTK / spaCy  
- Matplotlib / Seaborn  
- Google Drive API (montagem automática)
