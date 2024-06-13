# Natural-language-to-SQL

## Situation

In modern data-driven applications, interacting with databases is a common task. However, writing SQL queries can be intimidating for non-technical users. To address this challenge, the SQL-NLP Translator project aims to develop a system that translates natural language queries into SQL commands, making database querying more accessible and intuitive.

## Task

The primary task of this project is to train a language model to understand natural language questions related to databases and accurately generate corresponding SQL queries. This involves fine-tuning a pre-existing language model using Parameter-Efficient Fine-Tuning (PEFT) with Low-Rank Adaptation (LoRA) techniques to optimize model performance and efficiency.

## Method

### Parameter-Efficient Fine-Tuning (PEFT)
PEFT is a technique used to fine-tune large language models efficiently by updating only a small subset of parameters. It reduces computational resources and time required for fine-tuning while maintaining model accuracy.

### Low-Rank Adaptation (LoRA)
LoRA is a specific method within PEFT that focuses on adapting low-rank matrices efficiently during fine-tuning. This technique optimizes parameter updates, leading to faster convergence and improved efficiency in fine-tuning tasks.

## Example Results

- **Input**: "What is the average number of working horses of farms with greater than 45 total number of horses?"
- **Generated SQL Query**: `SELECT AVG(Working_Horses) FROM farm WHERE Total_Horses > 45`

The model successfully translates natural language queries into SQL commands with high accuracy, providing a user-friendly interface for database interactions.
