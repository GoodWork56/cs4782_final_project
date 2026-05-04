Delta is the strength of the watermark (the paper chose delta=2)

Gamma is the size of the green list (the paper chose gamma=0.25)

Threshold is the z-score at which this and above we believe the text to be AI (the paper chose threshold=4)

TPR stands for True Positive Rate (The rate at which an AI text is correctly flagged as AI)

FPR stands for False Positive Rate (The rate at which a human text is incorrectly flagged as AI)

Perplexity (PPL) is a measure of how “surprised” a language model is by a text, defined as the exponentiated average negative log-probability of the sequence under the model. In this paper it is used to assess whether watermarking harms generation quality, where lower perplexity indicates more natural and higher-quality text.