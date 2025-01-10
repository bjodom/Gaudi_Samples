# Using Paramater Efficient Fine Tuning on Llama 3 with 8B Parameters on One Intel&reg; Gaudi&reg; 2 AI Accelerator
There are two steps to this tutorial:  

The first notebook will Fine Tune the Llama3 8B model using Parameter Efficient Fine Tuining (PEFT) and then run inference on a text prompt.  This will be using the Llama3-8B model with two task examples from the Optimum Habana library on the Hugging Face model repository.   The Optimum Habana library is optimized for Deep Learning training and inference on First-gen Gaudi and Gaudi2 and offers tasks such as text generation, language modeling, question answering and more. For all the examples and models, please refer to the [Optimum Habana GitHub](https://github.com/huggingface/optimum-habana#validated-models).

This example will Fine Tune the Llama3-8B model using Parameter Efficient Fine Tuining (PEFT) on the timdettmers/openassistant-guanaco dataset using the Language-Modeling Task in Optimum Habana.

### Parameter Efficient Fine Tuning with Low Rank Adaptation
Parameter Efficient Fine Tuning is a strategy for adapting large pre-trained language models to specific tasks while minimizing computational and memory demands.   It aims to reduce the computational cost and memory requirements associated with fine-tuning large models while maintaining or even improving their performance.  It does so by adding a smaller task-specific layer, leveraging knowledge distillation, and often relying on few-shot learning, resulting in efficient yet effective models for various natural language understanding tasks.   PEFT starts with a pre-trained language model that has already learned a wide range of language understanding tasks from a large corpus of text data. These models are usually large and computationally expensive.   Instead of fine-tuning the entire pre-trained model, PEFT adds a task-specific layer or a few task-specific layers on top of the pre-trained model. These additional layers are relatively smaller and have fewer parameters compared to the base model.

### Merging Models

The second notebook merges the models and saves the newly created model in the models directory.  
