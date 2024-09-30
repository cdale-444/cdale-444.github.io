```mermaid
flowchart TD
    Start([Start]) --> |Generate Random Number| Generate[Generate Random Number]
    Generate --> |Prompt User for Guess| Input[User Input]
    Input --> |Validate Input| Validation{Is Input Valid?}
    Validation --> |Yes| Check[Check Guess]
    Validation --> |No| Error[Display Error Message]
    Error --> Input
    Check --> |Correct| Correct[Display Correct Message]
    Check --> |Too High| High[Display Too High Message]
    Check --> |Too Low| Low[Display Too Low Message]
    High --> Input
    Low --> Input
    Correct --> End([End])
