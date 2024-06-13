# Natural-language-to-SQL


## Situation

In modern data-driven applications, interacting with databases is a common task. However, writing SQL queries can be intimidating for non-technical users. To address this challenge, this project aims to develop a system that translates natural language queries into SQL commands, making database querying more accessible and intuitive.

## Task

The primary task of this project is to train a language model to understand natural language questions related to databases and accurately generate corresponding SQL queries. This involves fine-tuning a pre-existing language model using Parameter-Efficient Fine-Tuning (PEFT) with Low-Rank Adaptation (LoRA) techniques to optimize model performance and efficiency.

## Method

### Parameter-Efficient Fine-Tuning (PEFT)
PEFT is a technique used to fine-tune large language models efficiently by updating only a small subset of parameters. It reduces computational resources and time required for fine-tuning while maintaining model accuracy.

### Low-Rank Adaptation (LoRA)
LoRA is a specific method within PEFT that focuses on adapting low-rank matrices efficiently during fine-tuning. This technique optimizes parameter updates, leading to faster convergence and improved efficiency in fine-tuning tasks.

## Model Used: Google Gemma-2b

The Google Gemma-2b model is a state-of-the-art language model developed by Google. It is specifically designed for natural language processing tasks and has been fine-tuned for generating SQL queries from natural language questions in this project.

[Google Gemma-2b Documentation](https://cloud.google.com/vertex-ai/generative-ai/docs/open-models/use-gemma)

## Example Results
In the following examples, the question and context represent the input to the model. The context provides the schema or structure of the database table relevant to the question./n yagd

Example 1:
Question: What is the total revenue generated by farms with more than 1000 chickens?
Context: CREATE TABLE farm (Chickens INTEGER, Revenue FLOAT)
Answer: SELECT SUM(Revenue) FROM farm WHERE Chickens > 1000

Example 2:
Question: How many farms have more than 50 acres of land?
Context: CREATE TABLE farm (Acres FLOAT, Farm_ID INTEGER)
Answer: SELECT COUNT(*) FROM farm WHERE Acres > 50
