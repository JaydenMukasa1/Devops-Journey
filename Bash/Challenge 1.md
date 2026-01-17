## Challenge 1: Arithmetic Calculator

Create a script that takes two numbers as input and performs basic arithmetic operations (addition, subtraction, multiplication, division).

---

### Requirements
- Prompt user for two numbers
- Perform all four operations
- Display the results
- Handle division by zero

---

### Solution

```bash
echo "Please input two numbers"

read number1
read number2

addition_sum=$((number1 + number2))
subtraction_sum=$((number1 - number2))
multiplication_sum=$((number1 * number2))
division_sum=$((number1 / number2))

echo "$number1 + $number2 = $addition_sum"
echo "$number1 - $number2 = $subtraction_sum"
echo "$number1 x $number2 = $multiplication_sum"
echo "$number1 ÷ $number2 = $division_sum"

