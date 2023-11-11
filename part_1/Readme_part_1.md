Certainly! Here's a beginner's cheatsheet for Bash scripting in Ubuntu, with a focus on commands and examples:

### Bash Scripting Cheatsheet for Beginners

#### 1. **Shebang and Comments:**
   - Shebang: `#!/bin/bash`
   - Comments: `# This is a comment`

#### 2. **Variables:**
   - Declare and assign: `variable="Hello"`
   - Use variable: `echo $variable`

#### 3. **User Input:**
   - Read input: `read -p "Enter your name: " name`
   - Use input: `echo "Hello, $name"`

#### 4. **Conditions:**
   - if statement:
     ```bash
     if [ $a -gt $b ]; then
         echo "$a is greater than $b"
     fi
     ```
   - if-else statement:
     ```bash
     if [ $a -eq $b ]; then
         echo "$a is equal to $b"
     else
         echo "$a is not equal to $b"
     fi
     ```

#### 5. **Loops:**
   - For loop:
     ```bash
     for i in {1..5}; do
         echo "Iteration $i"
     done
     ```
   - While loop:
     ```bash
     count=0
     while [ $count -lt 5 ]; do
         echo "Count is $count"
         ((count++))
     done
     ```

#### 6. **Functions:**
   ```bash
   greet() {
       echo "Hello, $1!"
   }

   greet "John"
   ```

#### 7. **String Manipulation:**
   - Concatenation:
     ```bash
     str1="Hello"
     str2="World"
     result="$str1 $str2"
     echo $result
     ```
   - Substring:
     ```bash
     str="HelloWorld"
     echo ${str:0:5}  # Output: Hello
     ```

#### 8. **File Operations:**
   - Check if a file exists:
     ```bash
     if [ -e file.txt ]; then
         echo "File exists"
     fi
     ```
   - Reading from a file:
     ```bash
     while IFS= read -r line; do
         echo "Line: $line"
     done < file.txt
     ```

#### 9. **Command Substitution:**
   - Capture command output:
     ```bash
     current_date=$(date +%Y-%m-%d)
     echo "Current date is $current_date"
     ```

#### 10. **Arrays:**
   - Declare an array:
     ```bash
     fruits=("Apple" "Orange" "Banana")
     ```
   - Access elements:
     ```bash
     echo ${fruits[0]}  # Output: Apple
     ```

Feel free to modify and expand upon these examples as you explore more in Bash scripting!
