# Emoji Generation with Fine-tuned GPT-2

## Overview

This project involves fine-tuning a GPT-2 (Generative Pre-trained Transformer 2) language model to generate emoji based on a dataset available on Kaggle Datasets. The model is trained on emoji descriptions and associated codepoints to enhance its ability to generate relevant emoji based on input text.

## Project Structure

The project code is written in Python 3 and is designed to run in a Kaggle environment. The key files and directories include:

- **Code File**: The main code file is where the GPT-2 model is fine-tuned for emoji generation. The code is well-documented to guide users through the process.

- **Dataset**: The input data files, including `emoji_df.csv` and other related files, are stored in the `/kaggle/input/emoji-data-descriptions-codepoints/` directory.

- **Results**: The output of the fine-tuning process, including the trained model and tokenizer, is saved in the `/results/` directory.

## Code Explanation

The code begins by loading the necessary libraries and defining the input data directory. It then uses the Hugging Face Transformers library to fine-tune the GPT-2 model for language modeling. The trained model and tokenizer are saved locally and pushed to the Hugging Face Hub for easy sharing and access.

## Fine-tuning Process

The fine-tuning process involves tokenizing the input dataset, setting up data collation for language modeling, configuring training arguments, and initiating the training using the Trainer class from the Transformers library. The model is saved at specified intervals, and the final trained model and tokenizer are pushed to the Hugging Face Hub.

## Model Testing

A testing function, `generate_emoji`, is provided to demonstrate the model's capability to generate emoji based on input text. The function loads the trained model and tokenizer, uses the Transformers pipeline for text generation, and returns the generated emoji text.

## Getting Started

To fine-tune the GPT-2 model and generate emoji, follow these steps:

1. Ensure you have the required dependencies by installing them with the provided commands.
2. Load the dataset, specifically the `emoji_df.csv` file, from the specified input directory.
3. Run the `fine_tune_gpt2` function, providing the path to the dataset and specifying any optional parameters.
4. After fine-tuning, test the model using the `generate_emoji` function with your desired input text.

Feel free to experiment with hyperparameters, such as the number of training epochs and learning rate, to optimize the model's performance.

## Dependencies

- pandas
- datasets
- transformers
- huggingface_hub

## Note

Ensure that you have the Kaggle environment set up and the necessary dataset files available in the specified input directory before running the code.

Enjoy generating emoji with your fine-tuned GPT-2 model! 🚀🎉
