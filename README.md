# Uzbek Speech Recognition

Fine-tuning Whisper for Uzbek speech-to-text transcription.

## About

This project fine-tunes OpenAI's Whisper (small variant) on the Uzbek speech corpus to improve transcription accuracy for the Uzbek language. The model was trained on approximately 10,000 audio samples using transfer learning.

## Model

The fine-tuned model is available on HuggingFace Hub: https://huggingface.co/whiteh4t/whisper-small-uzbek

## Usage

```python
from transformers import pipeline

transcriber = pipeline("automatic-speech-recognition", model="whiteh4t/whisper-small-uzbek")
result = transcriber("path/to/audio.mp3")
print(result["text"])
