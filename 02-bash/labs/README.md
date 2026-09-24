# Bash Battle Arena : Level 1

## Objective:

Create a directory named "Arena" and then inside it, create three files: warrior.txt, mage.txt, and archer.txt. List the contents of the Arena directory.

## Commands used

mkdir Arena

cd Arena

touch warrior.txt mage.txt archer.txt 

ls

## Output

<img width="304" height="226" alt="image" src="https://github.com/user-attachments/assets/a762a7b8-5666-41ad-ae56-fcc470c19cae" />

# Bash Battle Arena : Level 2 (Variables and Loops)

## Mission:

Create a script that outputs the numbers 1 to 10, one number per line.

## Commands used
```bash
vim one-to-ten.sh

chmod +x one-to-ten.sh

./one-to-ten.sh
```
## Script
```bash
#!/bin/bash

for (( i=1; i<=10; i++ ))
do
        echo "Number: $i
done
```
## Output: 

<img width="265" height="200" alt="image" src="https://github.com/user-attachments/assets/c84f28ba-2b18-41da-8f8d-d7b17b0f1025" />

# Bash Battle Arena : Level 3 (Conditional statements)

## Mission:

Write a script that checks if a file named hero.txt exists in the Arena directory. If it does, print Hero found!; otherwise, print Hero missing!.

## Commands used
```bash
vim fine-hero.sh
chmod +x find-hero.sh
./find-hero.sh

```
## Script
```bash
#!/bin/bash
if [ -f /home/omar/Arena/hero.txt ]; then

        echo "Hero Found ! "

else
        echo "Hero Missing !"
fi

```
## Output: 

<img width="194" height="47" alt="image" src="https://github.com/user-attachments/assets/c7cf12fe-8deb-4869-a6c1-c934290a6f8a" />


# Bash Battle Arena - Level 4: File Manipulation
Mission: Create a script that copies all .txt files from the Arena directory to a new directory called Backup.

## Commands used :
mkdir Backup
vim manipulate.sh
chmod +x  manipulate.sh
./manipulate.sh

## Script :
```bash
#!/bin/bash

mkdir -p Backup

cp ~/Arena/*.txt ~/Backup/

```
Output:

<img width="672" height="127" alt="image" src="https://github.com/user-attachments/assets/8eca250e-6ebe-4372-bd8d-8e9799a71df8" />

# Bash Battle Arena : Level 5: The Boss Battle - Combining Basics
Mission: Combine what you've learned! Write a script that:

1. Creates a directory names 'Battlefield'
2. Inside Battlefield, create files named knight.txt, sorcerer.txt, and rogue.txt.
3. Check if knight.txt exists; if it does, move it to a new directory called Archive.
4. List the contents of both Battlefield and Archive.

Script:
```bash

#!/bin/bash

mkdir -p Battlefield

touch "Battlefield/knight.txt"

touch "Battlefield/sorcerer.txt"

touch "Battlefield/rogue.txt"

mkdir -p Archive


if [ -f "Battlefield/knight.txt" ]; then
        mv "Battlefield/knight.txt" "Archive"
        echo "File moved successfully"
fi


ls Battlefield Archive

```
## Output:

<img width="631" height="168" alt="image" src="https://github.com/user-attachments/assets/20cf676d-4420-432c-82c2-8d995ce8c8e8" />


# Challenge 1: Basic Arithmetic Calculator

Create a script that takes two numbers as input and performs basic arithmetic operations (addition, subtraction, multiplication, division).

Requirements:
-Prompt user for two numbers
-Perform all four operations
-Display the results
-Handle division by zero

## Commands used
```bash
vim ari-calc.sh
chmod +x ari-calc.sh
./ari-calc.sh
```
## Script
```bash
#!/bin/bash

read -p "Enter the first number: " num1

read -p "Enter the second number: " num2

echo "$num1 + $num2= $((num1 + num2))"
echo "$num1 - $num2= $((num1 - num2))"
echo "$num1 × $num2= $((num1 * num2))"

if  [ "$num2" -ne 0 ]; then
    echo "$num1 ÷ $num2= $((num1 / num2))"
else
    echo "Division: Cannot divide by zero"
fi
```
Output:

<img width="650" height="173" alt="image" src="https://github.com/user-attachments/assets/7c3a792e-7693-4f77-af3e-3956ce48ec59" />
<img width="687" height="169" alt="image" src="https://github.com/user-attachments/assets/784b55ae-d77c-4e39-a329-51d8970ed4f6" />


## Challenge 2: File Operations Script
Create a script that automates directory and file creation.

Requirements:
-Create a directory called bash_demo
-Navigate into the directory
-Create a file called demo.txt
-Write text to the file (include current date)
-Display the file contents

-Example output:

-Directory 'bash_demo' created. File 'demo.txt' created.

-File contents: This file was created by a Bash script on 2024-11-29

## Commands used
```bash
❯ vim ops.sh
❯ chmod +x ops.sh
❯ ./ops.sh

```
## Script
```bash
#!/bin/bash

mkdir bash_demo

touch bash_demo/demo.txt

echo "This file was created by a Bash script on 2026-09-23" > bash_demo/demo.txt

echo "Directory 'bash_demo' created. File 'demo.txt' created."

cat demo.txt

```

Output

<img width="358" height="120" alt="image" src="https://github.com/user-attachments/assets/971f06ac-e2f0-4c2f-b9eb-d70cab35906d" />

# Challenge 3: File Checker with Permissions

Create a script that checks if a file exists and displays its permissions.

Requirements:
Prompt user for a filename
Check if the file exists
If it exists, check if it's readable, writable, and executable
Display appropriate messages for each permission

## Commands used :
vim checker.sh
chmod +x checker.sh
./checker.sh

```
## Script
```bash
#!/bin/bash

read -p "What is the file name you are searching for?" $file

if [ -f $file ]; then
        echo "File exists"
else
        echo "File does not exist"
fi


if [ -r "$file" ]; then
    echo "Readable"
else
        echo "File unreadable"
fi

if [ -w "$file" ]; then
        echo "Writable"
else
        echo "Unwritable"
fi

if [ -x "$file" ]; then
    echo "Executable"
else
        echo "Not executable"
fi

```


## Output :

<img width="622" height="145" alt="image" src="https://github.com/user-attachments/assets/721607e0-333a-4f27-8072-f5ee147d9be3" />

