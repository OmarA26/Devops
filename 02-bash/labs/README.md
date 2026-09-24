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

## Challenge 1: Basic Arithmetic Calculator

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



