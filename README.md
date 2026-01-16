
# Breast cancer image classification

🇺🇸: This repository contains the source code and documentation for the practical work of the Digital Image Processing course (Computer Engineering | IFMG - Bambuí Campus).

To meet the goal of applying segmentation, filtering, and classification techniques in a real-world scenario, this project focuses on the analysis of medical images for the detection of breast cancer.

The central objective is to use DIP techniques (specifically segmentation and filtering) as pre-processing to optimize the automatic classification of tissues (Benign vs. Malignant) through Convolutional Neural Networks (CNNs).


🇧🇷: Este repositório contém o código-fonte e a documentação do trabalho prático da disciplina de Processamento Digital de Imagens (Engenharia de Computação | IFMG - Campus Bambuí).

Para atender à proposta de aplicar técnicas de segmentação, filtragem e classificação em um cenário real, este projeto foca na análise de imagens médicas para a detecção de Câncer de Mama.

O objetivo central é utilizar técnicas de PDI (especificamente segmentação e filtragem) como pré-processamento para otimizar a classificação automática de tecidos (Benigno vs. Maligno) através de Redes Neurais Convolucionais (CNN).


## Packages

🇺🇸:
- seaborn: Used to create statistical graphs (Confusion Matrix).
- scikit-learn (sklearn): Used to calculate the final metrics (classification_report and confusion_matrix).
- torch and torchvision: Definition of the CNN architecture (nn.Module), loading of the dataset (ImageFolder), and application of transformations to the images (transforms).
- torchinfo: Preparation of the model's structural summary (summary) with parameter counting.
- pygame: Playback of the audio file (mario_coin.mp3) to alert at the end of execution.
- matplotlib: Plotting graphs and visualization of image samples.
- numpy: Manipulation of multidimensional arrays and structuring of numerical data.
- shutil and os: Directory management and physical copying of files for dataset division (Training/Test/Validation).

🇧🇷: 
- seaborn: Usada para fazer gráficos estatísticos (Matriz de Confusão).
- scikit-learn (sklearn): Usada para calcular as métricas finais (classification_report e confusion_matrix).
- torch e torchvision: Definição da arquitetura da CNN (nn.Module), carregamento do dataset (ImageFolder) e aplicação de transformações nas imagens (transforms).
- torchinfo: Preparação do sumário estrutural do modelo (summary) com contagem de parâmetros.
- pygame: Reprodução do arquivo de áudio (mario_coin.mp3) para alerta ao fim da execução.
- matplotlib: Plotagem de gráficos e visualização de amostras das imagens
- numpy: Manipulação de arrays multidimensionais e estruturação de dados numéricos.
- shutil e os: Gerenciamento de diretórios e cópia física dos arquivos para a divisão do dataset (Treino/Teste/Validação).
## Parameters

🇺🇸:
new_split(Boolean):

- True: Executes the data partitioning routine. The script removes the existing directory structure in data_split, performs random shuffling of the source files (data_og), and recreates the physical distribution between the training, validation, and test folders.
- False: Ignores the partitioning step and uses the pre-existing directory structure.

new_model(Boolean):

- True: Instantiates a new CNN class object, initializes the network weights, and executes the complete training loop (in epochs).
- False: Omits the training step. Loads the state dictionary (state_dict) from a previously saved .pth file and sets the model to evaluation mode (eval()).

save_model(Boolean):

- True: At the end of the training loop execution, serializes the model parameters and saves them to the destination file in the models/ folder.
- False: The trained model resides only in volatile memory and is not saved to disk at the end of execution.

🇧🇷:
new_split(Boolean):
  - True: Executa a rotina de particionamento de dados. O script remove a estrutura de diretórios existente em data_split, realiza o embaralhamento aleatório dos arquivos fonte (data_og) e recria a distribuição física entre as pastas de treino, validação e teste.
  - False: Ignora a etapa de particionamento e utiliza a estrutura de diretórios preexistente.

new_model(Boolean):
  - True: Instancia um novo objeto da classe CNN, inicializa os pesos da rede e executa o loop de treinamento completo (em épocas).
  - False: Omite a etapa de treinamento. Carrega o dicionário de estados (state_dict) de um arquivo .pth previamente salvo e define o modelo para modo de avaliação (eval()).

save_model(Boolean):
  - True: Ao final da execução do loop de treinamento, serializa os parâmetros do modelo e os grava no arquivo de destino na pasta models/.
  - False: O modelo treinado reside apenas na memória volátil e não é gravado em disco ao final da execução.	
## Run Locally

Clone the project

```bash
  git clone https://github.com/eulergomees/breast_cancer_image_classification.git
```

Go to the project directory

```bash
  cd breast_cancer_image_classification
```

Create and activate a new conda envoriment

```bash
  conda create my_env 
  conta activate my_env
```

Install dependencies

```bash
  pip install -r /path/to/requirements.txt
```
Open a code editor (VSCODE exemple)

```bash
  code .
```


## Authors

- [@eulergomees](https://github.com/eulergomees)

