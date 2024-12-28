# OCR Model Using CNN-BiLSTM with CTC Loss

This project implements an Optical Character Recognition (OCR) system using a deep learning model built with Convolutional Neural Networks (CNN), Bidirectional Long Short-Term Memory (BiLSTM) layers, and the Connectionist Temporal Classification (CTC) loss function. The model is designed to recognize and interpret text from image data, making it suitable for various OCR applications.

## Project Overview
The OCR system processes image data, extracts textual features using CNN layers, captures sequential dependencies with BiLSTM layers, and aligns predicted sequences with target labels using the CTC loss function.

### Key Features:
- **Data Preprocessing:** Image normalization, resizing, and tokenization of text labels.
- **Model Architecture:** CNN for feature extraction, BiLSTM for sequence modeling, and CTC for alignment.
- **Custom Data Generator:** Handles image-text pair processing.
- **Training Pipeline:** Supports validation and model checkpointing.

## Dataset: MJSynth (Synth90k)
The **MJSynth Dataset**, also known as **Synth90k**, is a widely used synthetic dataset for OCR tasks. It contains around 9 million synthetic text images generated for OCR training and evaluation.

### How to Access MJSynth Dataset:
1. Visit the [official MJSynth dataset repository](http://www.robots.ox.ac.uk/~vgg/data/text/).
2. Download the dataset files, typically provided as `.tar.gz` archives.
3. Extract the downloaded files into a directory, maintaining the folder structure.
4. Ensure the image paths and corresponding text labels are correctly mapped in your data preprocessing pipeline.

The dataset provides text labels as part of image filenames, making it convenient for OCR training.

## Installation and Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/mohamedemad1210/ocr_model.git
   cd ocr_model
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Organize the dataset:
   Place the extracted MJSynth dataset in the `data/` folder.
4. Run the training script:
   ```bash
   python train.py
   ```

## Training
- The model uses the Adam optimizer and monitors validation loss.
- Training logs and model checkpoints are saved in the `models/` directory.

## Evaluation
After training, run the evaluation script:
```bash
python evaluate.py
```

## Results
The trained model generates predictions for text images and calculates accuracy and loss metrics.

## License
This project is licensed under the MIT License.

## Contact
For questions or collaborations, feel free to contact me at [mohamedemad0016@gmail.com](mailto:mohamedemad0016@gmail.com).

