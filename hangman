import random

def choose_word():
    words = ["house", "buy", "phone", "hit", "sean", "alexander", "drink", "melon"]
    return random.choice(words)


def display_word(word, guessed_letters):
    display = ""
    for letter in word:
        if letter in guessed_letters:
            display += letter + " "
        else:
            display += "_ "
    return display

def hangman():
    word = choose_word()
    guessed_letters = []
    attempts_left = 10

    print("Welcome to Hangman!")
    
    while True:
        print("\nAttempts left:", attempts_left)
        print(display_word(word, guessed_letters))
        
        guess = input("Guess a letter: ").lower()
        
        if guess in guessed_letters:
            print("You already guessed that letter.")
            continue
        elif guess in word:
            guessed_letters.append(guess)
            print("Good guess!")
        else:
            attempts_left -= 1
            print("Oops, wrong guess.")
        
        if all(letter in guessed_letters for letter in word):
            print("\nCongratulations! You guessed the word:", word)
            break
        elif attempts_left == 0:
            print("\nSorry, you ran out of attempts. The word was:", word)
            break

if __name__ == "__main__":
    hangman()


