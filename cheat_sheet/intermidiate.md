Certainly! Here's an intermediate-level cheatsheet for Bash scripting in Ubuntu, with a focus on more advanced commands and concepts:

### Intermediate Bash Scripting Cheatsheet

#### 1. **Functions and Return Values:**
   ```bash
   calculate_sum() {
       echo $(($1 + $2))
   }

   result=$(calculate_sum 10 20)
   echo "Sum: $result"
   ```

#### 2. **Command Line Arguments:**
   ```bash
   #!/bin/bash
   echo "Script name: $0"
   echo "First argument: $1"
   echo "Second argument: $2"
   ```

#### 3. **Error Handling:**
   ```bash
   if [ ! -f file.txt ]; then
       echo "Error: File not found!"
       exit 1
   fi
   ```

#### 4. **Arrays and Iteration:**
   ```bash
   fruits=("Apple" "Orange" "Banana")

   for fruit in "${fruits[@]}"; do
       echo "Fruit: $fruit"
   done
   ```

#### 5. **Associative Arrays:**
   ```bash
   declare -A person
   person=( ["name"]="John" ["age"]=30 ["city"]="New York" )

   echo "Name: ${person['name']}, Age: ${person['age']}, City: ${person['city']}"
   ```

#### 6. **File Operations:**
   - Copy a file:
     ```bash
     cp source.txt destination.txt
     ```

   - Move/Rename a file:
     ```bash
     mv oldfile.txt newfile.txt
     ```

   - Delete a file:
     ```bash
     rm unwantedfile.txt
     ```

#### 7. **String Manipulation:**
   - Length of a string:
     ```bash
     str="Hello, World!"
     length=${#str}
     echo "Length: $length"
     ```

   - Search and replace:
     ```bash
     sentence="Bash is awesome."
     new_sentence=${sentence/awesome/great}
     echo "Modified: $new_sentence"
     ```

#### 8. **Advanced Conditionals:**
   - Logical AND:
     ```bash
     if [ $a -gt 10 ] && [ $b -lt 20 ]; then
         echo "Both conditions are true."
     fi
     ```

   - Logical OR:
     ```bash
     if [ $a -eq 0 ] || [ $b -eq 0 ]; then
         echo "At least one condition is true."
     fi
     ```

#### 9. **Reading and Writing to Files:**
   - Read file line by line:
     ```bash
     while IFS= read -r line; do
         echo "Line: $line"
     done < input.txt
     ```

   - Write to a file:
     ```bash
     echo "New content" > output.txt
     ```

#### 10. **Running Commands in the Background:**
   ```bash
   long_running_command &
   ```

#### 11. **Regular Expressions:**
   ```bash
   if [[ $string =~ ^[0-9]+$ ]]; then
       echo "String contains only digits."
   fi
   ```

#### 12. **Environment Variables:**
   - Display all environment variables:
     ```bash
     printenv
     ```

   - Access specific variable:
     ```bash
     echo "Home directory: $HOME"
     ```


