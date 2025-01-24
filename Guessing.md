```mermaid
flowchart TD
 Start([Start]) --> 
    A@{ shape: subproc, label: "IntegerSecretNumber" } -->
    B@{ shape: subproc, label: "IntegerUserGuess" } -->
    C@{ shape: subproc, label: "SecretNumber = Random (10)" } --> 
    D@{ shape: lean-r, label: "Output please enter a number between 0 and 9" } -->
    E@{ shape: lean-r, label: "Input UserGuess" } -->
    F@{ shape: hex, label: "UserGuess <> SecretNumber" } --> 
    F --> K{Is it?}
    G -->|Yes| C[OK]
    H --> D[Rethink]
    I --> B
    J ---->|No| -->
    K@{ shape: lean-r, label: "Output Correct. Thanks for playing" }
 E[End]
    






 End([End])
```




    

