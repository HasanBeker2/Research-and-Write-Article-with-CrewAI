# L2: Create Agents to Research and Write an Article

This project demonstrates the use of crewAI, a framework for creating and managing multi-agent systems. In this notebook, agents are created to collaboratively research and write an article.

## Requirements

To run this project, you need to install the following libraries. If you're running this notebook on your own machine, you can install the necessary libraries using the following command:

```sh
pip install crewai==0.28.8 crewai_tools==0.1.6 langchain_community==0.0.29
```

## Overview

### About crewAI

crewAI is a framework designed for creating and managing multi-agent systems. It allows for the integration of various language models and tools to build collaborative agents capable of performing complex tasks.

### Creating Agents

In this project, agents are defined with specific `roles`, `goals`, and `backstories`. OpenAI's `gpt-3.5-turbo` is used as the language model for these agents. 

### Agent Roles
- **Planner:** Creates a plan for the article.
- **Writer:** Writes the content based on the plan.
- **Editor:** Edits the written content.

### Creating Tasks

Tasks are defined for each agent with:
- `description`
- `expected_output`
- `agent` assigned to the task

Tasks include:
- **Plan:** Creating a plan for the article.
- **Write:** Writing the content.
- **Edit:** Editing the content.

### Creating the Crew

A crew of agents is created and tasks are assigned to them. Tasks are performed sequentially as they are dependent on each other. The `verbose=2` option is used to see detailed logs of the execution.

### Running the Crew

Agents are executed to produce the results. Note that language models can provide different outputs for the same input, so results may vary.

### Displaying Results

Results of the execution are displayed as markdown within the notebook.

## Try it Yourself

You can experiment by passing in a topic of your choice and observing how the agents handle it.

## Using Other Popular Models

crewAI allows the integration of various popular models as language models for agents, such as:
- **Hugging Face:** Using the `HuggingFaceHub` endpoint.
- **Mistral API**
- **Cohere**

For more information on connecting to various LLMs, refer to the crewAI documentation on [Connecting to any LLM](https://docs.crewai.com/how-to/LLM-Connections/).

