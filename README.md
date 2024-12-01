
Student Grade Generator

This project provides a function in JavaScript to calculate the grade of a student based on their score. The function takes a score as input and returns the corresponding grade. The grading system is as follows:

	A > 79
	B - 60 to 79
	C - 59 to 49 
	D - 40 to 49
	E - less 40
	
1. Validates that the input score is between 0 and 100.
2. Returns "Invalid grade" for inputs outside the valid range.
3. Calculates the grade based on predefined ranges.


Function: gradeGenerator(score)
Input: A numeric score between 0 and 100.
Output: The corresponding grade (A, B, C, D, or E) or "Invalid grade" for inputs outside the range.

If score < 0 or score > 100, return "Invalid grade".
If score >= 80, return "A".
If score >= 60, return "B".
If score >= 50, return "C".
If score >= 40, return "D".
Otherwise, return "E".

	The code;
```javascript
function gradeGenerator(score) {

    if (score < 0 || score > 100) {
        return "Invalid grade";         // Check for invalid grade
    }

    // Determine grades
    if (score >= 80) {
        return "A";
    } else if (score >= 60) {
        return "B";
    } else if (score >= 50) {
        return "C";
    } else if (score >= 40) {
        return "D";
    } else {
        return "E"; // Covers scores less than 40
    }
}

// Test cases
console.log(gradeGenerator(89)); // Output: "A"
console.log(gradeGenerator(72)); // Output: "B"
console.log(gradeGenerator(42)); // Output: "D"
console.log(gradeGenerator(39)); // Output: "E"
