

### Installation

> [!IMPORTANT]
> Installation is mandatory.

```bash
git clone --depth 1 https://github.com/tao-2-v0/RZAI-Factory.git
cd RZAI-Factory.git
pip install -e ".[torch,metrics]"
```

Extra dependencies available: torch, torch-npu, metrics, deepspeed, bitsandbytes, hqq, eetq, gptq, awq, aqlm, vllm, galore, badam, qwen, modelscope, quality

> [!TIP]
> Use `pip install --no-deps -e .` to resolve package conflicts.

### Quickstart

Use the following 3 commands to run LoRA **fine-tuning**, **inference** and **merging** of the Llama3-8B-Instruct model, respectively.

```bash
llamafactory-cli train lesson_plan/lora/llama3.1_8b_lora_sft_train.yaml
llamafactory-cli export lesson_plan/lora/llama3.1_8b_lora_sft_export.yaml
```

### Deploy with OpenAI-style API and vLLM

```bash
API_PORT=8000 llamafactory-cli api ???
```