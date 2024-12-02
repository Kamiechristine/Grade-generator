## Function Description
function scoreEvaluator() {
    const points = ("Enter the student's marks (0 - 100):");
    const score = (points);

    if (score < 0 || score > 100 || (!score)) {
        console.log("Invalid input. Please enter a number between 0 and 100.");
    } else if (score > 79) {
        console.log("Grade: A");
    } else if (score >= 60) {
        console.log("Grade: B");
    } else if (score >= 49) {
        console.log("Grade: C");
    } else if (score >= 40) {
        console.log("Grade: D");
    } else {
        console.log("Grade: E");
    }
}
scoreEvaluator(50);

## Purpose
The purpose of this function is to:

Request the user to enter the marks of a student.
Validate the entered score to ensure it falls within the range of 0 to 100.
Assign a grade based on the score:
Grade A for scores above 79.
Grade B for scores between 60 and 79.
Grade C for scores between 49 and 59.
Grade D for scores between 40 and 48.
Grade E for scores below 40.
Provide error handling to notify the user when the input is invalid (e.g., entering a non-numeric value or a number outside the valid range).


## Parameters
points (string): A prompt or user input to request the student's marks.
score (number): The numeric value representing the student's score, which is validated before grading.

## Input Validation
Valid Inputs: The valid input is any numeric value between 0 and 100 (inclusive).

Invalid Inputs: If the input is not a number, or if it is outside the range of 0 to 100, the function will display an error message:


"Invalid input. Please enter a number between 0 and 100."
Note: The current version of the code is written in a way that seems to attempt to retrieve user input using a string assignment (const points = ("Enter the student's marks (0 - 100):");), but it does not actually request user input in its current state. For real-time user input, this part needs to be adapted to a method like prompt() in browsers or using Node.js functionality (like readline).

## Grading System
Grade A: Assigned when the score is greater than 79.
Grade B: Assigned when the score is between 60 and 79.
Grade C: Assigned when the score is between 49 and 59.
Grade D: Assigned when the score is between 40 and 48.
Grade E: Assigned when the score is 39 or below.

Example Usage
The following example demonstrates how the function works when called with different scores.


scoreEvaluator(85);  // Logs: Grade: A
scoreEvaluator(72);  // Logs: Grade: B
scoreEvaluator(56);  // Logs: Grade: C
scoreEvaluator(45);  // Logs: Grade: D
scoreEvaluator(30);  // Logs: Grade: E
scoreEvaluator("abc");  // Logs: Invalid input. Please enter a number between 0 and 100.
scoreEvaluator(150);  // Logs: Invalid input. Please enter a number between 0 and 100.


## Key Concepts
Input Validation:

The function ensures that the entered score is a valid number and within the range of 0 to 100. If the input is invalid (non-numeric or out of range), the function returns an error message.
Conditional Logic:

The function uses a series of if-else conditions to check the range of the score and assign the appropriate grade.
Handling Non-Numeric Inputs:

If the user enters a non-numeric value, the condition (!score) ensures that an error message is displayed.


## Potential Improvements
User Input via Prompt: The function as written does not actually request user input. For it to work as intended, you can replace the line const points = ("Enter the student's marks (0 - 100):"); with something like:


const points = prompt("Enter the student's marks (0 - 100):");
This would allow the function to work in a browser environment.

Grade Message Enhancement: Instead of just logging "Grade: A", the function could be enhanced to provide more detailed feedback, like "Excellent!" for grade A or "Needs Improvement" for grade E.

Repeated Prompt for Valid Input: Instead of just notifying the user once that the input is invalid, the function could repeatedly ask the user for valid input until they provide a valid score. This could be done by using a loop.

Handling Decimal Scores: The current function does not handle decimal scores (e.g., 85.5). To allow decimals, simply remove the integer validation or modify the logic to accept decimal values as well.

