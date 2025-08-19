import time
name = input("What is your name?")
print ("Hello, " + name, "TIme to play Hangman!")
print (" ")
time.sleep(1)
print ("Start guessing...")
time.sleep(0.5)
word = "Cricket"
guesses = ''
turns = 10
while turns > 0:
    failed = 0
    for char in word:
        if char in guesses:
            print (char)
        else:
            print( "_")
            failed += 1
    if failed == 0:
        print ("You Won")
        break
    guess = input("guess a character:")
    guesses += guess
    if guess not in word:
        turns -= 1
        print ("Wrong")
        print ("You have",+ turns, 'more guesses' )
    if turns == 0:
        print ("You lose")
