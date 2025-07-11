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

music-lstm/
├── FluidR3_GM.sf2            # SoundFont used for MIDI to audio conversion
├── generated_audio.mid       # Generated MIDI file from the LSTM model
├── generated_audio.wav       # Corresponding audio file converted from MIDI
├── lstm_music_model.pt       # Trained PyTorch LSTM model
├── midi/                     # Directory containing training MIDI files
├── music_lstm.ipynb          # Main Jupyter notebook for preprocessing, training, generation


---

## 🔄 How It Works

1. **MIDI Preprocessing**
   - Filters piano tracks or melodic voices
   - Converts notes and chords into string representations
2. **Sequence Encoding**
   - Maps notes to integer indices
   - Prepares input sequences and targets
3. **Model Training**
   - LSTM learns patterns over time
   - Prevents overfitting with dropout and multi-song training
4. **Generation**
   - Starts from a seed sequence
   - Predicts next notes using temperature sampling
5. **Export**
   - Reconstructs MIDI from predicted notes
   - Converts to `.wav` using `FluidSynth` and SoundFonts

---

## 🛠️ Tools & Technologies

- `Python`, `PyTorch`
- `music21`, `midi2audio`, `FluidSynth`
- `matplotlib`, `NumPy`

---

## ✅ Results

- Generated music that maintains melodic coherence while introducing original variations
- Avoided exact replication of training data through temperature sampling
- Output music playable via any MIDI or audio player

---

## 📎 Future Improvements

- Predict note durations for rhythmic variety
- Incorporate polyphonic/chord generation
- Deploy as a web demo using Gradio or Streamlit
