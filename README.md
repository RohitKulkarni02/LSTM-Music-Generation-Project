
# Music Generation Project

This project implements an LSTM (Long Short-Term Memory)-based neural network for music generation. The model is trained on MIDI files to learn temporal patterns in melodies, enabling the generation of coherent and creative music pieces. The goal of this project is to demonstrate how an LSTM network can learn sequential dependencies in music and generate new compositions that mimic the learned musical styles.

## Features

- **LSTM-based Model**: Utilizes an LSTM network to capture long-term dependencies in music sequences.
- **MIDI File Preprocessing**: Converts raw MIDI files into a format suitable for training (sequences of notes and chords).
- **Temperature Sampling**: Implements temperature-based sampling to control the creativity of generated music.
- **Music Generation**: Generates new music sequences that mimic learned musical styles from the training data.

## Installation

### Prerequisites

Make sure you have the following libraries installed:

- Python 3.x
- TensorFlow
- Keras
- NumPy
- Music21 (for MIDI parsing and manipulation)

You can install the required dependencies by running:

```bash
pip install -r requirements.txt
```

### Clone the Repository

Clone this repository to your local machine:

```bash
git clone https://github.com/YourUsername/Music-Generation-Project.git
cd Music-Generation-Project
```

## Usage

1. **Preprocess the MIDI files**: Use the provided script to convert raw MIDI files into sequences that can be used to train the LSTM model. This involves extracting note/chord information and organizing them into input/output sequences for training.

2. **Train the Model**: The LSTM model can be trained on the preprocessed music data using the training script. You can adjust hyperparameters such as the number of epochs, batch size, and LSTM layer configurations to suit your needs.

3. **Generate Music**: Once the model is trained, you can use the generation script to create new music sequences. The temperature parameter controls the level of creativity in the generated music — a higher temperature leads to more diverse output, while a lower temperature produces more predictable melodies.

```bash
python generate_music.py --temperature 0.5
```

### Example Output

After training, you can generate music pieces based on the learned patterns in the training dataset. The output is a MIDI file that contains a sequence of notes/chords in the style of the original training data.

## Structure

- **`train.py`**: Script to train the LSTM model on preprocessed MIDI data.
- **`generate_music.py`**: Script to generate new music based on the trained model.
- **`preprocess.py`**: Script to preprocess MIDI files and convert them into sequences.
- **`model.py`**: Contains the architecture of the LSTM model.
- **`data/`**: Directory to store your MIDI files for training.
- **`output/`**: Directory to store generated music MIDI files.
- **`requirements.txt`**: List of required Python packages for the project.

