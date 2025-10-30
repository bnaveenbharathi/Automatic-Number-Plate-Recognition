# Automatic Number Plate Recognition

Automatic Number Plate Recognition (ANPR) is a computer vision project designed to detect and recognize vehicle number plates from images and video streams. This repository provides an end-to-end solution for extracting license plate information using image processing and deep learning techniques.

## Features

- **License Plate Detection:** Locates number plates within images or video frames.
- **Character Segmentation:** Segments individual characters from detected plates.
- **Character Recognition:** Recognizes alphanumeric characters using trained models.
- **End-to-End Pipeline:** Integrates detection, segmentation, and recognition in a streamlined workflow.
- **Extensible Design:** Easily adaptable for various regions and plate formats.

## Technologies Used

- **Programming Language:** Python
- **Libraries:** OpenCV, NumPy, TensorFlow/Keras or PyTorch, Tesseract OCR, Matplotlib
- **Deep Learning:** CNN-based models for detection and recognition

## Installation

1. **Clone the Repository**
   ```sh
   git clone https://github.com/bnaveenbharathi/Automatic-Number-Plate-Recognition.git
   cd Automatic-Number-Plate-Recognition
   ```

2. **Install Dependencies**
   ```sh
   pip install -r requirements.txt
   ```

   Additional dependencies:
   - [Tesseract OCR](https://github.com/tesseract-ocr/tesseract) (if using Tesseract)
     - Install via: `sudo apt-get install tesseract-ocr` (Linux) or download from [here](https://github.com/tesseract-ocr/tesseract/wiki)

## Usage

You can use the ANPR pipeline on images or video files.

### Run on an Image

```sh
python main.py --image path/to/image.jpg
```

### Run on a Video

```sh
python main.py --video path/to/video.mp4
```

### Example Output

The program will output the detected number plate and recognized text in the terminal and optionally display or save the results.

## Project Structure

```
Automatic-Number-Plate-Recognition/
├── data/                # Sample images and videos
├── models/              # Pretrained models and weights
├── src/                 # Source code for detection, segmentation, recognition
│   ├── detector.py      # License plate detection logic
│   ├── segmenter.py     # Character segmentation logic
│   ├── recognizer.py    # Character recognition logic
│   └── utils.py         # Utility functions
├── main.py              # Main execution script
├── requirements.txt     # Python dependencies
└── README.md            # Project documentation
```

## How It Works

1. **Detection:** Uses image processing and/or deep learning (YOLO, Haar cascades, etc.) to locate the license plate region.
2. **Segmentation:** Extracts individual characters from the detected plate using contour analysis or deep learning.
3. **Recognition:** Identifies each character using an OCR engine (Tesseract) or a trained CNN classifier.
4. **Display/Export:** Outputs the recognized plate number and annotated image/video.

## Training

- **Data:** Use labeled images of license plates and characters for training detection and recognition models.
- **Model:** Train custom CNN models for character recognition or use pre-trained models (e.g., Tesseract).

## Contributing

Feel free to fork the repository and submit pull requests for improvements or bug fixes.

1. Fork the repo
2. Create a new branch (`git checkout -b feature-name`)
3. Make your changes
4. Commit and push (`git commit -am 'Add new feature'`)
5. Open a pull request

## License

This project is licensed under the [MIT License](LICENSE).

## Acknowledgements

- OpenCV team for image processing tools
- Tesseract OCR
- Dataset contributors

## Contact

For questions or support, open an issue or contact [bnaveenbharathi](https://github.com/bnaveenbharathi).
