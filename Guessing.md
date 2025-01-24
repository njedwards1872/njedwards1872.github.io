```mermaid
flowchart TD
 Start([Start]) --> 
    A@{ shape: subproc, label: "IntegerSecretNumber" } -->
    B@{ shape: subproc, label: "IntegerUserGuess" } -->
    C@{ shape: subproc, label: "SecretNumber = Random (10)" } --> 
    D@{ shape: lean-r, label: "Output please enter a number between 0 and 9" } -->
    E@{ shape: lean-r, label: "Input UserGuess" } -->
    F@{ shape: hex, label: "UserGuess <> SecretNumber" } -->  G{"UserGuess < SecretNumber"} -->
    H -- Yes --> I["Output too low"]
    G{"UserGuess < SecretNumber"} -->K{"UserGuess > SecretNumber"} -->
    L -- Yes --> M["Output too high"]
    
 End([End])
```




    

