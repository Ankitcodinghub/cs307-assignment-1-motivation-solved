# cs307-assignment-1-motivation-solved
**TO GET THIS SOLUTION VISIT:** [CS307 Assignment 1-Motivation Solved](https://www.ankitcodinghub.com/product/cs307-programming-assignment-pa-1-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;109457&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS307 Assignment 1-Motivation Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
As Computer Scientists/Engineers, you will constantly learn about new tools. While Google is always helpful, if you are working with Unix systems, there is another great utility. The man command, which stands for manual files have information about many Unix commands, including their options and arguments. Whenever you feel unsure about a command, manual pages provides you a quick tour of learning/remembering.

However, man pages can be a bit overwhelming. There could be tens of options for a simple command with long and precise explanations. If you are interested in only one of these options, it can be difficult to locate that option in the man page. Here, grep comes to our rescue. grep allows us to get the specific lines that we are interested in. In general, grep command is used for finding text fragments in text files matching to provided input patterns.

Your task requires combining man and grep commands using Unix pipes. In Unix, commands can be combined by directing the output of first command

(which is normally printed to the console) to the input of the second command (which normally expects an input from the console). The user provides piped commands in the following form to the shell:

&lt; command1 &gt; | &lt; command2 &gt;

In this setting, command1 is executed first as a process. When it terminates, its output is directed to its child process as the input. Then, the child process executes command2 using this input.

For this assignment, you are expected to write a C program that simulates piped execution of man and grep commands on the shell. For this purpose you will use fork, wait and exec system calls we have seen in the lectures. In addition, you will need to learn and use pipe system call yourselves for piping the commands. Details about the program, command structure and system calls are provided in the following sections.

2 Problem Description

For this programming assignment, you are asked to implement execution of a shell command admitting the following pattern:

man &lt; command &gt; | grep &lt; option &gt; &gt; output.txt (1)

Here, command and option are variables you will determine as arguments to the man and grep commands, respectively. Once they are fixed and the above command (1) is executed on the shell, it prints lines in the manual page of the command that contain the string option to the output.txt. You have to be careful about how to interpret the option variable. It is not an option for the grep command. It should be an option of the command that grep accepts as the search pattern argument. Also, you must determine the number of lines the grep command will pick when it finds a matching string. For most options, the explanation in the man page spans multiple lines. So, you must obtain all of them.

Rules and explanations on how to choose values for command and option variables are explained in Section 3. After you fix these values, the piped command you will simulate will be determined. You are expected to implement your simulation in a single C file called pipeSim.c. Guides and details about the implementation are presented in Section 4.

3 Command Formation &amp; Argument Selection

Before implementing your simulation, you have to pick values for command and option variables.

Once you fix these variables, your shell command will be determined. In order to inform us about the command you are simulating, you must write the exact command in a file called command.txt. This file will contain a single line which is the command. The command will be approximately in the form of (1).

Your implementation might require adding more options to man or grep commands. For instance, if you enforce grep to take the next three lines after it finds a matching string, you must reflect it to the command in the command.txt as well.

While evaluating your submission, we will first execute the command in your command.txt in Bash, then compile and run your simulation program in Bash and lastly compare the results in both output.txt files.

While deciding on variables of the piped command, you should first fix the command variable. You can select one item from the list below. They are some of the most useful command-line utilities for Unix systems. You can look at their man page and use Google to determine which is the most interesting one for you. After fixing the command, you will select an option of the command. All the options of the command can be found under the man page of command.

• ls

• rm

• touch

• find

• grep

• df

• diff

• ping

• wget

• top

Example: Here is an example where we selected a command that is not in

the list

selected command: kill selected flag (option) for kill: -L command.txt:

man k i l l −extraOptions | grep ”−L” −extraOptions &gt; output . txt

1

Here, −extraOptions are again variables, you might want to use to make sure that your implementation exactly simulates the piped command.

In your submission, we expect to find a pdf file called report.pdf. In this file, you will explain what your command and option does, and why they attracted your attention. Here is an example:

k i l l command k i l l s ( terminates ) a process via sending

various signals to the Operating System . −L flag is for listing the available signals in a nice table .

I picked this command and option because . . .

1

2

3

4

3.1 Niche Problems &amp; Corner Cases

When you execute man kill | grep “-L”, it will not successfully grep ”-L” from kill command’s man page. The reason is, the character {-} is a special character, so the shell does not interpret this as a part of the search query. You have to solve this problem yourselves.

Again, let’s focus on the given example command man kill | grep “-L” for demonstration purposes. After you solve the special character problem, you will see that only the first line of the definition of flag -L will be displayed in the console as the output. The problem here is, actual definition was consisting of 2 lines.

actual definition:

-L, –table

List signal names in a nice table. grep result: -L, –table

Basically, the second line of the definition was ignored, since the second line was not including the string -L. We expect you to find a solution to this, and print all the necessary lines to output full definition. You do not have to automatically infer the number of lines you need. Once you decide on the command and option, you can look at the man page of the command, see how many lines the option description occupies and directly use this number in command.txt and your implementation.

4 C Program Implementation

In pipeSim.c file, you will implement the simulation of the piped command. In Chapter 5 of the OSTEP book, p3.c and p4.c are example command execution simulations of the shell. You should fully understand these programs and the chapter to understand the nature of the shell. Your implementation must agree with the structure of these programs.

Difference of your implementation from the examples in the book is that your implementation will simulate the execution of two commands that are connected. Similar to examples, each command must execute in a separate process. These processes must be descending from the initial process which will simulate the shell. The initial process should wait until the piped command finishes its execution as the shell would do. The shell process should not contain the bug we have seen in the lecture. It should not print to the console until all the processes descending from it terminate.

In order to implement your simulation as described, you must use fork, wait and exec system calls as in the examples. You should describe the process hierarchy generated by your program in your report (report.pdf).

In addition to these system calls, you have to utilize pipe system call for interprocess communication. Basically, pipe takes two file descriptors as input and connects the parent and child processes using these descriptors. The parent process’ descriptor is in the writing mode and the child’s descriptor is in reading mode. Using these descriptors, the parent can send its output to the child as the input. You can get more information about pipes on this page.

We want to ensure that your program allows correct interleaving of the processes. By correct interleaving we mean that the initial process that represents the shell should wait until all of subprocesses that execute commandsman and grep finish. Therefore, each process should print their process IDs to the console (not to any file). Only the shell process should print second time after the piped command execution finishes. Below is an example output in the console with correct print ordering:

I’m SHELL process, with PID: 38810 – Main command is: &lt;insert piped command here&gt;

I’m MAN process, with PID: 38811 – My command is: &lt;insert man command here&gt;

I’m GREP process, with PID: 38812 – My command is: &lt;insert grep command here&gt; I’m SHELL process, with PID:38810 – execution is completed, you can find the results in output.txt

5 Submission

The content of the zip file is as follows:

• command.txt: The piped command your program simulates. The command here will be used for evaluation.

• report.pdf: Your report that explains your choices on variables and process hierarchy of your program.

• pipeSim.c: Your C implementation.

• You don’t need to submit the generated output files (output.txt).

6 Grading

Some parts of the grading will be automated. If automated tests fail, your code will not be manually inspected for partial points. Some students might be randomly called for an oral exam to explain their implementations and reports.

Submissions will be graded over 100 points:

1. Compilation (10 pts): Your program compiles, runs and terminates without an error.

2. Process Hierarchy (20 pts): Process hierarchy described in your report represents correct shell simulation. Your description in the report must match with the reality (your C implementation).

3. Successful man (15 pts): Your command.txt contains just a man command without grep and the output of executing this command matches with the output of your implementation.

4. Successful piped command (40 pts): Your command.txt contains a piped command (both man and grep) and the output of executing this command matches with the output of your implementation.

5. Correct interleaving (20 pts): When your implementation is executed, lines printed to the console have the same order with the example execution presented at the end of Section 4.

6. Correct grep option (5 pts): Your implementation and the command in command.txt solves the special character problem described in Section 3.1.

7. Correct number of lines (5 pts): Your implementation and the command prints all the description lines for the given command, option pair as described in Section 3.1.

The first criterion is a precondition for all the other criteria. Similarly, the fourth item is a precondition for items 5, 6 and 7. It means that you will not get any credits from these items if you cannot get full credits from item 4. Items 3 and 4 are mutually exclusive. You can get points from only one.
