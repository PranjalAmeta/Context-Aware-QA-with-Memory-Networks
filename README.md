# Context-Aware Question Answering using Memory Network
## Overview
  + Memory network is a type of neural network architecture that are used to solve tasks that  involve reasoning over long term dependencies.
  + Memory Network works in multiple hops.each hops allows model to revisit the memory refining the info retrieved at each hop.

 + **The purpose of this project is to build a QA system that can:**
   * Understand a given story and retain key information.
   * Answer questions based on multiple hops in the memory, finding relevant information in each step.
   * Support tasks like single supporting fact retrieval as well as complex questions involving multi-hop reasoning.
  
## Dataset
  * The Facebook bAbI Dataset is a synthetic dataset developed by Facebook AI Research to       evaluate the ability of machine learning models to perform reasoning and answer questions    based on text inputs. It is composed of 20 different tasks, each testing a different aspect of logical and contextual reasoning.

## Model Architecture
  + Embedding Layer-Transforms words into dense vectors.
  + Memory Layers(Hops)- Each hop involves a query-to-story matching process that is used to find relevant sentences in the story. The story embedding is iteratively updated based on the attention weights from each hop.
  + Attention Mechanism: Uses a softmax distribution to assign relevance weights to each sentence in the story, helpful in determining wh8ich sentence should we pay attention to determine the answer to the query.

## Model Evaluation
  + To evaluate the model's performance, we utilized the attention weights to see how our model assigned the weights to inference the answer from.
  + Sentences having higher attention weights are more likely to contain answer to the questions.

## Refrences
 + Sainbayar Sukhbaatar, Arthur Szlam, Jason Weston, Rob Fergus, "End-To-End Memory Networks," 2015.
 + Facebook bAbI Dataset - A set of synthetic QA tasks that evaluate a model's reasoning ability
