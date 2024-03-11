# Lab Report 5

**Part 1:**

---

Original Post from Student:

Title: Need help debugging infinite loop in Java program

Hello everyone, 
I'm encountering an issue with my Java program for the Software Tools and Techniques course. I'm getting stuck in an infinite loop, and I'm not sure why. I've attached a screenshot below showing the output I'm getting.

Symptom:

When I run my program, it seems to be stuck in a loop, printing the message that it compiled successfully and is runnnig the program without stopping.

Description of Bug:

My guess is that there might be an issue with the condition in my loop, but I'm not entirely sure. It's possible that the loop condition is never being satisfied, causing it to run indefinitely.

Here's the screenshot of the output:

![Image](https://github.com/dacamp20/cse15l-lab-reports/blob/main/lr5-3.jpg?raw=true) 

---

Response from TA:

Hi there,

Thanks for reaching out! It sounds like you might indeed be encountering an issue with your loop condition. Have you tried adding some print statements inside the loop to see what's happening?

Additionally, you might want to try running your program with a debugger to step through the code and see where it's getting stuck.

---

Student's Follow-Up Post:

Title: Re: Need help debugging infinite loop in Java program

Hi everyone,

Thanks for the suggestions! I added some print statements inside my loop, and I think I've identified the issue.

Terminal Output After Adding Print Statements:

![Image](https://github.com/dacamp20/cse15l-lab-reports/blob/main/lr5-1.jpg?raw=true)

Description of Bug:

It looks like my loop condition is never being satisfied, causing the program to get stuck in an infinite loop. Specifically, the variable I'm using to control the loop is not being updated correctly within the loop body.

I'll need to fix this by ensuring that the loop variable is properly updated so that the loop can terminate when it should. Thanks for pointing me in the right direction!

---

Setup Information:

File & Directory Structure:

Main.java

run.sh

Contents of Main.java Before Fixing the Bug:

![Image](https://github.com/dacamp20/cse15l-lab-reports/blob/main/lr5-4.jpg?raw=true)

Contents of run.sh:

![Image](https://github.com/dacamp20/cse15l-lab-reports/blob/main/lr5-2.jpg?raw=true)

Full Command Line to Trigger the Bug:

`bash run.sh`

Description of What to Edit to Fix the Bug:

In the Main.java file, make sure to update the count variable inside the loop to prevent an infinite loop. Add count++ or any appropriate update statement inside the loop body to ensure that the loop condition eventually becomes false and the loop terminates.

---

**Part 2:**
One of the most valuable things I learned in the second part of this quarter was how to use the Java debugger, JDB, to analyze and debug code effectively. It allowed me to step through my Java programs, inspect variables, and identify the root causes of bugs more efficiently. Additionally, crafting Bash scripts to automate routine processes introduced me to the power of scripting, enhancing my understanding of shell programming and its practical applications in software development.

---
