SynthGen — Synthetic Dataset Generator
A tool that generates diverse synthetic training datasets using Llama 3.2 running locally on GPU. No OpenAI API. No cost per token. Just open source LLMs.
What it does
Give it a topic, set the number of examples, and SynthGen generates diverse training data automatically — Q&A pairs, multiple choice questions, and explanations with follow-up questions. Output is saved as a JSONL file ready for fine-tuning.
Demo
Built with a Gradio UI — enter a topic, choose examples, generate and download your dataset instantly.
Tech Stack

Meta Llama 3.2 3B Instruct
HuggingFace Transformers
BitsAndBytes (4-bit NF4 Quantization)
Gradio
Kaggle T4 x2 GPU

Key Concepts
4-bit Quantization — Compresses Llama 3.2 from 16GB to ~5GB VRAM using BitsAndBytes NF4 format. Makes it possible to run on a free T4 GPU.
Diverse Prompt Templates — Uses 3 different prompt styles to generate varied outputs — simple Q&A, multiple choice, and explanation format. Better diversity means better training data.
JSONL Format — Output is saved as JSON Lines — the standard format for fine-tuning datasets on HuggingFace.
How to Run

Open the notebook on Kaggle
Enable GPU T4 x2
Add your HuggingFace token in Kaggle Secrets as HF_TOKEN
Run all cells
Enter a topic in the Gradio UI and generate your dataset

