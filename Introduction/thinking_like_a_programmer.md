# 🌟 Thinking Like a Programmer.

**The hardest thing to learn about programming is not the syntax but how to apply it to solve real world problems.**
**Thinking like a programmer involves looking at descriptions of what your program needs to do, workout what code features are needed to achieve those things, and making all that work together.**

**_I want you to create a simple "guess the number" type game. It should choose a random number between 1 and 100, then challenge the player to guess the number in 10 turns. After each turn, the player should be told if they are right or wrong, and if they are wrong, whether the guess was too low or too high. It should also tell the player what numbers they previously guessed. The game will end once the player guesses correctly, or once they run out of turns. When the game ends, the player should be given an option to start playing again._**

## 🎯 **1. Core Requirementspp**

### 1. Generate Random Number

- #### Generate a random Number between 1 and 100 for the player to guess

**2. Game loop**

- #### Allow the player 10 entries to guess a number untill the correct entry

- #### Give feedback after an enrty, - if the entry is correct, congradulate the player and end the game - if the entry is incorrect tell the player if the guess is too high or too low

- #### Keep track of the players guess and display them after every turn

**3. Game end**

- #### Game ends after the player has exceeded the 10 turns without finding the correct guess, end the game and display the correct answer or if he/she finds the correct guess . Add play again option

**4. Play again option**

- #### After the game ends, allow the player to play again by restarting the state of the game.

## 🛠️ **2. Input and Output**

**1.Input option**

- #### The players guess

**2. Output option**

- #### Feedback after each guessing attempt

- #### List of Previous guesses

- #### Game feedback win/loose

## ⏳ **3. Game logic**

**1. Initialise Game**

- #### Generate a number between 1 and 100
- #### initialise the turns to 0
- #### Clear Previous guesses

**2. Game loop**

- #### Prompt the player for a guess
- #### Validate the guess tob ebetween 1-100
- #### Compare the guess to the random number
- #### If correct end the game and congradulate the player
- #### if incorrect provide feedback and add the guess to the guess list

**3. Game end**

- #### Display the game feedback , win/loose
- #### Display option to play again

## 🚀 **4. Technical consideration**

**1. Random Number Generation**

- #### Use `Math.random() Math.floor()` to generate a random number between 1 and 100

**2. Input Validation**

- #### Ensure the player input s avalid number between 1 and 100

**3. Tracking previous Guess**

- #### use an array to stpore the player's guesses and display them after each turn

**4. Game state management**

- #### use varriables to track the random number, number of turms, and a list of previous guesses.

**5. Play again option**

- #### Use a loop or a recursive function if the player choses an option to play again
