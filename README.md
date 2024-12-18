# YouTube Video Summarization

## 🎯 Overview
Automatically extract, transcribe, and summarize YouTube video content using advanced summarization techniques.

## 📚 Summarization Techniques

### 1. Extractive Summarization
- **Approach**: Selects and extracts most important original sentences
- **Characteristics**:
  - Preserves original wording
  - Uses verbatim text fragments
  - More straightforward implementation
  - Directly pulls key sentences from source material

### 2. Abstractive Summarization
- **Approach**: Generates new sentences capturing content essence
- **Model**: DistilBART (sshleifer/distilbart-cnn-12-6)
- **Characteristics**:
  - Creates novel sentences
  - Rephrases and compresses content
  - More flexible and human-like summaries
  - Generates interpretative summaries

## 🚀 Features
- YouTube video transcript extraction
- Automatic Speech Recognition (ASR)
- Dual summarization approaches
- Performance evaluation using ROUGE metrics

## 📦 Technologies
- Python
- Transformers
- YouTube Transcript API
- HuggingSound
- DistilBART Summarization Model

## 🔧 Installation

### Prerequisites
- Python 3.7+
- pip
- FFmpeg

### Install Dependencies
```bash
pip install transformers youtube_transcript_api pytube huggingsound librosa soundfile torch
```

## 💡 Usage

### Abstractive Summarization Example
```python
from transformers import pipeline

summarizer = pipeline('summarization', model="sshleifer/distilbart-cnn-12-6")
summary = summarizer(
    full_transcript, 
    min_length=5, 
    max_length=20
)
```

## 🔍 Key Components
- **Transcript Extraction**: YouTube Transcript API
- **Speech Recognition**: HuggingSound (Wav2Vec2)
- **Summarization**: 
  - Extractive: Sentence ranking
  - Abstractive: DistilBART CNN Model

## 📊 Performance Evaluation
- **ROUGE Metrics**:
  - ROUGE-1: Unigram overlap
  - ROUGE-2: Bigram overlap
  - ROUGE-L: Longest common subsequence
