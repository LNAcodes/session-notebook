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


# JavaScript DOM & Events – Session Notes

## 1. Connecting JavaScript to HTML

```html
<script src="./js/index.js" defer></script>
```
## 2. The DOM (Document Object Model)

The DOM represents the HTML document as JavaScript objects

Accessible via the global document object

```
document;
document.body;
document.head;

```
## 3. Selecting Elements (querySelector)

Best practice: use data-* attributes for JavaScript.

```
const button = document.querySelector('[data-js="add"]');
```
Other possible selectors:
```
".class"
"#id"
"tag"
```
Rule:

Classes → CSS

data-* attributes → JavaScript

## 5. Working with Classes (classList)
```
element.classList.add("dark");
element.classList.remove("dark");
element.classList.toggle("dark");
```
## 6. Calculator Challenge – Key Learnings
Mathematical Operations
```
addButton.addEventListener("click", () => {
  const result = operand1 + operand2;
  console.log(result);
});
```
Operators:
+ add
- subtract
* multiply
/ divide
** exponent
% modulo

Updating Values

If a variable changes, it must be declared with let.

```
let operand1 = 12;
```

## 7. Dark Mode Challenge – Key Learnings

Dark mode is controlled by the dark class on <body>.
```
document.body.classList.add("dark");
document.body.classList.remove("dark");
document.body.classList.toggle("dark");
```

## 8. Personal Stolperfallen & Lessons Learned
8.1 Exact Naming Matters

subtract ≠ substract

JavaScript is case-sensitive

8.2 data-js Must Match HTML Exactly

HTML:
```
data-js="toggle-button"
```
JavaScript:
```
'[data-js="toggle-button"]'
```
8.3 const vs let

const → value cannot change

let → value can change

Rule:

If the value changes later → use let

8.4 Toggle Means Toggle

Correct:
```
classList.toggle("dark");
```
Wrong:
```
classList.add("toggle");
```
8.5 Debugging Workflow

Check selectors first

Use console.log() to inspect values

Test one event listener at a time

## 9. Mental Model

HTML provides structure
data-js connects JavaScript to HTML
Events trigger logic
Logic updates values or classes
CSS reacts to class changes

# Before Coding Checklist (JavaScript DOM)

## Before Writing Code
- [ ] Read the HTML first
- [ ] Identify all `data-js` attributes
- [ ] Decide which variables need `let` vs `const`
- [ ] Name variables clearly (e.g. `addButton`, not `btn1`)

## While Coding
- [ ] Select elements with `querySelector`
- [ ] Add one `addEventListener` at a time
- [ ] Use `console.log()` to verify behavior
- [ ] Test in DevTools after each step

## If Something Does Not Work
- [ ] Check `data-js` spelling
- [ ] Check variable names
- [ ] Check event type (`"click"`)
- [ ] Check `classList.add/remove/toggle`
- [ ] Look for console errors first

## Final Check
- [ ] Code is readable
- [ ] No unused variables
- [ ] Behavior matches the task description
