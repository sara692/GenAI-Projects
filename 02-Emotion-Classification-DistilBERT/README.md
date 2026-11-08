# Emotion Classification with DistilBERT

## 📋 Project Overview
This project implements a text classification system to detect emotions from text using a fine-tuned DistilBERT model. The model is trained on the 'emotion' dataset from Hugging Face, which contains 6 emotion classes.

### 🎯 Objectives
- Fine-tune a DistilBERT model for emotion classification
- Perform comprehensive data cleaning and preprocessing
- Evaluate model performance using accuracy and F1 metrics
- Visualize results through confusion matrices

## 📊 Dataset

### Dataset Information
- **Source**: Hugging Face Datasets (`emotion`)
- **Classes**: 6 emotion categories
  | Label | Emotion |
  |-------|---------|
  | 0 | Sadness |
  | 1 | Joy |
  | 2 | Love |
  | 3 | Anger |
  | 4 | Fear |
  | 5 | Surprise |

### Dataset Splits
| Split | Size |
|-------|------|
| Train | 16,000 samples |
| Validation | 2,000 samples |
| Test | 2,000 samples |

## 🔧 Data Preprocessing

### Data Cleaning Steps
1. **Missing Values Check**: Verified no missing values in the dataset
2. **Duplicate Handling**:
   - Removed exact duplicates (same text and same label)
   - Identified and removed conflicting duplicates (same text with different labels)
3. **Class Distribution**: Analyzed and visualized the distribution of emotions in the training set

### Tokenization
- **Tokenizer**: DistilBERT tokenizer
- **Parameters**:
  - Max length: 512 tokens
  - Padding: True
  - Truncation: True

## 🤖 Model Architecture

### Base Model
- **Model**: DistilBERT (distilled version of BERT)
- **Checkpoint**: `distilbert-base-uncased`
- **Task**: Sequence Classification
- **Output Classes**: 6
- **Trainable Parameters**: ~67 million

### Device Configuration
- **GPU**: Used if available (CUDA)
- **CPU**: Fallback option

## ⚙️ Training Configuration

### Hyperparameters
| Parameter | Value |
|-----------|-------|
| Batch Size | 32 |
| Number of Epochs | 2 |
| Learning Rate | 2e-5 |
| Weight Decay | 0.01 |
| Evaluation Strategy | Per epoch |
| Optimizer | AdamW |
| Loss Function | Cross-Entropy |

### Training Features
- Gradient accumulation
- Weight decay for regularization
- Per-epoch evaluation
- Comprehensive logging

## 📈 Evaluation Metrics

### Primary Metrics
1. **Accuracy**: Overall correct predictions
2. **Weighted F1-Score**: Harmonic mean of precision and recall (weighted by class support)

### Visualization
- Normalized confusion matrix for test set
- Per-class performance analysis
- Error pattern identification

## 🎯 Results

### Model Performance
- Evaluated on held-out test set (2,000 samples)
- Confusion matrix visualization shows:
  - Diagonal values: Class-wise accuracy
  - Off-diagonal values: Misclassification patterns
  - Normalized values: Proportion of correct predictions per class

### Performance Insights
- Identification of most confused emotion pairs
- Class-wise accuracy analysis
- Overall model strengths and weaknesses

## 💻 Usage Guide

### Quick Start
```python
from transformers import AutoModelForSequenceClassification, AutoTokenizer

# Load model and tokenizer
model = AutoModelForSequenceClassification.from_pretrained('path/to/model')
tokenizer = AutoTokenizer.from_pretrained('distilbert-base-uncased')

# Make prediction
text = "Your text here"
inputs = tokenizer(text, return_tensors='pt', truncation=True, padding=True)
outputs = model(**inputs)
prediction = outputs.logits.argmax(-1).item()

# Map to emotion
emotion_map = {0: "sadness", 1: "joy", 2: "love", 3: "anger", 4: "fear", 5: "surprise"}
predicted_emotion = emotion_map[prediction]
```

### Training Your Own Model
1. Load and preprocess the dataset
2. Configure training arguments
3. Initialize the Trainer
4. Run training and evaluation
5. Save the trained model

## 📁 Project Structure
```
emotion-classification/
│
├── README.md
├── requirements.txt
├── src/
│   ├── data_preprocessing.py
│   ├── model_training.py
│   └── evaluation.py
├── notebooks/
│   └── emotion_analysis.ipynb
└── models/
    └── trained_model/
```

## 🔍 Key Findings

### Data Quality Insights
- Initial duplicate analysis revealed data inconsistencies
- Conflicting labels were identified and removed
- Clean data improved model reliability

### Model Performance
- Effective emotion detection across 6 categories
- Clear visualization of prediction patterns
- Identified areas for potential improvement

## 📦 Dependencies

### Required Packages
```
numpy>=1.21.0
pandas>=1.3.0
matplotlib>=3.4.0
seaborn>=0.11.0
scikit-learn>=1.0.0
torch>=1.9.0
transformers>=4.11.0
datasets>=2.0.0
umap-learn>=0.5.0
huggingface-hub>=0.5.0
```

### Hardware Requirements
- **GPU**: Recommended (CUDA-compatible)
- **RAM**: Minimum 8GB
- **Storage**: 2GB free space

## 🚀 Future Improvements

### Potential Enhancements
1. **Model Optimization**
   - Experiment with different pre-trained models (RoBERTa, ALBERT)
   - Implement learning rate scheduling
   - Add cross-validation

2. **Data Augmentation**
   - Back-translation for more training samples
   - Synonym replacement
   - Random text perturbations

3. **Advanced Techniques**
   - Ensemble methods
   - Attention visualization
   - Error analysis dashboard

## 📚 References

1. [Hugging Face Transformers Documentation](https://huggingface.co/docs/transformers/index)
2. [DistilBERT Paper](https://arxiv.org/abs/1910.01108)
3. [Emotion Dataset on Hugging Face](https://huggingface.co/datasets/emotion)

## 📄 License

This project is released under the MIT License — feel free to use it for
learning or as a portfolio reference.

## 👨‍💻 Author

**Sara Ibrahim**  
*Data Scientist | Machine Learning / AI Engineer*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/sara-ibrahim-omran)  
[![Email](https://img.shields.io/badge/Email-Contact%20Me-red?style=flat&logo=gmail)](mailto:Saraomran433@gmail.com)

### 🌟 Let's Connect!

I'm passionate about solving real-world problems with data, machine learning, and AI. Feel free to reach out for:

- 💼 Job opportunities and collaborations
- 📚 Technical discussions and knowledge sharing
- 🚀 Project ideas and innovative solutions

**⭐ If you find this project helpful, please give the repo a star!**


