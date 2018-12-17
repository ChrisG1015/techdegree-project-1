# techdegree-project-1
#if response != 'y' 'n':
#   input("Oops! That's not a valid answer!\nAre You Trying to break me apart?\nPlease choose [y]es or [n]o!:")
#number_of_guess = 0




import random

print("______Welcome To the Number Game!_____\nFirst Off, What's Your Name?: ")
name = input()
response = input("Hi, " + name + "! Would You Like To Play A Game? [y]es or [n]o:")
#print("okey dokey, " + name + "!")

random.seed()

while True:
    if response == 'y':
        number = random.randint(1, 10)
        number_of_guess = 0
        while True:
                guess = input("Guess A Number Between 1 - 10: ")
                guess = int(guess)
               # number_of_guess = number_of_guess

                number_of_guess += 1
                if guess < number:
                    print("That's a little low, bring it up a notch!:")
                elif guess > number:
                    print("Thats a tad bit high... take it down a bit!:")

                elif guess == number:
                    print("WOAH! YOU GOT IT! NOT BAD! THIS IS HOW MANY TRIES IT TOOK!: ", "\n>>> ", number_of_guess)

                    response = input("Do you want to play again (y)es or (n)o: ")
                #elif guess != (int)
                 #   print("umm...thats not a number")
                    break
                else:
                    print("ehhh you too many tries! The number was", number)

    elif response == 'n':
        print(":( goodbye " + name)
        exit(0)

    else:
        print('You entered wrong choice. Try again.')
        response = input("Do you want to play again (y)es or (n)o: ")
