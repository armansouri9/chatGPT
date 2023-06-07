# chatGPT
Communication with chatGPT with Python
# GPT-3 Chatbot

This repository contains code for a chatbot powered by OpenAI's GPT-3.5 model. The chatbot utilizes the capabilities of GPT-3.5 to provide interactive and intelligent responses to user input.

## Installation

To run the chatbot, you need to install the `openai` package. You can install it using pip:

```
!pip install openai
```

## Setup

Before using the chatbot, you need to set up your OpenAI API key. Replace `'your api-key'` in the code with your actual API key.

## Usage

The chatbot uses the `chat_with_GPT3` function to interact with the GPT-3.5 model. It takes user input, sends it to the model, and returns the assistant's reply.

To start an interactive conversation with the chatbot, run the following code:

```python
import openai

# Set up your OpenAI API key
openai.api_key = 'your api-key'

def chat_with_GPT3(user_message):
    response = openai.ChatCompletion.create(
        model="gpt-3.5-turbo",
        messages=[
            {"role": "system", "content": "You are a helpful assistant."},
            {"role": "user", "content": user_message},
        ]
    )
    
    assistant_reply = response.choices[0].message.content
    return assistant_reply

# Interact with the chatbot
while True:
    user_input = input("you: ")
    reply = chat_with_GPT3(user_input)
    print("me: ", reply)
```

You can input your message as the user and receive the chatbot's response as the assistant. The chatbot will continue to respond until you stop the program.

Feel free to explore and modify the code to customize the chatbot's behavior based on your requirements.

## Note

Please note that the code provided is a simplified example and may require additional modifications and enhancements to fit your specific use case.
