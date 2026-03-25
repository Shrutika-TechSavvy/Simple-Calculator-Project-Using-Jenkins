# Jenkins + GitHub Calculator Project

So basically, in this project, I tried to understand how Jenkins actually works with GitHub in a simple way, instead of jumping directly into complex pipelines.

At first, I created a basic calculator script (calculator.sh) and uploaded it to my repository on GitHub. The idea was simple — just perform a few arithmetic operations like addition, subtraction, multiplication, and division.

Then I moved to Jenkins and created a new freestyle project. After that, I connected Jenkins to my GitHub repository by providing the repository URL. This step is really important because Jenkins doesn’t store code on its own — it always pulls the latest code from GitHub.

Once the connection was set, I added a Build Step using “Execute Shell”. Honestly, this part is where things started making sense
Here, I gave Jenkins two commands:

 - chmod +x calculator.sh → to make the script executable
 - ./calculator.sh → to actually run the script

Without this, Jenkins would just download the code and sit idle, not doing anything.

After saving everything, I clicked on Build Now. At this point, Jenkins started doing its job in the background:

It cloned the repository from GitHub
Checked out the latest code from the main branch
Executed the shell script
Displayed the output in the console

And finally, I got this output:

Addition: 15
Subtraction: 5
Multiplication: 50
Division: 2
Finished: SUCCESS

Seeing Finished: SUCCESS was actually satisfying because it confirmed that everything—from GitHub
<img width="1777" height="883" alt="image" src="https://github.com/user-attachments/assets/c27e4a45-a585-45f3-9fee-f9ae4a9048b0" />


Now,I did few changes in the calculator.sh and jenkins build now shows output :
<img width="1803" height="680" alt="image" src="https://github.com/user-attachments/assets/b45fe446-cd89-49c6-8502-9c9371559763" />
<img width="1796" height="861" alt="image" src="https://github.com/user-attachments/assets/70c91c2a-e6db-401a-b9f1-e02188bf214d" />

