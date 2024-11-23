# Deep Learning-Based Human Action Recognition

## Abstract  
This thesis aims to develop a deep learning model for human action recognition in videos, specifically for monitoring regulatory compliance at **Novo Nordisk**, a leading pharmaceutical company in Denmark.

The research addresses the need for automated, accurate, and real-time monitoring of human actions in manufacturing environments to ensure adherence to safety and regulatory protocols.  

The proposed model combines Convolutional Neural Networks (CNNs) with Recurrent Neural Networks (RNNs) to leverage their strengths:  
- **CNNs** capture spatial information within video frames, utilizing **InceptionV3** for frame-level feature extraction.  
- **RNNs**, specifically Long Short-Term Memory (LSTM) layers, process and model temporal dependencies and dynamics across frame sequences, enabling robust action recognition in diverse industrial settings.  

The findings highlight the potential of this approach for automating compliance monitoring in the pharmaceutical industry and broader applications in **video surveillance, human-computer interaction, and sports analytics**.

---

## Problem Statement  
The need to accurately interpret human actions in videos is vital for applications such as:  
- Autonomous systems  
- Behavioral analysis  
- Video retrieval  

The challenge lies in effectively capturing both **spatial** and **temporal** features:  
- **CNNs** excel at extracting spatial features but fail to model temporal dependencies.  
- **RNNs** capture temporal dynamics but struggle with raw video frames' complex spatial information.  

### Key Challenge  
**How can we design a model that integrates spatial and temporal information to accurately recognize predefined human actions in video sequences?**

---

## Methodology  
This project utilizes a hybrid architecture:  
1. **Pretrained CNN (InceptionV3)**: Used as a feature extractor to capture spatial information from video frames.  
2. **RNN with GRU**: Processes the temporal relationships between frames.  
3. **Fully Connected Layer**: Performs the final classification.  

This combination enables the model to effectively handle spatial and temporal aspects of video data, essential for achieving accurate video classification.

---

## Environment Setup  
- The implementation was carried out using **Google Colab**, leveraging high-performance **GPUs** and **TPUs** for training and evaluation.  
- The dataset, stored in **Google Drive**, was mounted within the Colab environment for efficient access.

---

## Dataset and Scope  
- A **self-curated dataset** with selected categories from the **UCF50 dataset** was used, emphasizing foundational methodologies due to limited resources.  
- **Transfer learning** with pretrained InceptionV3 was applied for computational efficiency.  

### Limitations  
- Advanced models like **Transformers** and **3D CNNs** were excluded due to computational constraints.  

---

## Training and Evaluation  

### Key Observations  
1. **Initial Performance**:  
   - Training accuracy: **45.85%**  
   - Validation accuracy: **0.77%**  
   - Training loss: **1.0259**  
   - Validation loss: **1.2667**  

2. **Performance Improvements**:  
   - Validation accuracy reached **96.92%** by epoch 6.  
   - Best model checkpoint: **Epoch 26**, validation loss of **0.1689**, validation accuracy **97.69%**.  

3. **Final Performance**:  
   - Validation accuracy stabilized at **96.92%**.  
   - Test set accuracy: **100%**, demonstrating excellent generalization.  

4. **Overfitting Analysis**:  
   - Final training accuracy: **99.34%**.  
   - Minimal divergence between training and validation accuracy, confirming robustness.

---

## Inference Results  
The model was tested on a randomly selected video. The predicted class probabilities are:  
- **Biking**: **93.99%**  
- **Diving**: **3.95%**  
- **IceDancing**: **2.06%**  

The results show a high-confidence prediction for the **Biking** class, with lower probabilities for other classes.

---

## Summary of Findings  
- The CNN-RNN model is **highly effective** for video classification in human action recognition tasks.  
- Strong performance was observed in standard accuracy metrics and confidence evaluations.  
- The results demonstrate the model's robustness in handling unseen data and capturing essential spatial and temporal patterns.

---

## Scope for Future Work  
Future studies could explore:  
- Incorporating advanced models like **Transformers** and **3D CNNs**.  
- Expanding the dataset to include more diverse actions.  
- Optimizing the architecture for real-time deployment in manufacturing settings.

---

## How to Run  
1. Clone this repository:  
   ```bash
   git clone https://github.com/your-username/your-repository.git
