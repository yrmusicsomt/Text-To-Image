
# Fine-Tuning Stable Diffusion on Skyscrapers

This repository provides a Jupyter Notebook for fine-tuning **Stable Diffusion** to generate **skyscraper images** using **Hugging Face's diffusers library**.

## Overview

The notebook demonstrates the following steps:

1. **Downloading the base model** and generating sample images.
2. **Fine-tuning Stable Diffusion** on a custom dataset of skyscrapers.
3. **Generating new images** from the fine-tuned model.

## Features

- **Stable Diffusion fine-tuning** with a custom dataset.
- **Optimization with 8-bit Adam** for reduced memory usage.
- **Image generation comparisons** between base and fine-tuned models.

## Installation

Install the required dependencies:

```bash
pip install git+https://github.com/huggingface/diffusers.git
pip install accelerate
pip install datasets
pip install bitsandbytes
```

## Usage

### 1. Download Base Model & Sample Images
Set an environment variable for the model:

```bash
export MODEL_NAME=stabilityai/stable-diffusion-2-1
```

Run the notebook to initialize and generate images from the base model.

### 2. Fine-Tune the Model
Clone the dataset and Hugging Face's fine-tuning script, then start training:

```bash
# Example command inside the notebook
--use_8bit_adam  # Flag to optimize memory usage
```

The fine-tuned model will be saved in the `city-building-model` folder.

### 3. Generate Images from the Fine-Tuned Model
Load the fine-tuned model and generate new images. Compare the outputs to see improvements.

## Model & Training Details

- **Base Model**: Stable Diffusion 2.1
- **Fine-tuning Method**: Hugging Face's diffusers training scripts
- **Optimization**: Adam optimizer with 8-bit precision
- **Hardware Requirements**: GPU (Google Colab Free Tier supported)

## Results & Observations

- The fine-tuned model produces **higher-quality skyscraper images**.
- **Increasing the number of epochs** improves detail but requires more GPU memory.
- **Using 8-bit Adam** helps optimize memory usage for Google Colab.

## Future Work

- Experiment with **more training iterations** for better refinement.
- Fine-tune on **different architectural datasets**.
- Deploy the model for **interactive generation**.

## References

- [Hugging Face Diffusers](https://github.com/huggingface/diffusers)
- [Stable Diffusion 2.1](https://huggingface.co/stabilityai/stable-diffusion-2-1)
