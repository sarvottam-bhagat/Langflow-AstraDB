# Langflow Project

[![Langflow Demo](https://img.youtube.com/vi/lSjp5Q-if5c/maxresdefault.jpg)](https://youtu.be/lSjp5Q-if5c?si=-PBxobbSieHOtwnw)

*Click the image above to watch a demonstration of this Langflow application in action.*

## Overview

Langflow is a powerful flow-based UI application for building and deploying AI workflows. This repository contains a Langflow project configuration file (`Langflow.json`) that defines a conversational AI application with vector database integration.

## Langflow.json

The `Langflow.json` file is a configuration file that defines the structure and behavior of a Langflow application. It contains:

- **Flow Definition**: A visual representation of the application's components and how they connect
- **Component Configuration**: Detailed settings for each component in the flow
- **UI Layout**: Positioning information for the visual editor

## Flow Architecture

This particular flow implements a conversational AI application with the following components:

### Input/Output Components
- **ChatInput**: Captures user messages
- **ChatOutput**: Displays agent responses

### Agent Components
- **Agent**: The main conversational agent that processes user queries
- **Prompt**: Template system for structuring agent prompts

### Data Processing Components
- **AstraDB**: Vector database integration for semantic search
- **ParserComponent**: Processes and formats data
- **SplitText**: Divides text into manageable chunks
- **File**: Handles file uploads and processing

### Flow Connections
The components are connected in a workflow that:
1. Takes user input from ChatInput
2. Searches AstraDB for relevant information
3. Processes the search results
4. Combines the results with the user query in a prompt
5. Sends the prompt to the agent
6. Returns the agent's response to ChatOutput

## Usage

To use this flow:

1. Import the `Langflow.json` file into a Langflow instance
2. Configure the AstraDB connection with your credentials
3. Upload relevant documents to be processed and stored in the vector database
4. Start interacting with the chatbot interface

## Requirements

- Langflow application (version 1.3.2 or compatible)
- AstraDB account and API token
- Appropriate embedding models as specified in the configuration

## Configuration

Key configuration elements include:

- **AstraDB Settings**: API endpoints, tokens, collection names
- **Embedding Models**: Configuration for text embedding generation
- **Agent Settings**: System prompts, tools, and behavior parameters
- **UI Layout**: Component positioning and connections

## Additional Information

This flow is designed for retrieval-augmented generation (RAG) applications, allowing the agent to access and reference information from a vector database when responding to user queries.
