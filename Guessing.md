```mermaid
flowchart TD
    Start([Start]) --> DeclareVariables[/Declare Integer SecretNumber, UserGuess/]
    DeclareVariables --> GenerateSecretNumber[/Generate SecretNumber = Random(10)/]
    GenerateSecretNumber --> PromptUser([Output: "Please enter a number between 0 and 9"])
    PromptUser --> GetUserInput[/Input: UserGuess/]
    
    GetUserInput --> CheckEquality{Is UserGuess == SecretNumber?}
    CheckEquality -- Yes --> CorrectGuess([Output: "Correct. Thanks for playing"])
    CorrectGuess --> End([End])
    
    CheckEquality -- No --> CheckTooLow{Is UserGuess < SecretNumber?}
    CheckTooLow -- Yes --> OutputTooLow([Output: "Too low"])
    CheckTooLow -- No --> OutputTooHigh([Output: "Too high"])
    
    OutputTooLow --> Reprompt([Output: "Please enter a number between 0 and 9"])
    OutputTooHigh --> Reprompt
    Reprompt --> GetUserInput
End([End])```



    

