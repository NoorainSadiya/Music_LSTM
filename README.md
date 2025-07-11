# 🎶 LSTM-Based Music Generator

An AI model that composes original piano-style melodies by learning from real-world MIDI files using LSTM networks. The project covers full pipeline: dataset creation, model training, generation, visualization, and audio export.

---

## ✨ Demo

🎧 [Listen to a generated sample](#)  
📁 Output MIDI: `generated_audio.mid`  
📁 Output WAV: `generated_audio.wav`  

*(Links or embedded audio players can go here once hosted)*

---

## 📌 Features

- Parses and filters melodic content from multiple MIDI files
- Trains an LSTM model to learn sequential note patterns
- Uses temperature sampling for creative generation
- Converts generated sequences to playable MIDI and WAV files
- Visualizes musical structure through pitch and frequency plots

---

## 🧠 Model Architecture

- `3-layer LSTM` with hidden size `512`
- Input: One-hot encoded sequences of `50` notes
- Output: Predicted next note (classification)
- Loss: `CrossEntropyLoss`, Optimizer: `Adam`

---

## 🗂 Project Structure

