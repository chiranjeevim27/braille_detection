# Braille Character Recognition using Ensemble Model

This repository contains code for a Braille character recognition project using a combination of two pre-trained models and an ensemble approach. The goal is to recognize Braille characters from images and improve accuracy using an ensemble model.

## Dataset

The dataset used for this project is the [Braille Character Dataset](https://www.kaggle.com/datasets/shanks0465/braille-character-dataset) available on Kaggle. It consists of images of Braille characters.

## Data Preprocessing

The dataset is preprocessed using Python and OpenCV. Images are resized to 32x32 pixels and organized into directories based on the first letter of the corresponding Braille character.

## Model Architecture

The project uses two pre-trained models: [EfficientNetV2B0](https://keras.io/api/keras_cv/models/backbones/efficientnetv2/) and another model trained separately. The outputs of these models are combined using a weighted average layer to create an ensemble model. The ensemble model is then fine-tuned on the Braille dataset.

## Training

Training is performed using an ImageDataGenerator with data augmentation. The ensemble model is trained for multiple epochs, and callbacks such as ModelCheckpoint, ReduceLROnPlateau, and EarlyStopping are used to monitor and improve the training process.

## Files

- `braille.ipynb`: Jupyter Notebook containing the entire code for the project.
- `requirements.txt`: File listing the required Python dependencies.

## Usage

1. Clone the repository:

   ```bash
   git clone https://github.com/chiranjeevim27/braille_detection.git
   ```

2. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Download the dataset from the provided Kaggle link and place it in the `./Braille Dataset/Braille Dataset/` directory.

4. Run the Jupyter Notebook `braille.ipynb` to execute the code.

## Results

The final ensemble model achieves improved accuracy compared to individual models. The model weights are saved in the repository for future use.

## Contributors

- [Chiranjeevi](https://github.com/chiranjeevim27/)
  

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Feel free to contribute, report issues, or suggest improvements!
