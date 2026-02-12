This project implements a state-of-the-art Vision-Encoder-Decoder architecture. It leverages the hierarchical power of the Swin Transformer as a vision encoder and the autoregressive capabilities of GPT-2 as a linguistic decoder to generate human-like captions for complex visual scenes.

🚀 Architectural HighlightsEncoder: microsoft/swin-tiny-patch4-window7-224Uses Shifted Window Self-Attention to capture both local textures and global spatial relationships.Hierarchical design allows for multi-scale feature extraction.Decoder: gpt2Fine-tuned for conditional text generation based on visual hidden states.Implemented with Beam Search ($k=4$) to optimize sequence probability.Dataset: Trained and evaluated on COCO2017, the gold standard for image-to-text tasks.


 Performance MetricsThe model was evaluated on a sampled test set from COCO2017, achieving competitive scores for a base-sized model:MetricScoreInterpretationROUGE-L39.0Measures sentence-level structural similarity (Longest Common Subsequence).BLEU-410.3Measures exact n-gram overlap; reflects precision in word choice.


 🖥️ Live Interface (Gradio)
The project includes a Gradio web interface that allows users to:

Upload any image (JPG/PNG).

Adjust Beam Search size for more deterministic or diverse captions.

Modify Temperature to control the "creativity" of the GPT-2 decoder.
