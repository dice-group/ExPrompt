![exprompt-high-resolution-logo-black-transparent](https://github.com/user-attachments/assets/236166c4-b1c2-40a1-b611-450d11f5891b)



Detecting the veracity of a statement automatically is a challenge the world is grappling with due to the vast amount of data spread across the web. Verifying a given claim typically entails validating it within the framework of supporting evidence like a retrieved piece of text. Classifying the stance of the text with respect to the claim is called stance classification and is an important part of many approaches that tackle the automatic identification of false information and fake news. Despite advancements in automated fact-checking, most systems still rely on a substantial quantity of labeled training data, which can be costly. In this work, we avoid the costly training or fine-tuning of models by reusing pre-trained large language models together with few-shot in-context learning. Since we do not train any model, our approach ExPrompt is lightweight,
demands fewer resources than other stance classification methods and can server as a modern baseline for future developments. At the same time, our evaluation shows that our approach is able to outperform former state-of-the-art stance classification approaches regarding accuracy by at least 2 percent.

## Pre-Req
In our evaluation, we use Mixtral-8x7B and Llama-3-70B as pre-trained LLMs. Both these LLMs should be hosted as a service on Ollama for reproducing the results. We describe both models in the following.

### Mixtral-8x7B 
Mixtral is a large language model that uses a sparse mixture of expert models. For each token, it uses 2 out of 8 experts, that are implemented as feed-forward networks. As a result, for each token, only a limited set of all model parameters is used, which allows faster inference time. It outperforms the Llama2 model with 70B parameters, on tasks such as mathematics and code writing by using fewer parameters.

### Llama-3-70B 
Llama 3 is a publicly available large decoder-only language model, developed by Meta.2 There are different versions available ranging from 7 billion up to 70 billion parameters. Compared to Llama 2, the Llama 3 model uses a tokenizer with 128K tokens and grouped query attention.

## How to install

```
cd [dataset_name]
python3 stance_detection_using_[LLM_name].py

```
