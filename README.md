# Audio Classification using CNNs 🎶🔊

This project performs **audio classification** on rainforest soundscapes using **Convolutional Neural Networks (CNNs)**.  
The dataset was generated using [Scaper](https://github.com/justinsalamon/scaper) to mix rainforest background noises with sounds from the **UrbanSound8K** dataset.

---

## Dataset
You can download it directly from [Data](https://drive.google.com/drive/folders/1YuzRUYVXOscxmsvQSffU8cBoBdDGnlrq?usp=sharing)

- Directory structure:
  - `background/` → rainforest background sounds
  - `chainsaw/` → background + chainsaw sounds
  - `engine/` → background + engine sounds
  - `storm/` → background + thunderstorm sounds
- Each class contains **100 WAV files**.

---

## Workflow
1. **Convert audio to spectrograms**  
   - Generated Mel-spectrograms from `.wav` files using **Librosa**.
   - Saved spectrograms as `.png` images.

2. **Load spectrogram images**  
   - Resized images to `224x224`.
   - Normalized pixel values.

3. **Build CNN model (Keras)**  
   - 4 convolution + max-pooling layers  
   - Dense layer with 1024 units  
   - Output layer with 4 softmax classes

4. **Train model**  
   - Optimizer: `Adam`  
   - Loss: `SparseCategoricalCrossentropy`  
   - Trained for **50 epochs** with validation split.

5. **Evaluate performance**  
   - Achieved **~81% test accuracy**.  
   - Plotted training/validation accuracy.  
   - Displayed confusion matrix for class predictions.

---

## Results 📊
- **Training Accuracy:** → 100% (final epoch)  
- **Validation Accuracy:** → ~84% peak  
- **Test Accuracy:** → **81.25%**  
- **Confusion Matrix:** Shows classification performance across 4 classes.

---

## Example Plots
- Training vs Validation Accuracy  
- Confusion Matrix  
---
