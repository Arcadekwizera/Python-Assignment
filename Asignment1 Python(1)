import random
# List of words to choose from
word_list = ["apple", "banana", "cherry", "grape", "orange"]
# Select a random word from the list
random_word = random.choice(word_list).lower()
# Initialize variables
user_guess = ["-"] * len(random_word)
guesses_remaining = 6
warnings_remaining = 3
# Vowels
vowels = ['a', 'e', 'i', 'o', 'u']
print("Welcome to the Word Guessing Game!")
print("Here's your word to guess: " + " ".join(user_guess))
# Main game loop
while guesses_remaining > 0 and "-" in user_guess:
 print("Guesses remaining:", guesses_remaining)
 print("Warnings remaining:", warnings_remaining)
 print("Letters not yet used:", " ".join([c.upper() if c == "-" else "-" for c in
user_guess]))

 guess = input("Guess a letter: ").lower()

 # Check if the input is a single letter
 if len(guess) != 1 or not guess.isalpha():
 print("Please enter a single letter.")
 if warnings_remaining > 0:
 warnings_remaining -= 1
 else:
 guesses_remaining -= 1
 continue

 # Check if the letter has already been guessed
 if guess in user_guess:
 print("You've already guessed that letter.")
 if warnings_remaining > 0:
 warnings_remaining -= 1
 else:
 guesses_remaining -= 1
 continue

 # Check if the guessed letter is in the word
 if guess in random_word:
 for i in range(len(random_word)):
 if random_word[i] == guess:
 user_guess[i] = guess
 print("Correct guess! " + " ".join(user_guess))
 else:
 print("Incorrect guess.")
 if guess in vowels:
 guesses_remaining -= 2
 else:
 guesses_remaining -= 1

# Check if the user won or lost
if "-" not in user_guess:
 score = guesses_remaining * len(set(random_word))
 print("Congratulations! You guessed the word:", random_word)
 print("Your score:", score)
else:
 print("Sorry, you've run out of attempts. The word was:", random_word)
