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


