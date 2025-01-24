```mermaid
flowchart TD
 Start([Start]) --> 
    A@{ shape: subproc, label: "IntegerSecretNumber" } -->
    B@{ shape: subproc, label: "IntegerUserGuess" } -->
    C@{ shape: subproc, label: "SecretNumber = Random (10)" } --> 
    D@{ shape: lean-r, label: "please enter a number between 0 and 9" } -->
    E@{ shape: lean-r, label: "Input UserGuess" } -->
    F@{ shape: hex, label: "UserGuess <> SecretNumber" }--> G{"UserGuess < SecretNumber"} -->
    H -- Yes --> I["too low"] -->N
    G{"UserGuess < SecretNumber"} -->K{"UserGuess > SecretNumber"} -->
    L -- Yes --> M["too high"] -->N
    F ---->|No| P[End]
   
    N@{ shape: lean-r, label: "Please enter a number between 0 and 9" } --> O@{ shape: lean-r, label: "Input UserGuess" } -->F
    P@{ shape: lean-r, label: "Correct. Thanks for playing" } -->

 End([End])
```
### step 1 input command for secret number
### Step 2 imput command for user guess
### Step 3 Generate number randomizer with a range from 0 to 10
### Step 4 Display text Please enter a number between 0 and 9
### Step 5 Input the user's guess
### Step 6 If they guess correctly go to step 10
### Step 7 If the user's guess is greater than the random number display Output too high, If the user's guess is less than the random number display Output too low.
### Step 8 If answered wrong redirect to please enter a number between 0 and 9
### Step 9 Loop continues untill user correctly guesses the number
### Step 10 If number is correctly guessed output Correct Thanks for playing.


    

