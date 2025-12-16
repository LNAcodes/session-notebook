# JavaScript Basics & Variables – Session Notes

## 1. JavaScript Overview

JavaScript is a programming language originally for browsers; can also run in Node.js (terminal).
Browser JS → interacts with websites
Node.js JS → runs in terminal/console
Programs are executed sequentially (line by line).
Syntax must be precise; computers do not forgive errors.

Console Output
jsconsole.log("Hello World!");
console.clear(); // clears the console
console.error("Error!"); // logs an error

## 2. Variables
Declaration

const → value cannot be changed (preferred)
let → value can be reassigned
var → outdated, avoid

Assignment
= stores the value on the right into the variable on the left
jsconst aNumber = 42;
let counter = 0;
counter = counter + 1; // increments counter
Naming

Use camelCase: monthlyContribution
Be specific: totalSavings better than counter
Longer descriptive names are better than short ones

Data Types

string → "abc"
number → 1234
boolean → true / false
null → nothing
undefined → not set
BigInt / Symbol → less common

## 3. Math & Operators

+ → add numbers or concatenate strings
-, *, /, ** → standard arithmetic
% → remainder (useful for clocks, even/odd checks)

Increment/Decrement
jscount++  // +1
count--  // -1
count += 6  // add 6
Operator precedence: multiply/divide before add/subtract

## 4. Handling Input in Node.js
process.argv is an array of terminal arguments:
bashnode index.js 30
jsconst currentAge = Number(process.argv[2]);

process.argv[2] → first user input
Number() → converts string input to a number
Do not change this line; enter the number in terminal

## 5. Typical Challenges & Learnings
Tip Calculator

Convert percentage correctly (0.1 for 10%)
totalCost = mealCost + tipAmount (not multiplied!)
Takeaway: small errors in formula lead to wrong results; check math carefully

Circle Area & Circumference

Use Math.PI and exponentiation ** for area
Clear console output
Takeaway: separate calculation from output, use descriptive variable names

Lifetime Calculator

Input from process.argv makes program flexible
Each calculation requires its own variable:

total days lived
remaining days
percentage of life
sleeping days


Hurdle: translating text requirements into formulas; think in plain language first
Takeaway: step-by-step reasoning helps more than copying formulas

## 6. Common Hurdles for Beginners

Confusion between variables vs. strings in console.log
Forgetting Number() when using terminal input
Misunderstanding operator precedence
Feeling pressured by other students' speed – progress is individual
Isolated challenges make it hard to see connections (practice multiple tasks to see patterns)

## 7. Key Takeaways

Learn through doing, not just reading or watching videos
Always name variables descriptively
Keep calculations separate from console output
Start with plain-language pseudocode before writing JS
Understand input → calculation → output workflow
Repetition = learning; gradual understanding builds confidence
GitHub visibility ≠ learning quality – focus on comprehension

## 8. Tips for Practicing

Start small: one variable, one calculation, one output
Check your results in the console step by step
Use feature branches for each challenge to keep main stable
Experiment with terminal input via process.argv for interactive scripts
Reflect on why formulas work, not just how to type them

## 9. Mental Notes

Mistakes are expected and useful
If overwhelmed: pause, simplify, write pseudocode
Progress is cumulative – today's challenges build tomorrow's understanding
