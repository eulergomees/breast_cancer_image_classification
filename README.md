# Breast cancer image classification

Este repositório contém o código-fonte e a documentação do trabalho prático da disciplina de Processamento Digital de Imagens (Engenharia de Computação | IFMG - Campus Bambuí).

Para atender à proposta de aplicar técnicas de segmentação, filtragem e classificação em um cenário real, este projeto foca na análise de imagens médicas para a detecção de Câncer de Mama. 

O objetivo central é utilizar técnicas de PDI (especificamente segmentação e filtragem) como pré-processamento para otimizar a classificação automática de tecidos (Benigno vs. Maligno) através de Redes Neurais Convolucionais (CNN).

## Bibliotecas utilizadas:
  - seaborn: Usada para fazer gráficos estatísticos (Matriz de Confusão).
  - scikit-learn (sklearn): Usada para calcular as métricas finais (classification_report e confusion_matrix).
  - torch e torchvision: Definição da arquitetura da CNN (nn.Module), carregamento do dataset (ImageFolder) e aplicação de transformações nas imagens (transforms).
  - torchinfo: Preparação do sumário estrutural do modelo (summary) com contagem de parâmetros.
  - pygame: Reprodução do arquivo de áudio (mario_coin.mp3) para alerta ao fim da execução.
  - matplotlib: Plotagem de gráficos e visualização de amostras das imagens
  - numpy: Manipulação de arrays multidimensionais e estruturação de dados numéricos.
  - shutil e os: Gerenciamento de diretórios e cópia física dos arquivos para a divisão do dataset (Treino/Teste/Validação).

## Parâmetros de configuração:

new_split(Boolean):
  - True: Executa a rotina de particionamento de dados. O script remove a estrutura de diretórios existente em data_split, realiza o embaralhamento aleatório dos arquivos fonte (data_og) e recria a distribuição física entre as pastas de treino, validação e teste.
  - False: Ignora a etapa de particionamento e utiliza a estrutura de diretórios preexistente.

new_model(Boolean):
  - True: Instancia um novo objeto da classe CNN, inicializa os pesos da rede e executa o loop de treinamento completo (em épocas).
  - False: Omite a etapa de treinamento. Carrega o dicionário de estados (state_dict) de um arquivo .pth previamente salvo e define o modelo para modo de avaliação (eval()).

save_model(Boolean):
  - True: Ao final da execução do loop de treinamento, serializa os parâmetros do modelo e os grava no arquivo de destino na pasta models/.
  - False: O modelo treinado reside apenas na memória volátil e não é gravado em disco ao final da execução.	

## Procedimentos para execução:

1. Instalação de Dependências:
  	 Execução do gerenciador de pacotes baseada no arquivo requirements.txt.
2. Execução:
   Configurar as flags descritas em Parâmetros de configuração dentro do arquivo .ipynb e executar as células sequencialmente.