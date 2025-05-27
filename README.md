# ContraSiamTrip
Siamese and Triplet Networks for sentence similarity using contrastive learning.

# Sentence Similarity with Siamese and Triplet Networks:
This project demonstrates how to use Siamese Networks and Triplet Networks with BERT to detect semantic similarity between sentence pairs using the PAWS (Paraphrase Adversaries from Word Scrambling) dataset.

# 📦 Installation:
Install the required packages:


pip install transformers datasets sentence-transformers faiss-cpu torchmetrics


# 📚 Dataset:
The PAWS: labeled_final dataset is used, which contains pairs of sentences labeled as paraphrase (1) or not (0).

# 🧠 Models:
1. Siamese Network
Uses BERT embeddings for both input sentences.

Combines the embeddings using element-wise difference and product.

Feeds into a feedforward neural network for binary classification (paraphrase or not).

Optimized with Binary Cross-Entropy loss.

2. Triplet Network
Trains using triplets: an anchor, a positive (paraphrase), and a negative (non-paraphrase).

Learns embeddings such that the anchor is closer to the positive than the negative.

Optimized with Triplet Margin Loss.

# 📈 Results:
Both models report classification performance using precision, recall, F1-score, and confusion matrices for Siamese, while Triplet is evaluated based on embedding quality.

# 📌 Disclaimer:
This project was developed as part of a personal learning journey in NLP. As such, it may include experimental implementations, non-optimized code, or areas for improvement. Feedback, suggestions, and contributions are always welcome!
