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


## Como Utilizar o Modelo Fine-Tuned
Para utilizar o modelo fine-tuned para inferências de Visual Question Answering, siga o exemplo abaixo:

```python
from peft import PeftModel, PeftConfig
from transformers import AutoModelForCausalLM

# Carregar a configuração do modelo fine-tuned
config = PeftConfig.from_pretrained("vannynakamura/paligemma_vqav2")

# Carregar o modelo base
base_model = AutoModelForCausalLM.from_pretrained("google/paligemma-3b-pt-224")

# Carregar o modelo fine-tuned
model = PeftModel.from_pretrained(base_model, "vannynakamura/paligemma_vqav2")
```
