# Projeto de Fine-Tuning do PaliGemma para Visual Question Answering (VQA)

## Descrição do Projeto
Este projeto visa realizar o fine-tuning do modelo PaliGemma para a tarefa de Visual Question Answering (VQA).

## Objetivo
O objetivo principal deste projeto é treinar o modelo PaliGemma de forma eficaz para que ele possa responder a perguntas sobre imagens, proporcionando uma maior precisão e entendimento contextual. Para isso, utilizei o datasets VQAv2.

Parametros:
   - **learning_rate**: 2e-05
   - **train_batch_size**: 4
   - **eval_batch_size**: 8
   - **seed**: 42
   - **gradient_accumulation_steps**: 4
   - **total_train_batch_size**: 16
   - **optimizer**: AdamW com betas=(0.9, 0.999) e epsilon=1e-08
   - **lr_scheduler_type**: linear
   - **lr_scheduler_warmup_steps**: 2
   - **num_epochs**: 10

## Dependências
  1. Instale as dependências:
   ```bash
    pip install -r requirements.txt
   ```
