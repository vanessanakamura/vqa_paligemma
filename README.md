# Projeto de Fine-Tuning do Aligemma para Visual Question Answering (VQA)

## Descrição do Projeto
Este projeto visa realizar o fine-tuning do modelo Aligemma para a tarefa de Visual Question Answering (VQA). VQA é uma tarefa de visão computacional que combina processamento de imagem e linguagem natural para responder perguntas sobre imagens. Com a adaptação do modelo Aligemma, buscamos melhorar a precisão na resposta a perguntas relacionadas ao conteúdo visual de uma imagem.

## Objetivo
O objetivo principal deste projeto é treinar o modelo Aligemma de forma eficaz para que ele possa responder a perguntas sobre imagens, proporcionando uma maior precisão e entendimento contextual. Para isso, utilizamos datasets de VQA, que contêm imagens, perguntas e respostas corretas, como base para o treinamento.

## Modelo Aligemma
Aligemma é um modelo robusto que combina características de processamento de linguagem natural e visão computacional. Ele é utilizado como base para a tarefa de VQA devido à sua capacidade de lidar com inputs multimodais e gerar respostas precisas. A adaptação envolve ajustar os pesos do modelo pré-treinado para se adequar às particularidades do dataset de VQA utilizado.

## Dataset Utilizado
Para treinar o modelo, utilizamos um dataset popular para VQA que inclui um grande número de imagens com perguntas correspondentes e respostas. Esse dataset possibilita que o modelo aprenda a identificar objetos, contextos e relações em uma imagem para responder perguntas em linguagem natural.

## Etapas do Fine-Tuning
1. **Pré-processamento dos Dados**: As imagens e perguntas do dataset foram pré-processadas para serem compatíveis com o modelo Aligemma. Isso inclui normalização das imagens e tokenização das perguntas.
2. **Treinamento**: Realizamos o treinamento do modelo utilizando técnicas de fine-tuning, ajustando os pesos do Aligemma para aprender as características do dataset de VQA.
3. **Avaliação**: Após o treinamento, avaliamos o desempenho do modelo utilizando métricas como `accuracy` e `BLEU` para medir a qualidade das respostas geradas.

## Resultados
Os resultados obtidos indicaram uma melhora significativa na capacidade do modelo de responder corretamente às perguntas sobre imagens, especialmente em categorias de perguntas relacionadas a objetos e contextos visuais. Mais detalhes sobre os resultados e métricas estão disponíveis no relatório do projeto.

## Como Reproduzir o Projeto
Para reproduzir este projeto, siga os passos abaixo:
1. Clone este repositório:
   ```bash
   git clone <URL_DO_REPOSITORIO>
   ```
2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```
3. Execute o script de treinamento:
   ```bash
   python train_vqa_aligemma.py
   ```

## Dependências
- Python 3.8+
- PyTorch
- Transformers
- OpenCV
- Outros pacotes listados em `requirements.txt`

## Contribuição
Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests para melhorar o projeto.

## Licença
Este projeto está licenciado sob a licença MIT. Consulte o arquivo `LICENSE` para mais detalhes.
