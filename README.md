## 1. Introduction  
This repo re-implements *“A Watermark for Large Language Models”* (Kirchenbauer et al.), which proposes a method for embedding detectable watermarks in LLM-generated text via token-level biasing during generation.

---

## 2. Chosen Result  
We reproduce Figures 3a, 3b, and Figure 2 (left), analyzing how δ (watermark strength) and γ (green list fraction) affect z-score and perplexity, capturing the trade-off between detectability and text quality.

---

## 3. GitHub Contents  
- code/: Watermark generation, detection, and experiments  
- data/: README describing C4 dataset usage (streaming setup)  
- results/: Plots for z-score, perplexity, parameter sweeps, and extended experiments  
- report/: Final report PDF  
- poster/: Poster PDF used for presentation  

---

## 4. Re-implementation Details  
We implement green-list watermarking using OPT-350M and evaluate detectability via z-score and quality via perplexity using a reference OPT model. Experiments are run on the C4 dataset with PyTorch and Hugging Face libraries.

---

## 5. Reproduction Steps  
Run all cells in `code/FinalProject4782.ipynb`.  
Dependencies: PyTorch, Transformers, Datasets, NumPy, Pandas, Matplotlib (GPU recommended).  
Plots are generated manually from notebook outputs.

---

## 6. Results / Insights  
Our results reproduce the paper’s trends: increasing δ increases both z-score and perplexity, while decreasing γ increases z-score but reduces generation flexibility and increases perplexity. Higher perplexity compared to the paper is attributed to using OPT-350M instead of OPT-6.7B, reflecting differences in model capacity.

---

## 7. Conclusion  
Our implementation validates the paper’s main claim that watermarking introduces a measurable trade-off between detectability and text quality. Results also show sensitivity to model scale and parameter choices.

---

## 8. References  
- Kirchenbauer et al., *A Watermark for Large Language Models*: https://arxiv.org/pdf/2301.10226  
- Model: facebook/opt-350m  
- Dataset: allenai/c4  
- Dataset usage: Hugging Face `datasets` streaming mode  
- Translation models: Helsinki-NLP/opus-mt-en-de, Helsinki-NLP/opus-mt-de-en  
- Frameworks: PyTorch, Hugging Face Transformers, Hugging Face Datasets, NumPy, Pandas, Matplotlib  

---

## 9. Acknowledgements  
We thank Professors Kilian Q. Weinberger and Wei-Chiu Ma, along with the CS 4782 course staff, for their guidance and support throughout the project.