# Basic-chat-bot
Basic chatbot Code alpha 
#Basic chatbot

import random


def get_response(user_input):
    responses = {
        "hi": ["Hello!", "Hi there!", "Hey!"],
        "how are you?": ["I'm doing well, thank you!", "I'm fine, thanks for asking.", "I'm good!"],
        "what's your name?": ["I'm just a humble chatbot.", "You can call me ChatBot.",
                              "I don't have a name, but you can call me whatever you like."],
        "bye": ["Goodbye!", "Bye!", "See you later!"]
    }

    if user_input.lower() in responses:
        return random.choice(responses[user_input.lower()])
    else:
        return "I'm not sure how to respond to that."


def chat():
    print("Hi, I'm a basic chatbot. How can I help you?")
    while True:
        user_input = input("You: ")
        if user_input.lower() == "exit":
            print("Goodbye!")
            break
        response = get_response(user_input)
        print("ChatBot:", response)


chat()
