cli-scavenger-hunt.md



### Command Line Scavenger Hunt

- Create a scavenger hunt with 4-5 clues similar to the one described here using commands you learned this week and/or ones you already knew.
- Obviously, like this but without the answers :-)
- We'll check in at 10 min, hopefully groups are ready to trade
- Trade with another group.
- Go hunting!


**Setup:**
Create a directory structure with several subdirectories and files. Some files should contain clues and instructions for the next steps. Here's an example structure:

```
/scavenger_hunt
├── clue1.txt
├── clue2
│   └── clue2.txt
├── clue3
│   ├── hidden_clue.txt
│   └── next_step.txt
└── final_clue.txt
```

**Content of Clues:**
Each clue file should contain a simple task or command that students need to execute to find the next clue. 

**Clue 1:**
   - **File:** `/scavenger_hunt/clue1.txt`
   - **Content:**
     ```
     Welcome to the Command Line Scavenger Hunt!
     Your first task is to list all files in this directory.
     What's the name of the subdirectory? Go there to find the next clue.
     ```
   - **Expected Command:** `ls`

4. **Clue 2:**
   - **File:** `/scavenger_hunt/clue2/clue2.txt`
   - **Content:**
     ```
     Great job! Now use the command to print the current directory.
     Write down the path and proceed to the 'clue3' directory.
     ```
   - **Expected Command:** `pwd`

5. **Clue 3:**
   - **File:** `/scavenger_hunt/clue3/next_step.txt`
   - **Content:**
     ```
     Almost there! There's a hidden file in this directory.
     Use the command to list all files, including hidden ones, to find it.
     ```
   - **Expected Command:** `ls -a`
   - **Hidden File:** `/scavenger_hunt/clue3/.hidden_clue.txt`

6. **Final Clue:**
   - **File:** `/scavenger_hunt/final_clue.txt`
   - **Content:**
     ```
     Congratulations! You've reached the final clue.
     Use the command to display the contents of this file and celebrate your success!
     ```
   - **Expected Command:** `cat final_clue.txt`

