Grammar Scoring Engine for Voice

This project implements a Grammar Scoring Engine that takes spoken-voice samples as input and outputs a grammar-score on a scale (e.g., 0–5) reflecting the grammatical correctness of the spoken response. It is designed for applications such as language learning, automated speaking assessment, and interview-preparation feedback.

Key Features

Uses automatic speech recognition (ASR) to convert voice samples into text (leveraging e.g., the Whisper model).

Applies a fine-tuned text-understanding model (e.g., BERT or variants) to assess grammatical correctness, combined with rule-based features.

Supports both single-file scoring and batch processing of multiple audio files.

Getting Started

Prerequisites

Python 3.8+

Google Colab (recommended) or local GPU environment

(Optional) Kaggle account to access the dataset

Installation

git clone https://github.com/SriKrishnaMishra/-Grammar-Scoring-Engine-for-Voice  
cd Grammar-Scoring-Engine-for-Voice  
pip install -r requirements.txt  


Usage Example

from grammar_scorer import GrammarScoringEngine  
scorer = GrammarScoringEngine()  
score = scorer.score_audio("path/to/audio.wav")  
print(f"Grammar Score: {score}/5")  
# Batch mode:  
scores = scorer.score_batch(["file1.wav", "file2.wav", …])  

Dataset

The system is built and evaluated using the “SHL Grammar Scoring Dataset” which comprises ~444 voice samples (45–60 seconds each) annotated with grammar-scores (0–5). Samples include speakers with varied accents and real-world speaking contexts.

Results & Insights

ASR (Whisper) provides high-quality transcriptions even in accented/noisy speech.

Fine-tuning BERT-style models on transcript data enables capturing grammatical patterns effectively.

A hybrid approach (ASR + NLP grammar model + rule-based features) yields stronger performance than pure individual approaches.

Although the dataset is relatively small, careful augmentation and evaluation show competitive error metrics.

Future Improvements

Support for additional languages beyond English

Real-time scoring API or web interface for easy use

Larger-scale training dataset and domain-adaptation

Detailed error-feedback (highlighting which grammar structures were problematic)

Integration into language-learning platforms or speaking-practice apps

Contributing

Contributions are welcome! Feel free to open issues or pull-requests.

License

This project is licensed under the MIT License.

Author

Sri Krishna Mishra (GitHub-https://github.com/SriKrishnaMishra/-Grammar-Scoring-Engine-for-Voice)

Thank you for checking out this project — your feedback is much appreciated!
