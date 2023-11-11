### Advanced Bash Scripting Cheatsheet

#### 1. **Process Management:**
   - Running processes in the background:
     ```bash
     command &
     ```

   - List all running processes:
     ```bash
     ps aux
     ```

   - Killing a process by name:
     ```bash
     pkill process_name
     ```

#### 2. **Signal Handling:**
   - Trap signals:
     ```bash
     trap 'echo "Ctrl+C pressed"' SIGINT
     ```

#### 3. **Job Control:**
   - Managing jobs:
     ```bash
     jobs
     ```

   - Bring a job to the foreground:
     ```bash
     fg %1
     ```

   - Send a job to the background:
     ```bash
     bg %1
     ```

#### 4. **Advanced File Operations:**
   - File descriptor redirection:
     ```bash
     command 2> error.log
     ```

   - Process substitution:
     ```bash
     diff <(command1) <(command2)
     ```

   - Check if a file is readable, writable, and executable:
     ```bash
     if [ -r file.txt ] && [ -w file.txt ] && [ -x file.txt ]; then
         echo "File is readable, writable, and executable."
     fi
     ```

#### 5. **Advanced String Manipulation:**
   - Regular expression matching:
     ```bash
     if [[ $string =~ ^[0-9]+$ ]]; then
         echo "String contains only digits."
     fi
     ```

   - Extracting substring using regex:
     ```bash
     string="This is a sentence."
     if [[ $string =~ ([a-z]+) ]]; then
         echo "Matched: ${BASH_REMATCH[1]}"
     fi
     ```

#### 6. **Error Handling and Logging:**
   - Logging to a file:
     ```bash
     echo "Log message" >> logfile.txt
     ```

   - Logging errors to syslog:
     ```bash
     logger "An error occurred."
     ```

#### 7. **Networking:**
   - Fetching external data (e.g., JSON from an API):
     ```bash
     curl -s https://api.example.com/data.json
     ```

   - Checking internet connectivity:
     ```bash
     ping -c 1 google.com && echo "Internet is reachable" || echo "Internet is not reachable"
     ```

#### 8. **Advanced Arrays:**
   - Multidimensional arrays:
     ```bash
     matrix=( [0,0]=1 [0,1]=2 [1,0]=3 [1,1]=4 )
     echo "Value at [1,0]: ${matrix[1,0]}"
     ```

#### 9. **Advanced Control Flow:**
   - Selective command execution:
     ```bash
     condition && command_if_true || command_if_false
     ```

   - Short-circuiting with `&&` and `||`:
     ```bash
     [ -d directory ] && echo "Directory exists" || echo "Directory does not exist"
     ```

#### 10. **Advanced Functions:**
   - Recursive functions:
     ```bash
     factorial() {
         if [ $1 -le 1 ]; then
             echo 1
         else
             echo $(( $1 * $(factorial $(( $1 - 1 ))) ))
         fi
     }
     ```

#### 11. **Advanced Parameter Expansion:**
   - Default values:
     ```bash
     echo "Variable is not set or is empty: ${variable:-default}"
     ```

   - Use default if variable is unset:
     ```bash
     echo "Variable is unset: ${unset_variable:=default}"
     ```


