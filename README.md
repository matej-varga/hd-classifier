# Hirschsprung Disease Classification CNN

## Project Overview

Deep Convolutional Neural Network (DenseNet121) to classify Hirschsprung Disease from AP contrast enema radiographs. Provides probability scores for HD vs. No HD. Proof‐of‐concept advisory tool—not for clinical diagnosis. Research use only; always consult qualified radiologists for definitive interpretation.

## Contents

```
├── model/
│   └── hd_classifier.h5
├── notebook/
│   └── run_classification.ipynb
├── data/
│   ├── positive/    # AP images with confirmed HD
│   └── negative/    # AP images without HD
└── README.md
```

### model/

* `hd_classifier.h5` – Trained Keras model file for inference (DenseNet121).

### notebook/

* `run_classification.ipynb` – Jupyter notebook showing how to load the model and run predictions on new images.

### data/

* `positive/` – Folder of sample AP radiographs labeled positive for HD.
* `negative/` – Folder of sample AP radiographs labeled negative for HD.

## Installation

1. Clone this repository:

   ```bash
   git clone https://github.com/matej-varga/hd-classifier.git
   cd hd-classifier
   ```

## Usage

1. Prepare your input images according to the following criteria:

   * AP projection only.
   * Contrast visible (positive white) and distal colon fully opacified.
   * No borders or frames, no text within the image.
2. Launch the notebook:

   ```bash
   jupyter lab notebook/run_classification.ipynb
   ```
3. Follow the instructions within to load images, preprocess, and run inference.

## Model Architecture

* Base: DenseNet121
* Training data: 1,082 labeled AP images (HD vs. No HD)
* Output: Binary classification with probability score

## Disclaimer & Legal Notice

**Proof of Concept:** This project is intended solely for research and educational purposes. The model is an advisory system and is not intended for clinical diagnosis or treatment. It may produce false positives or negatives, potentially leading to incorrect clinical decisions.

**No Medical Liability:** Use at your own risk. The authors, affiliated institutions, and distributors disclaim any liability for any direct, indirect, incidental, or consequential damages of any kind arising out of the use of this software, including but not limited to personal injury, health issues, or death.

**Ongoing Study:** The performance and safety of this system are still under investigation. Always consult qualified radiologists and pathologists for definitive diagnosis.

---

## License

This repository is licensed under the Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0). See the [LICENSE](LICENSE) file for details.

*Last updated: August 7, 2025*
