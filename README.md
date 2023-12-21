# Generative Large Language Models for Human-Like Behavior

This repository contains a functional implementation of a model inspired by the concepts outlined in the paper, "Generative Agents: Interactive Simulacra of Human Behavior."

## Overview

The models provided in this repository are distributed as Jupyter notebooks, designed for easy execution either locally or on Google Colab. For local execution, we recommend using Jupyter Lab for a smoother experience. The notebooks are compatible and should run seamlessly on Google Colab.

## Model Availability

- **Stable Version**: [Generative Model (Simple)](https://github.com/xevor11/Generative_Agents_CS743_Project/notebook/generative_model_simple.ipynb)

## Model Details

The current model simulates the town of Phandalin, an introductory scenario from the Dungeons & Dragons 5e adventure. Phandalin was chosen due to its rich, open-ended nature, providing a more diverse and flexible scenario compared to the simplified setup in the original paper.

## Model Functions

The `generative_model_simple.ipynb` file includes several key functions:

### `generate_action_prompts`

Generates action prompts for the model, considering the current simulation time, individual plans, locations, and memories. It returns a dictionary of prompts for each individual.

### `execute_actions`

Executes actions based on the generated prompts, transforming the action paragraphs into past tense and providing emoji representations of actions. It returns dictionaries containing the resulting actions and their emoji representations.

### `update_memories_ratings`

Updates memory ratings for individuals based on their observations and memories at the current simulation time. It uses a specified function `get_rating` to extract ratings from responses.

### `compress_memories`

Responsible for compressing memories for each individual, this function utilizes memory ratings and generates compressed recollections for the specified number of memories. It returns dictionaries containing the compressed memories.

### `update_location_ratings`

Updates location ratings for individuals based on their observations and prompts. It assesses the likelihood of an individual being in specific areas in the next hour and updates the current location accordingly.

## Constraints and Considerations

The model, as described in the paper, ideally requires access to a high-quality instruction model such as GPT-3. However, due to resource constraints and the need for high-context queries, running such a model can be costly. To mitigate these limitations, this implementation utilizes lower-parameter, locally executable models.

## Future Development

The ongoing development of this project involves:

- **Emoji Representation of Agent Decisions** (Work in Progress)
- **Enhanced Context Compression** - Creating a suite of questions to further compress agent contexts effectively.
- **Verification of Context Compression** - Assessing the efficacy of context compression through an additional layer of prompts.
