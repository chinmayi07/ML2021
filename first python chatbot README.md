# ML2021
CODE FOR THE CHATBOT
#Documentation of chatbot
#This is a chatbot to tell the date and time and also weather of a place
#The first thing that this chatbot does is that it greets the user when the user greets the bot.
#The second thing is the bot welcomes the user by asking his/her name
#Then when the user asks the bot what can you do it tells what it does
#The bot gives the date and time when the user gives option as 1 
#If the user gives 2 as choice then it shows the weather of the place the user gives
#Finally when the user give 3 as choice the bot ends the chat 


import random
def greet():
    greet=["Hi I am chatbot and will do you what you ask me to do","Hello I am chatbot and I will you whatever you ask me to do"]
    print(random.choice(greet))

def welcome(name):
    print("Hi",name)
    print("Nice to meeet you!... How can I help you?")

def show_menu():
    print("---------------------------------------------------------------")
    print("       1.I will tell you what is date and time")
    print("       2.I will tell you the weather for the place you ask")
    print("       3.Exit this chat")
    print("---------------------------------------------------------------")
    try:
        return int(input("Enter the number of which you want to know : "))
    except:
        print("Only numbers")

def ask_question(question):
    try:
        return question
    except:
        print("Ask a question")

def weather():
    place=input("Enter the place which you want to know : ")
    if place=="Chennai" or place=="chennai":
        print("The temperature in Chennai is 28 degrees and it is raining slightly")
    elif place=="Vijayawada" or place=="vijayawada":
        print("The temperature in Vijayawada is 26 degrees and it is raining heavily")
    elif place=="hyderabad" or place=="Hyderabad":
        print("The temperature in Hyderabad is 23 degrees and it is raining")
    elif place=="Bhimavaram" or place=='bhimavaram':
        print("The temperature in Bhimavaram is 24 degrees and it is cloudy")
    elif place=="delhi" or place=="Delhi":
        print("The temperature in Delhi is 35 degrees and it is sunny")

def time():
    print("Time")

def bot():
    greeting=input()
    greet()
    name=input('Your good name please?')
    welcome(name)
    question=input()
    ask_question(question)
    option=show_menu()
    while option!=3:
        if option==1:
            time()
        elif option==2:
            weather()
        option=show_menu()
    else:
        print("Thank you!.. Let's meet next time")
        
bot()


Video link for working of the chatbot:

