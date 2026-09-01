# 01 flowchart test

## MC 

1. A condition block has usually how many flowlines going out of it?

   1. One, representing the next step.
   1. Two, for the "true" and "false"
   1. Three, for the "true", "false", and "unknown"
   1. It depends on the number of variables defined in the condition

1. If we want to input two variables and output their sum in a flowchart, which of the following to we typically use?

   1. Variable
   1. Condition
   1. Process
   1. Terminal 

1. You're asked to design a flowchart for this process: "You are cutting a piece of string with length `string_length` into equal pieces of `piece_length`. Output `piece_count`, how many pieces you can cut.".

   ```mermaid
   flowchart LR
    Start([Start])
    Input[/Input string_length, piece_length/]
    Init[piece_count = 0]
    Cond{string_length >= piece_length?}
    Subtract[string_length = string_length - piece_length
    piece_count = piece_count + 1]
    Output[/Output piece_count/]
    End([End])

    Start --> Input
    Input --> Init
    Init --> Cond
    Cond -- true --> Subtract
    Subtract --> Cond
    Cond -- false --> Output
    Output --> End
   ```

   Which of the following statements is/are correct?
   
   1. The flowchart is wrong, because flowcharts cannot loop back to an earlier decision block.
   2. The flowchart is partially correct, because it outputs the (how many pieces you can cut)+1.
   3. The flowchart is correct.
   4. The flowchart is wrong, because `piece_count` must be defined in a condition to *decide* how many pieces (`piece_count`) we get. 
---

## Draw flowcharts:

1. You are preparing tea. Use no decisions.

   Boil water in a kettle. Put a tea bag into a cup. Pour the boiled water into the cup. Wait 3 minutes for the tea to steep. Remove the tea bag.

1. You are coding a keypad-based access control check for your dormitory door.

   Input 4 digits from the keypad one by one. Then compare it with `PIN`. If correct, unlock the door and output Access granted. Otherwise, keep the door locked and output Access denied and go back.

1. You are programming an automated plant-watering system that checks on the garden once per day, indefinitely.

   As long as there is a next day, do the following:
   
   - Input `soil_moisture` and `is_daytime`.
     - If it is daytime:
         - If soil_moisture is below 30, turn on the watering pump for 5 minutes.
         - Otherwise, do not water.
     - Otherwise (nighttime), keep the pump off and skip the moisture check entirely.
   - Move on to the next day.
