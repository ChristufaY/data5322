# Homework 3 – Bird Species Classification from Sound using Neural Networks

This project applies **deep learning** to classify bird species common to the Seattle area using audio spectrograms. As part of the **Statistical Machine Learning II** course, the goal was to build a custom neural network that learns meaningful features from time-frequency representations of bird calls.

📓 Project Notebooks:  
- `hw3/binary.ipynb` – Binary classification (2 bird species)  
- `hw3/multiclass.ipynb` – Multiclass classification (12 bird species)  

---

## 🎯 Objective

Given spectrogram images of short bird calls, the task was to predict the bird species by training a custom neural network architecture. The project included:

- Training a **binary classifier** for two species
- Building a **12-class CNN** to classify all species
- Evaluating the model on **external mystery test clips**
- Justifying predictions with audio and visual cues

The spectrograms are 2D arrays (128×517) derived from 3-second audio samples, and reflect key frequency-time patterns unique to each species.

---

## 🧠 Neural Network Architecture

A custom **Convolutional Neural Network (CNN)** was developed from scratch using PyTorch/Keras, and iteratively improved through multiple experiments. Highlights include:

- **5 convolutional blocks** with ReLU activation and max-pooling
- **Global average pooling** to reduce overfitting
- Fully connected softmax output layer (12 units)
- Comparison across various optimizers, dropout rates, and layer depths

Two models were built:
- `binary.ipynb`: A lighter CNN trained on two species with high accuracy
- `multiclass.ipynb`: A deeper CNN evaluated across all 12 species

Each architecture was tuned using training accuracy, validation loss, and confusion matrices.

---

## 🐦 External Evaluation

Three real-world mystery clips were processed and analyzed:
- Converted raw MP3 files into spectrograms using the same preprocessing pipeline
- Ran predictions using the trained multiclass model
- Compared predictions to spectrogram visuals and audio clips to identify likely species
- Noted instances where multiple birds may be calling simultaneously, supported by multi-peaked spectrograms and ambiguous model confidence

---

## 🔍 Observations & Insights

- **Challenging Species**: Species with short, noisy, or harmonically dense calls were hardest to classify and often confused with each other.
- **Model Performance**: The CNN showed strong performance on well-separated classes, but struggled with imbalanced classes or overlapping frequency ranges.
- **Training Challenges**: Model training was computationally intensive. Training the full 12-class model took several hours, highlighting practical considerations in model selection and hardware.

---

## 📈 Technical Summary

This project served as an end-to-end application of neural networks to a real-world audio classification task. Key takeaways include:

- Data preprocessing for audio (resampling, spectrogram conversion)
- Designing and debugging CNN architectures
- Evaluating models using accuracy, loss curves, and domain-specific reasoning
- Limitations of CNNs with overlapping or mixed signal inputs
- Insights into alternative models (e.g., spectrogram-based RNNs or transformer-based models)

---

## 📄 Deliverables

- `binary.ipynb`: Binary classification between two selected bird species  
- `multiclass.ipynb`: Full 12-class CNN model with evaluation and test predictions  
- Formal written report (submitted separately): Describes model methodology, experiments, results, and audio-based interpretations

---

## 🧾 Citation

Data was sourced from the Birdcall competition and **Xeno-Canto**, via curated spectrograms provided in the assignment. Spectrograms were processed from 3-second audio clips sampled at 22,050 Hz and visualized as 128×517 arrays.

**Reference**:  
Blewett, L. A., Rivera Drew, J. A., King, M. L., Williams, K. C. W., Backman, D., Chen, A., & Richards, S. (2024). *IPUMS Health Surveys: National Health Interview Survey, Version 7.4*. https://doi.org/10.18128/D070.V7.4

---

## 🏁 Summary

This homework demonstrates practical experience in **deep learning for audio**, combining technical modeling with domain understanding of sound data. It showcases:
- Custom neural network design
- Thoughtful evaluation with external test inputs
- A balance between experimentation and interpretation

The project reflects a blend of machine learning, domain-specific insight, and communication skills—essential for applied AI work.


