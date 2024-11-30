# Text-to-Emoji Translator

## Project Overview
This project involves creating a neural network that translates phrases or sentences into sequences of emojis. The model would identify keywords and contextual meanings from the input text and map them to the most relevant emojis.

## Data Source
Dataset: (https://www.kaggle.com/datasets/rtatman/emojinet/data)

EmojiNet is the largest machine-readable emoji sense inventory that links Unicode emoji representations to their English meanings extracted from the Web. EmojiNet is a dataset consisting of:

1. 12,904 sense labels over 2,389 emoji, which were extracted from the web and linked to machine-readable sense definitions seen in BabelNet
2. Context words associated with each emoji sense, which are inferred through word embedding models trained over Google News corpus and a Twitter message corpus for each emoji sense definition
3. Specification of the most likely platform-based emoji sense for a selected set of emoji (since emoji presentation is different on different platforms)

## Expected Outcomes

1. A functional text-to-emoji translator capable of interpreting and representing text with emoji sequences.
   
2. Insights into how emojis can succinctly convey textual meaning

## Script Breakdown

### Features
1. Dataset Processing: Extracts data from emojis.json. Filters and cleans the dataset to standardize labels and remove invalid data. Combines multiple emoji data sources for improved coverage.

3. Emoji Dictionary Creation: Builds a dictionary of emojis using external sources like the emoji Python library. Consolidates emoji names and symbols into a structured dataset.

3. Data Augmentation: Applies random oversampling to balance the dataset for better model performance.

4. Model Training: Fine-tunes the Hugging Face T5-small model to map descriptive labels (e.g., "happy") to emojis. Supports training on custom input-output pairs.

5. Translation Mechanism: Predicts emojis for user-provided text using the trained T5 model. Includes a fallback mechanism that directly maps words to emojis from the dataset if the model fails.

6. Interactive Interface: Provides an interactive command-line interface to translate text into emojis.

### File Structure

1. emojis.json.zip: Compressed dataset containing emoji information.

2. processed_emojis.csv: Preprocessed dataset saved after cleaning.

3. emoji_t5_model/: Directory containing the fine-tuned T5 model and tokenizer.

### Setup Instructions

1. Install Dependencies: pip install pandas emoji torch transformers

2. Prepare Dataset: Upload the emojis.json.zip file. Extract the file using the provided script.

3. Preprocess Data: Run the code to clean and combine datasets. Save the processed dataset as processed_emojis.csv.

4. Train the Model: Fine-tune the T5 model on the processed dataset. Save the trained model and tokenizer for future use.

5. Run the Translator: Use the interactive translator to input text and receive emojis as output.

### Usage - Running the Emoji Translator

1. Translate Text to Emoji: Input a phrase, such as "happy" or "car," and the system will output the most relevant emoji.

2. Interactive Mode: Run the interactive_emoji_translator_with_fallback() function to launch an interactive session. Type "exit" to quit.

## References
Dataset: (https://www.kaggle.com/datasets/rtatman/emojinet/code)

Sanjaya Wijeratne, Lakshika Balasuriya, Amit Sheth, Derek Doran. EmojiNet: An Open Service and API for Emoji Sense Discovery. In 11th International AAAI Conference on Web and Social Media (ICWSM 2017). Montreal, Canada; 2017.
EmojiNet was developed by Sanjaya Wijeratne, Lakshika Balasuriya, Amit Sheth and Derek Doran. EmojiNet is licensed under a Creative Commons Attribution-NonCommercial-ShareAlike 3.0 Unported (CC BY-NC-SA 3.0) license.. 

## Contact

For any questions or suggeations, feel free to contact:
Louis Canjar, Rian King, Natasia McLean, John Wolfe
