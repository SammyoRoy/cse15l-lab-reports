# Lab Report 4

4) **Log into ieng6**

*Keys pressed: `<up><enter>`*

<img width="274" alt="image" src="https://user-images.githubusercontent.com/29411228/221387889-9c4d4d84-cd42-4e4f-b0b5-fb19d66bf9ab.png">


The `ssh cs15lwi23ams@ieng6.ucsd.edu` command was 1 up in the search history, so I used up arrow to access it.

5) **Clone your fork of the repository from your Github account**

*Keys pressed: `<right-click><enter>`*

<img width="429" alt="image" src="https://user-images.githubusercontent.com/29411228/221469951-ee6ccf9f-bbcb-4567-95ad-1a8a6478fdf1.png">

The `git clone git@github.com:SammyoRoy/lab7.git` was copied to my clipboard, so right clicking pastes it into the terminal.

6) **Run the tests, demonstrating that they fail**

*Keys pressed: `<ctrl+c><right-click><enter>`*
  
 <img width="779" alt="image" src="https://user-images.githubusercontent.com/29411228/221474622-bec7bd94-0b91-4ba2-a7df-5ee75581fa8e.png">


I used `<ctrl+c>` to copy the following command from a Google Doc, and then right-clicked to paste it into the terminal.
  ```
   cd lab7; javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java;
   java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
  ```
The semi-colons chain the commands together, so they run consecutively automatically. The whole command compiles and runs the relevant java classes.
  
7) **Edit the code file to fix the failing test**

 *Keys pressed `<ctrl+r><"n"><enter> <ctrl+w><"merge"><enter>, <down[10 times]><left[6 times]><backspace><"2">, <ctrl+o><enter><ctrl+x>`*
  
  <img width="713" alt="image" src="https://user-images.githubusercontent.com/29411228/221472517-92064403-1f5b-469f-ad34-7fe329652c48.png">

 I used `<ctrl+r>` to reverse search my previous commands. Typing "n" shows the `nano ListExamples.java` command I had used previously. I then search the file for "merge" using `<ctrl+w>`, and then navigated down to the bug using the arrowkeys. After fixing the bug, I saved and exited the file using `<ctrl+o>` and `<ctrl+x>`.
    
8) **Run the tests, demonstrating that they now succeed**
    
  *Keys pressed: `<right-click><enter>`*
    
  <img width="775" alt="image" src="https://user-images.githubusercontent.com/29411228/221473493-1b99cbfd-8fe4-4413-b07b-40fb3ab69d1d.png">
The following command was still copied, so I right-clicked to paste it.
 
 ```
   cd lab7; javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java;
   java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
   ```

This compiled and ran the JUnit tests again.

9) **Commit and push the resulting change to your Github account**
    
  *Keys pressed: `<ctrl+c><right-click><enter>`*
 
  <img width="603" alt="image" src="https://user-images.githubusercontent.com/29411228/221474439-5613e338-cb7b-4480-a374-d24c23e4141f.png">

  I used `<ctrl+c>` to copy the following command from a Google Doc: `<git add ListExamples.java; git commit -m fixed; git push>`. This pushes
  the change I made to my fork.
  
