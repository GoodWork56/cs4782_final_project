Dataset

Hugging Face `allenai/c4` (English), loaded in streaming mode.

pip install datasets transformers torch
from datasets import load_dataset
dataset = load_dataset("allenai/c4", "en", streaming=True)

No local download required. Internet connection required.