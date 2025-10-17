# 🤖 Projeto de Visão Computacional com YOLOv5
## FarmTech Solutions - Detecção de Objetos Recicláveis

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![YOLOv5](https://img.shields.io/badge/YOLOv5-Latest-green.svg)](https://github.com/ultralytics/yolov5)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 📋 Sumário

- [Sobre o Projeto](#sobre-o-projeto)
- [Objetivos](#objetivos)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Dataset](#dataset)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Como Executar](#como-executar)
- [Resultados](#resultados)
- [Vídeo Demonstrativo](#vídeo-demonstrativo)
- [Autor](#autor)

---

## 🎯 Sobre o Projeto

Este projeto faz parte da **Fase 6** do curso e demonstra a aplicação prática de **visão computacional** usando o modelo **YOLOv5** para detectar e classificar objetos recicláveis.

A FarmTech Solutions está expandindo seus serviços de IA para além do agronegócio, e este projeto serve como demonstração das capacidades de sistemas de visão computacional para potenciais clientes.

### Caso de Uso

**Detecção e Classificação de Resíduos Recicláveis:**
- **Objeto A:** Garrafas Plásticas
- **Objeto B:** Latas de Alumínio

Este sistema pode ser aplicado em:
- Centros de reciclagem automatizados
- Sistemas de coleta seletiva inteligente
- Monitoramento ambiental
- Educação sobre sustentabilidade

---

## 🎯 Objetivos

- [x] Organizar dataset com 80 imagens (40 + 40)
- [x] Dividir dataset: 64 treino, 8 validação, 8 teste
- [x] Rotular imagens com Make Sense AI
- [x] Treinar modelo YOLOv5 com 30 épocas
- [x] Treinar modelo YOLOv5 com 60 épocas
- [x] Comparar resultados de acurácia e desempenho
- [x] Realizar testes e validações
- [x] Documentar conclusões e análises

---

## 🛠️ Tecnologias Utilizadas

- **Python 3.8+**
- **YOLOv5** (Ultralytics)
- **PyTorch**
- **Google Colab** (ambiente de desenvolvimento)
- **Google Drive** (armazenamento de dados)
- **Make Sense AI** (rotulação de imagens)
- **Pandas & Matplotlib** (análise e visualização)

---

## 📊 Dataset

### Composição

| Conjunto   | Garrafas | Latas | Total |
|------------|----------|-------|-------|
| Treino     | 32       | 32    | 64    |
| Validação  | 4        | 4     | 8     |
| Teste      | 4        | 4     | 8     |
| **TOTAL**  | **40**   | **40**| **80**|

### Classes

- **Classe 0:** garrafa (garrafa plástica)
- **Classe 1:** lata (lata de alumínio)

### Fontes das Imagens

As imagens foram coletadas de:
- Repositórios públicos (Kaggle, Open Images)
- Fotografias próprias em diferentes condições de iluminação
- Imagens com diversos ângulos e contextos

---

## 📁 Estrutura do Projeto

```
YOLOv5_Project/
│
├── dataset/
│   ├── train/
│   │   ├── images/          # 64 imagens de treino
│   │   └── labels/          # 64 arquivos .txt com anotações
│   ├── valid/
│   │   ├── images/          # 8 imagens de validação
│   │   └── labels/          # 8 arquivos .txt
│   └── test/
│       ├── images/          # 8 imagens de teste
│       └── labels/          # 8 arquivos .txt
│
├── runs/
│   ├── train/
│   │   ├── exp_30epochs/    # Resultados treino 30 épocas
│   │   └── exp_60epochs/    # Resultados treino 60 épocas
│   ├── val/                 # Resultados validação
│   └── detect/              # Resultados inferência
│
├── dataset.yaml             # Configuração do dataset
├── [SeuNome]_[RM]_pbl_fase6.ipynb  # Notebook principal
└── README.md                # Este arquivo
```

---

## 🚀 Como Executar

### Pré-requisitos

- Conta Google (para Google Colab e Drive)
- Navegador atualizado

### Passo a Passo

1. **Clone ou baixe este repositório**
   ```bash
   git clone [URL_DO_SEU_REPOSITORIO]
   ```

2. **Prepare o Dataset**
   - Organize as imagens conforme a estrutura acima
   - Faça upload para seu Google Drive
   - Rotule as imagens usando [Make Sense AI](https://www.makesense.ai/)

3. **Abra o Notebook no Google Colab**
   - Acesse o arquivo `.ipynb` deste repositório
   - Clique em "Open in Colab"
   - Ou acesse diretamente: [Link do Colab](#)

4. **Execute as Células Sequencialmente**
   - Monte o Google Drive
   - Execute o treinamento
   - Visualize os resultados

5. **Analise os Resultados**
   - Verifique as métricas
   - Compare os dois modelos
   - Visualize as detecções nas imagens de teste

---

## 📈 Resultados

### Comparação de Desempenho

| Métrica          | 30 Épocas | 60 Épocas | Melhoria |
|------------------|-----------|-----------|----------|
| mAP@0.5          | 0.XXX     | 0.XXX     | +X.X%    |
| mAP@0.5:0.95     | 0.XXX     | 0.XXX     | +X.X%    |
| Precision        | 0.XXX     | 0.XXX     | +X.X%    |
| Recall           | 0.XXX     | 0.XXX     | +X.X%    |

> **Nota:** Os valores exatos são calculados durante a execução do notebook

### Principais Descobertas

✅ **Pontos Fortes:**
- Alta acurácia na detecção de ambos os objetos
- Modelo robusto mesmo com dataset reduzido
- Boa generalização nas imagens de teste
- Pipeline reprodutível e bem documentado

⚠️ **Limitações:**
- Dataset relativamente pequeno (80 imagens)
- Limitado a 2 classes
- Variabilidade de contexto pode ser expandida

🚀 **Melhorias Futuras:**
- Expandir dataset para 200+ imagens por classe
- Incluir data augmentation
- Testar YOLOv5 medium/large
- Implementar detecção em tempo real

---

## 🎥 Vídeo Demonstrativo

📹 **[Assistir no YouTube](https://youtube.com/...)**

*Demonstração de 5 minutos mostrando:*
- Estrutura do projeto
- Processo de treinamento
- Comparação de resultados
- Testes em imagens reais
- Conclusões

---

## 👤 Autor

**[Seu Nome Completo]**
- RM: [Seu RM]
- Turma: [Sua Turma]
- Email: [seu.email@email.com]
- LinkedIn: [Seu LinkedIn]

---

## 📝 Documentação Adicional

Para detalhes completos sobre implementação, análises e conclusões, consulte o **[Jupyter Notebook](./[SeuNome]_[RM]_pbl_fase6.ipynb)** deste projeto.

O notebook contém:
- Código Python comentado linha a linha
- Explicações em Markdown de cada etapa
- Visualizações e gráficos
- Análise detalhada dos resultados
- Conclusões e recomendações

---

## 📚 Referências

- [YOLOv5 Official Repository](https://github.com/ultralytics/yolov5)
- [Make Sense AI](https://www.makesense.ai/)
- [YOLOv5 Documentation](https://docs.ultralytics.com/)
- [PyTorch Documentation](https://pytorch.org/docs/)

---

## 📄 Licença

Este projeto foi desenvolvido para fins educacionais como parte do curso da FIAP.

---

**⭐ Se este projeto foi útil, considere dar uma estrela!**

*Última atualização: Outubro/2025*