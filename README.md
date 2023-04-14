# open source ChatGPT and beyond

Open source efforts to implement ChatGPT-like models and beyond.

| institution                                | model                                                                                      | language                 | base model                                 | main feature                                                                                                                                                                                                                                                                                                                                                               |
| :----------------------------------------- | :----------------------------------------------------------------------------------------- | ------------------------ | :----------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Meta                                       | [LLaMA](https://github.com/facebookresearch/llama)                                            | en                       | -                                          | LLaMA-13B outperforms GPT-3(175B) and LLaMA-65B is competitive to PaLM-540M.<br />Base model for most follow-up works.                                                                                                                                                                                                                                                     |
| @ggerganov                                 | [llama.cpp](https://github.com/ggerganov/llama.cpp)                                           | en                       | LLaMA                                      | c/cpp implementation for llama and some other models, using quantization.                                                                                                                                                                                                                                                                                                 |
| Stanford                                   | [Alpaca](https://github.com/tatsu-lab/stanford_alpaca)                                        | en                       | LLaMA/OPT                                  | use 52K instruction-following data generated by Self-Instructt techniques to fine-tune 7B LLaMA,<br /> the resulting model,  Alpaca, behaves similarly to the `text-davinci-003` model on the Self-Instruct instruction-following evaluation suite.<br />Alpaca has inspired many follow-up models.                                                                 |
| LianJia                                    | [BELLE](https://github.com/LianjiaTech/BELLE)                                                 | en/zh                    | BLOOMZ-7B1-mt                              | maybe the first Chinese model to follow Alpaca.                                                                                                                                                                                                                                                                                                                            |
| Tsinghua                                   | [ChatGLM-6B](https://github.com/THUDM/ChatGLM-6B)                                             | en/zh                    | GLM                                        | well-known Chinese model, in chat mode, and can run on single GPU.                                                                                                                                                                                                                                                                                                         |
| Databricks                                 | [Dolly](https://github.com/databrickslabs/dolly)                                              | en                       | GPT-J 6B                                   | use Alpaca data to fine-tune a 2-year-old model: GPT-J, which exhibits surprisingly high quality<br /> instruction following behavior not characteristic of the foundation model on which it is based.                                                                                                                                                                    |
| @tloen                                     | [Alpaca-LoRA](https://github.com/tloen/alpaca-lora)                                           | en                       | LLaMA-7B                                   | trained within hours on a single RTX 4090,<br />reproducing the [Stanford Alpaca](https://github.com/tatsu-lab/stanford_alpaca) results using [low-rank adaptation (LoRA)](https://arxiv.org/pdf/2106.09685.pdf),<br />and can run on a Raspberry pi.                                                                                                                           |
| ColossalAI                                 | [ColossalChat](https://github.com/hpcaitech/ColossalAI/blob/main/applications/Chat/README.md) | en/zh                    | LLaMA-7B                                   | provides a unified large language model framework, including:<br />Supervised datasets collection<br />Supervised instructions fine-tuning<br />Reward model training<br />RLHF<br />Quantization inference<br />Fast model deploying<br />Perfectly integrated with the Hugging Face ecosystem                                                                            |
| Shanghai AI Lab                            | [LLaMA-Adapter](https://github.com/ZrrSkywalker/LLaMA-Adapter)                                | en                       | LLaMA-7B                                   | Fine-tuning LLaMA to follow instructions within 1 Hour and 1.2M Parameters                                                                                                                                                                                                                                                                                                 |
| PhoebusSi                                  | [Alpaca-CoT](https://github.com/PhoebusSi/Alpaca-CoT)                                         | en/zh                    | LLaMA<br />ChatGLM-6B<br />BLOOM           | extend CoT data to Alpaca to boost its reasoning ability.<br />aims to build an instruction finetuning (IFT) platform with extensive instruction collection (especially the CoT datasets)<br /> and a unified interface for various large language models.                                                                                                                 |
| AetherCortex                               | [Llama-X](https://github.com/AetherCortex/Llama-X)                                            | en                       | LLaMA                                      | Open Academic Research on Improving LLaMA to SOTA LLM                                                                                                                                                                                                                                                                                                                      |
| Together                                   | [OpenChatKit](https://github.com/togethercomputer/OpenChatKit)                                | en                       | GPT-NeoX-20B                               | OpenChatKit provides a powerful, open-source base to create both specialized and general purpose chatbots for various applications.<br /> The kit includes an instruction-tuned language models, a moderation model, and an extensible retrieval system for including <br />up-to-date responses from custom repositories.                                                 |
| nomic-ai                                   | [GPT4All](https://github.com/nomic-ai/gpt4all)                                                | en                       | LLaMA                                      | trained on a massive collection of clean assistant data including code, stories and dialogue                                                                                                                                                                                                                                                                               |
| @ymcui                                     | [Chinese-LLaMA-Alpaca](https://github.com/ymcui/Chinese-LLaMA-Alpaca)                         | en/zh                    | LLaMA-7B/13B                               | expand the Chinese vocabulary based on the original LLaMA and use Chinese data for secondary pre-training,<br /> further enhancing Chinese basic semantic understanding. Additionally, the project uses Chinese instruction data<br /> for fine-tuning on the basis of the Chinese LLaMA, significantly improving the model's understanding and execution of instructions. |
| UC Berkley<br />Stanford<br />CMU          | [Vicuna](https://github.com/lm-sys/FastChat)                                                  | en                       | LLaMA-13B                                  | Impressing GPT-4 with 90% ChatGPT Quality                                                                                                                                                                                                                                                                                                                                  |
| @NouamaneTazi                              | [bloomz.cpp](https://github.com/NouamaneTazi/bloomz.cpp)                                      | en/zh                    | BLOOM                                      | C++ implementation for BLOOM inference.                                                                                                                                                                                                                                                                                                                                    |
| HKUST                                      | [LMFlow](https://github.com/OptimalScale/LMFlow)                                              | en/zh                    | LLaMA<br />Galatica<br />GPT-2<br />...    | An extensible, convenient, and efficient toolbox for finetuning large machine learning models, designed to be user-friendly,<br /> speedy and reliable, and accessible to the entire community.                                                                                                                                                                            |
| [Cerebras Systems](https://www.cerebras.net/) | [Cerebras-GPT](https://huggingface.co/cerebras/Cerebras-GPT-13B)                              | en                       | -                                          | Pretrained LLM, GPT-3 like, Commercially available, efficiently trained on the[Andromeda](https://www.cerebras.net/andromeda/) AI supercomputer,<br />trained in accordance with [Chinchilla scaling laws](https://arxiv.org/abs/2203.15556) (20 tokens per model parameter) which is compute-optimal.                                                                          |
| UT Southwestern/<br />UIUC/OSU/HDU         | [ChatDoctor](https://github.com/Kent0n-Li/ChatDoctor)                                         | en                       | LLaMA                                      | Maybe the first domain-specific chat model tuned on LLaMA.                                                                                                                                                                                                                                                                                                                 |
| LAION-AI                                   | [Open Assistant](https://github.com/LAION-AI/Open-Assistant)                                  | en                       | GPT-J<br />CodeGen<br />FlanT5<br />GPT-JT | a project meant to give everyone access to a great chat based large language model.                                                                                                                                                                                                                                                                                        |
| UCSD/SYSU                                  | [baize](https://github.com/project-baize/baize)                                               | en<br />zh(comming soon) | LLaMA                                      | fine-tuned with[LoRA](https://github.com/microsoft/LoRA). It uses 100k dialogs generated by letting ChatGPT chat with itself. <br />Alpaca's data is also used to improve its performance.                                                                                                                                                                                    |
| UC Berkley                                 | [Koala](https://github.com/young-geng/EasyLM)                                                 | en                       | LLaMA                                      | Rather than maximizing*quantity* by scraping as much web data as possible, the team focus on collecting a small *high-quality* dataset.                                                                                                                                                                                                                                |
| @imClumsyPanda                             | [langchain-ChatGLM](https://github.com/imClumsyPanda/langchain-ChatGLM)                       | en/zh                    | ChatGLM-6B                                 | local knowledge based ChatGLM with langchain.                                                                                                                                                                                                                                                                                                                              |
| @yangjianxin1                              | [Firefly](https://github.com/yangjianxin1/Firefly)                                            | zh                       | bloom-1b4-zh<br />bloom-2b6-zh             | Instruction Tuning on Chinese dataset. Vocabulary pruning, ZeRO, and tensor parallelism<br /> are used to effectively reduce memory consumption and improve training efficiency.                                                                                                                                                                                           |
| microsoft                                  | [GPT-4-LLM](https://github.com/Instruction-Tuning-with-GPT-4/GPT-4-LLM)                       | en/zh                    | LLaMA                                      | aims to share data generated by GPT-4 for building an instruction-following LLMs with supervised learning and reinforcement learning.                                                                                                                                                                                                                                      |
| EleutherAI                                 | [pythia](https://github.com/EleutherAI/pythia)                                                | en                       | -                                          | combine interpretability analysis and scaling laws to understand how knowledge develops<br /> and evolves during training in autoregressive transformers.                                                                                                                                                                                                                  |
| Hugging Face                               | [StackLLaMA](https://huggingface.co/trl-lib/llama-7b-se-rl-peft)                              | en                       | LLaMA                                      | trained on StackExchange data and the main goal is to serve as a tutorial and walkthrough on<br /> how to train model with RLHF and not primarily model performance.                                                                                                                                                                                                      |
| Nebuly                                     | [ChatLLaMA](https://github.com/nebuly-ai/nebullvm/tree/main/apps/accelerate/chatllam)         | en                       | -                                          | a library that allows you to create hyper-personalized ChatGPT-like assistants using your own data and the least amount of compute possible.                                                                                                                                                                                                                              |
| @juncongmoo                                | [ChatLLaMA](https://github.com/juncongmoo/chatllama)                                          | en                       | LLaMA                                      | LLaMA-based RLHF model, runnable in a single GPU.                                                                                                                                                                                                                                                                                                                         |
| @juncongmoo                                | [minichatgpt](https://github.com/juncongmoo/minichatgpt)                                      | en                       | GPT/OPT ...                                | To Train ChatGPT In 5 Minutes with ColossalAI.                                                                                                                                                                                                                                                                                                                             |
| @LC1332                                    | [Luotuo-Chinese-LLM](https://github.com/LC1332/Luotuo-Chinese-LLM)                            | zh                       | LLaMA/ChatGLM                              | Instruction fine-tuned Chinese Language Models, with colab provided!                                                                                                                                                                                                                                                                                                       |
| @Facico                                    | [Chinese-Vicuna](https://github.com/Facico/Chinese-Vicuna)                                    | zh                       | LLaMA                                      | A Chinese Instruction-following LLaMA-based Model, fine-tuned with Lora, cpp inference supported, colab provided.                                                                                                                                                                                                                                                          |
| @yanqiangmiffy                             | [InstructGLM](https://github.com/yanqiangmiffy/InstructGLM)                                   | en/zh                    | ChatGLM-6B                                 | ChatGLM based instruction-following model, fine-tuned on a variety of data sources, supports deepspeed accelerating and LoRA.                                                                                                                                                                                                                                            |
| alibaba                                    | [Wombat](https://github.com/GanjinZero/RRHF)                                                  | en                       | LLaMA                                      | a novel learning paradigm called RRHF, as an alternative of RLHF,  is proposed, which scores responses generated by<br /> different sampling policies and learns to align them with human preferences through ranking loss. And the performance<br />is comparable to RLHF, with less models used in the process.                                                      |
| microsoft                                  | [deepspeed-chat](https://github.com/microsoft/DeepSpeed/tree/master/blogs/deepspeed-chat)     | -                        | -                                          | Easy, Fast and Affordable RLHF Training of ChatGPT-like Models at All Scales.                                                                                                                                                                                                                                                                                              |
| @WuJunde                                   | [alpaca-glassoff](https://github.com/WuJunde/alpaca-glassoff)                                 | en                       | LLaMA                                      | a mini image-acceptable Chat AI can run on your own laptop,  based on[stanford-alpaca](https://github.com/tatsu-lab/stanford_alpaca) and [alpaca-lora](https://github.com/tloen/alpaca-lora).                                                                                                                                                                                   |
