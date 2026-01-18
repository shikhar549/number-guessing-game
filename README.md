# number-guessing-game
import random

def secrect_num():
    secrect_num=random.randint(1,50)
    guess=None
    attempts=0
    
    print("Welcome to the number guessing game")
    print("You have to guess the number from 1 to 50")
    print("can you guess it ?")
    name=input("Enter your name:")

    while guess!=secrect_num:

        try:
            
            guess_str=input("Enter the number:")
            guess=int(guess_str)
            attempts +=1

            if guess<secrect_num:
                print("this is too low\ntry again")
            elif guess>secrect_num:
                print("This is too high\ntry again")
            else:
                print(f"Congratulation! {name} You guess it right!")
                print(f"It took {attempts} attempts")
        except ValueError:
            print("Invalid input,please enter valid integer")
if __name__=="__main__":
    secrect_num()

