# GenAI Based ShopAssist Application

## Introduction

In this project, task is to build ShopAssist AI, which is a laptop recommendation chat-bot that can:
- Interact with users interactively,
- Understand the user’s laptop requirements, and,
- Recommend the most suitable laptops based on their needs and preferences.

## Project Background
In today’s digital age, online shopping has become the preferred option for many consumers.
However, the vast array of choices and the lack of personalised assistance can make the shopping experience overwhelming and challenging.
This chat-bot combines the power of LLMs and rule-based functions to provide accurate and reliable recommendations during the online laptop shopping experience.

## Problem Statement
Given a dataset containing laptop information (product names, specifications, descriptions, etc.), build a chat-bot that parses the dataset and provides accurate laptop recommendations based on user requirements. 
This chat-bot, named ShopAssist AI, will
- Interact with users,
- Understand their laptop requirements,
- Recommend the most suitable laptops from a dataset based on their needs and preferences.

Primarily, this chat-bot will analyse the ‘Description’ column for each laptop,
understand whether the user’s requirements match the laptop's specifications and
then forward a relevant laptop as a recommendation.

## System Design / Architecture
This entire project will be divided into 3 stages:

### Stage 1: Understanding User Requirement
This stage will actually interact with the user proactively and understand the user's requirements.
It is very much necessary that user provides all the necessary information which are needed to filter out products from the database.
Therefore, this stage will keep the conversation alive with the user until all the required information about the product is received.
Once all the required information is extracted from the user, the same will be provided to the next stage in appropriate format.

### Stage 2: Product Mapping & Extraction
All the details about the products (which are in database) are first gathered and 
information is extracted from these products in the same format which is provided as an output of Stage 1
Strict comparison are made to filter out only those products from the database which matches the user requirement provided by Stage 1
Hereby, only the filtered & top 3 products will be sent out  to the next stage for recommending to the user

### Stage 3: Product Recommendation
Here, the chat-bot indulges itself as a good sales representative to elaborate on the product which are provided by previous stage.
This chat-bot needs to explain the filtered products to the user from the user perspective / profile by carefully detailing all the information accurately.

Finally, all the stages are combined to form an interactive chat-bot which can be deployed on web
