# Lab Report 5

I'm going to explore how I could have done the task for Lab Report 4 using a Bash script (or 2).

First, we need to create two new files: `Lab5.sh` that runs in your local context, and `SSHGradingScript.sh` that runs on the remote computer. This is because, through trial and error, I learned that when you log in through SSH on a local host's bash script, it doesn't run the rest of the bash script because the remote computer is running a distinct terminal from the one that your local bash script resides in.

We will first edit `SSH GradingScript.sh` to complete the majority of the task. 

5) **Clone your fork of the repository from your Github account**

Use `git clone git@github.com:SammyoRoy/lab7.git` to clone the fork.

6) **Run the tests, demonstrating that they fail**

Change directory into lab7 using `cd lab 7`. Then write the following lines to run the tests.
```
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
```
7) **Edit the code file to fix the failing test**

To edit the code file, we will use the `sed` command, which stands for stream editor and is capable of directly editing files.
`sed -i "43s/.*/index2 += 1;/" ListExamples.java`

This command uses the `sed` utility to perform an in-place edit (`-i`) on the file `ListExamples.java`.
The `sed` command searches for the 43rd line in the file (`43s/`) and replaces the entire line with the text `index2 += 1;`.

8) **Run the tests, demonstrating that they now succeed**

Run the tests again:
```
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
```

9) **Commit and push the resulting change to your Github account**

We can push the changes using the following commands:
```
git add ListExamples.java
git commit -m fixed
git push
```

In summary, `SSHGradingScript.sh` should look like:
```
git clone git@github.com:SammyoRoy/lab7.git

cd lab7
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests

sed -i "43s/.*/index2 += 1;/" ListExamples.java

javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests

git add ListExamples.java
git commit -m fixed
git push
```

Next we will edit `Lab5.sh` to log into Ieng6 and to run `SSHGradingScript.sh`.
4) **Log into ieng6**
Write: `ssh cs15lwi23ams@ieng6.ucsd.edu bash SSHGradingScript.sh`

That's it for the two Bash scripts. However, we need to copy `SSHGradingScript.sh` onto our remote computer. To do so, open your terminal and execute the following command (make sure you're in the folder containing `SSHGradingScript.sh`):
`$ scp SSHGradingScript.sh cs15lwizzz@ieng6.ucsd.edu:`
This copies `SSHGradingScript.sh` into the home directory of the remote computer. 

And we're done! When we want to complete the task now, all we need to do is type `bash Lab5.sh` on our local terminal and hit enter.


