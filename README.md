# pbl_fase6_farmtech

# FarmTech - Despertar da rede neural
# FIAP - Faculdade de Informática e Administração Paulista

<p align="center">
<a href= "https://www.fiap.com.br/"><img src="assets/logo-fiap.png" alt="FIAP - Faculdade de Informática e Admnistração Paulista" border="0" width=40% height=40%></a>
</p>

<br>


## 👨‍🎓 Integrantes: 
- <a href="https://www.linkedin.com/company/inova-fusca">Anna Cecilia Moreira Cabral</a>
- <a href="https://www.linkedin.com/company/inova-fusca">Heitor Exposito de Sousa</a>
- <a href="https://www.linkedin.com/company/inova-fusca">Letícia Gomez Pinheiro</a> 
- <a href="https://www.linkedin.com/company/inova-fusca">Thiago Sabato Romano</a> 
- <a href="https://www.linkedin.com/company/inova-fusca">Vicenzo de Simone Montefusco</a>

## 👩‍🏫 Professores:
### Tutor(a) 
- <a href="https://www.linkedin.com/company/inova-fusca">Leonardo Ruiz Orabona</a>
### Coordenador(a)
- <a href="https://www.linkedin.com/company/inova-fusca">Andre Godoi Chiovato</a>
## **Projeto Base: Sistema de Irrigação Inteligente Simulado**
---

Export to Sheets
💡 Visão Geral do Projeto
Este projeto faz parte da Fase 6 do PBL e tem como objetivo demonstrar a capacidade da FarmTech Solutions em expandir seus serviços de IA para a área de Visão Computacional.

Desenvolvemos um modelo de Detecção de Objetos utilizando a arquitetura YOLOv5 (You Only Look Once) treinado em um dataset customizado de 80 imagens. O objetivo final é simular a entrega de um sistema de alta acurácia para clientes em novas áreas (saúde animal, segurança patrimonial, etc.).

🎯 Objetivos de Negócio
Demonstrar a acurácia e a velocidade de um sistema de Visão Computacional.

Comparar o desempenho do modelo com diferentes volumes de treinamento (30 vs. 60 épocas).

Entregar um modelo robusto, capaz de identificar objetos com alta confiança.

🛠️ Tecnologias Utilizadas
Modelo: YOLOv5 (Arquitetura S)

Framework: PyTorch

Ambiente: Google Colab (GPU) e Google Drive (Armazenamento)

Rotulação: Make Sense AI

Linguagem: Python

📂 Estrutura da Entrega
A solução completa (código, logs de treinamento e relatórios de análise) está contida no arquivo Jupyter Notebook/Colab.

1. Notebook Jupyter (Relatório Completo)
O arquivo principal da entrega, contendo todo o passo a passo da solução, a descrição do dataset, as comparações de métricas (mAP50, mAP50-95, Loss), os comandos executados e as conclusões do projeto.

Nome do Arquivo: LeticiaGomezPinheiro_rm561332_pbl_fase6.ipynb

➡️ Acesse o Notebook Executável para a Solução Completa:
https://colab.research.google.com/drive/1rFeQxA1zlB3g1nYta88n8x8SlOnhr35u?usp=sharing

⚙️ Passo a Passo da Solução (Sumário Executivo)
O notebook detalhado acima segue as seguintes etapas:

Preparação de Dados: Organização de um dataset de 80 imagens de Notebook e Lápis, divididas em conjuntos de Treino (64), Validação (8) e Teste (8).

Rotulação: Criação dos rótulos no formato YOLO, garantindo a distinção correta entre as Classes 0 (notebook) e 1 (lápis).

Treinamento (Simulação 1): Treinamento do modelo yolov5s por 30 épocas.

Treinamento (Simulação 2): Treinamento do modelo yolov5s por 60 épocas.

Análise e Validação: Comparação das métricas de desempenho. A simulação de 60 épocas foi escolhida como o melhor modelo, atingindo um mAP50 de 94.6% na validação.

Teste Final: Aplicação do melhor modelo (60 épocas) no conjunto de testes para validação final com prints de evidência.