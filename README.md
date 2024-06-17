# MediBot

MediBot is a suite of advanced medical chatbots designed to assist with various healthcare tasks. The project is organized into three main applications: Basic, Report Assistant, and Advanced, each providing specialized functionalities for different use cases.

## Table of Contents

- [Introduction](#introduction)
- [Demo Video](#demo-video)
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Dependencies](#dependencies)
- [Configuration](#configuration)
- [Contributors](#contributors)


## Introduction

MediBot is designed to offer medical assistance through interactive chat interfaces. It utilizes OpenAI's GPT-4 model to provide responses and facilitate conversations tailored to medical contexts. The project includes:
- **Basic**: A simple chat interface for basic medical queries.
- **Report Assistant**: Assists with report analysis and answers questions based on provided documents.
- **Advanced**: A comprehensive medical diagnostic system with multiple agents and tasks.

## Demo-Video
[![Demo Video](http://img.youtube.com/vi/Fs0JUmZyLZw/0.jpg)](https://www.youtube.com/watch?v=Fs0JUmZyLZw "Demo Video")


## Installation

To set up the MediBot, follow these steps:

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/MediBot.git
    cd MediBot
    ```

2. Create and activate a virtual environment:
    ```sh
    python3 -m venv env
    source env/bin/activate
    ```

3. Install the dependencies:
    ```sh
    pip install -r requirements.txt
    ```

4. Set up environment variables:
    - Create a `.env` file in the project root directory.
    - Add your OpenAI API key:
      ```
      OPENAI_API_KEY=your_openai_api_key
      ```

## Usage

### Basic

To run the Basic MediBot:
```sh
panel serve src\basic.py
```

### Report Assistant

To run the Report Assistant MediBot:
```sh
panel serve src\report_assistant.py
```

### Advanced 

To run the Advanced MediBot:
```sh
panel serve src\advanced.py
```

### All 3 together

To run all 3 together and get an option to select from these three:
```sh
panel serve src\advanced.py src\basic.py src\report_assistant.py
```
Then go to your browser and type:
```sh
http://localhost:5006/
```

## Features 

### Basic:

- Simple chat interface
- Real-time responses using OpenAI's GPT-4 model

### Report Assistant:

- Upload PDF reports for analysis
- Retrieve answers to queries based on the content of the reports

### Advanced:

- Multi-agent system with specific roles (Medical Interviewer, Medical Diagnostician, General Doctor)
- Sequential task processing for comprehensive diagnostics
- Customizable human interface for interaction

## Dependencies

```sh
openai
panel
dotenv
langchain
chroma
crew
crewai
```

## Configuration

### YAML Configuration Files

Agents Configuration ```(config/agents.yaml)```:
Defines the agents involved in the diagnostic process.

Tasks Configuration ```(config/tasks.yaml)```:
Specifies the tasks and the sequence of their execution.

## Contributors

- [Mudit Agrawal](https://github.com/Mudiit4)
- [Mridul Gupta](https://github.com/mridul-g)
