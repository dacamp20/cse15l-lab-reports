# Lab Report 4


For each numbered step starting from when you log in, so steps 4-9, take a screenshot, and write down exactly which keys you pressed to get to that step. For special characters like <enter> or <tab>, write them in angle brackets with code formatting. Then, summarize the commands you ran and what the effect of those keypresses were.

**Step 4: Log into ieng6**

Screenshot:

![Image](https://github.com/dacamp20/cse15l-lab-reports/blob/main/s4.jpg?raw=true)

Keys pressed: `<up><enter>` `<up><up><enter>`

Explanation: The `ssh dacampuzano@ieng6.ucsd.edu` was one up in the search history. Then the `cs15lwi24` was two up in the search history so I accessed them using the `<up>` and `<enter>` keys.


**Step 5: Clone your fork of the repository from your Github account**

Screenshot:

![Image](https://github.com/dacamp20/cse15l-lab-reports/blob/main/s5.jpg?raw=true)

Keys pressed: `git clone <Ctrl-v>` `ls` `cd l<tab>` `ls`

Explanation: I copied the ssh url from my fork of the repository and used `Ctrl-v` keys to paste it into the command line. Then I use `ls` to view if it was added properly then I changed my directory to `lab7` using `l<tab>` to auto complete the `lab7` directory I was serching for. Finally I used `ls` again to view the `test.sh` file is there with the rest of the files.


**Step 6: Run the tests, demonstrating that they fail**

Screenshot:

![Image](https://github.com/dacamp20/cse15l-lab-reports/blob/main/s6.jpg?raw=true)

Keys pressed: `bash t<tab>`

Explanation: I ran the bash script using `t<tab>` to auto complete the `test.sh` file that I wanted to run.


**Step 7: Edit the code file to fix the failing test**

Screenshot:

![Image](https://github.com/dacamp20/cse15l-lab-reports/blob/main/s7.1.jpg?raw=true)
![Image](https://github.com/dacamp20/cse15l-lab-reports/blob/main/s7.2.jpg?raw=true)

Keys pressed: `vim L<tab>.java` `44<shift>g` `e` `x` `i` `2` `Esc` `<shift>;wq`

Explanation: I use `vim L<tab>.java` to auto complete the `ListExamples.java` file. Then I use `44<shift>g` to access the 44th line of the code that contains the error. Then I use `e` to get to the last character of the first word which is `index1`. Then I use the `x` key to delete the last charcter of the word, which is 1. Then I used the `i` key to go into insert mode. Then I type in `2` to fix the error. Then I use `Esc` to exit insert mode. Finally I use the `<shift>;wq` keys to enter `:wq` to save and quit.


**Step 8: Run the tests, demonstrating that they now succeed**

Screenshot:

![Image](https://github.com/dacamp20/cse15l-lab-reports/blob/main/s8.jpg?raw=true)

Keys pressed: `bash t<tab>`

Explanation: I ran the bash script again using `t<tab>` to auto complete the `test.sh` file that I wanted to run.


**Step 9: Commit and push the resulting change to your Github account**

Screenshot:

![Image](https://github.com/dacamp20/cse15l-lab-reports/blob/main/s9.1.jpg?raw=true)
![Image](https://github.com/dacamp20/cse15l-lab-reports/blob/main/s9.2.jpg?raw=true)

Keys pressed: `git add .` `git commit -m "updated"` `git push`

Explanation: I use the `git add .` keys to add all my changes from my current directory to the staging area. Then I used the `git commit -m "updated"` keys to create a new commit with the changes in my staging area along with a commit message of "updated". Finally I use the `git push` keys to push and upload my commited changes from my local repository to the remote repository on GitHub.

---
