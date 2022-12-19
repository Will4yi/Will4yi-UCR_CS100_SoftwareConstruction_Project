[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-c66648af7eb3fe8bc4f294546bfd86ef473780cde1dea487d3c4ff354943c9ae.svg)](https://classroom.github.com/online_ide?assignment_repo_id=8894541&assignment_repo_type=AssignmentRepo)

# Quiz Maker
 
 
 Authors: [William Yi](https://github.com/will4yi), [Chengzhe Liu](https://github.com/uxxx0521), [Nilesh Patyal](https://github.com/nileshpat), [Briana Moyer](https://github.com/bailytt)


## Project Description
 * Why is it important or interesting to you?
 
 We are all students. This may be something useful we can use to make ourselves study guides in the future.
 
 * What languages/tools/technologies do you plan to use? (This list may change over the course of the project)
 
 We plan to use C++, Visual Studio, GoogleTest, Valgrind.
 
 * What will be the input/output of your project?
 
 Inputs: The uploaded file can contain a list of different types of
questions (e.g. multiple choice, true/false, free response) as well as the correct answers(answers can be optional for free response questions).
 
 Outputs: Text File.
 
 * What are the features that the project provides?
 This description should be in enough detail that the TA/instructor can determine the complexity of the project and if it is sufficient for the team members to complete in the time allotted. 
 
1) This application allows instructors to create quizzes by uploading text files representing question pools. 

2) The instructor can automatically create a quiz based on the uploaded question pool by specifying the required questions types and number of questions. 

3) A quiz can also have questions consisting of other sub-questions of different types. 

4) Instructors can allow students to take
a quiz once or multiple times. 


 
## Class Diagram
![alt text](https://i.imgur.com/H0NXX0n.png)

QuizPool: This will be our main object that we will add or call functions to control what we desire.  
Array: Currently initialized with an array of integers 0-9 of size 10. For STUB testing purposes.  
Expand(): Will expand as needed when size of array is not enough to hold new question objects.  


QuizControls: List of controls for the QuizPool.  
Get/Set MaxAttempts(): Getter and setter for the int value of MaxAttempts.  
Randomize(): A function with parameters "Seed, Number of Questions, Number of Swaps" to randomize a given Array. Using a swapper helper function swaps the element in the array with random array indexes, a specified number of times.  
Get/Set Array Elements(): Currently manipulates an array of ints size 10 for STUB file testing purposes.  


Questions: These questions are one of three types of questions. Multiple choice, True/False, and Free Response. They are either created individually, uploaded from a quiz file, and exist in the existing quiz pool.



Multiple choice, True/False, Free Response: These questions inherit from the questions object. They are a composition of the questions object, meaning cannot stand alone if the question is destroyed.



QuizFileTxt: A text file that is an aggregate of quiz pool. The quiztxtfile can be used to add to an empty or existing quiz pool as the new base. Multiple quiz txt files can be added to the existing list of question pools to form a bigger question pool. The quiz pool can generate a quiz file txt as the finished product.
 
 > ## Phase III
 > You will need to schedule a check-in for the second scrum meeting with the same reader you had your first scrum meeting with (using Calendly). Your entire team must be present. This meeting will occur on week 8 during lab time.
 > * Before the meeting you should perform a sprint plan like you did in Phase I.
 > * You should also make sure that your README file (and Project board) are up-to-date reflecting the current status of your project and the most recent class diagram. Previous versions of the README file should still be visible through your commit history.
> 
> During the meeting with your reader you will discuss: 
 > * How effective your last sprint was (each member should talk about what they did)
 > * Any tasks that did not get completed last sprint, and how you took them into consideration for this sprint
 > * Any bugs you've identified and created issues for during the sprint. Do you plan on fixing them in the next sprint or are they lower priority?
 > * What tasks you are planning for this next sprint.

 
 > ## Final deliverable
 > All group members will give a demo to the reader during lab time. ou should schedule your demo on Calendly with the same reader who took your second scrum meeting. The reader will check the demo and the project GitHub repository and ask a few questions to all the team members. 
 > Before the demo, you should do the following:
 > * Complete the sections below (i.e. Screenshots, Installation/Usage, Testing)
 > * Plan one more sprint (that you will not necessarily complete before the end of the quarter). Your In-progress and In-testing columns should be empty (you are not doing more work currently) but your TODO column should have a full sprint plan in it as you have done before. This should include any known bugs (there should be some) or new features you would like to add. These should appear as issues/cards on your Project board.
 > * Make sure your README file and Project board are up-to-date reflecting the current status of your project (e.g. any changes that you have made during the project such as changes to your class diagram). Previous versions should still be visible through your commit history. 
 
 ## Screenshots
 > Screenshots of the input/output after running your application
![alt text](https://i.imgur.com/9qeK7cB.png)


 ## Installation/Usage
 > Instructions on installing and running your application

Facing many challenges, we were unable to realize a fully functioning QuizMaker by the deadline. However, in its completion, the Quiz Maker's functionality will follow these guidelines.

- Program may be ran using any IDE
- Upon running, User will be given 3 options to either upload questions to a new quizpool, add to an existing one, or generate a quiz.
- Choice 1: User will be prompted to enter the number of questions and assign a name for the new Quiz Pool. 
- Choice 2: User will be asked to enter the name of an existing quizpool followed by the name up the text file they would like to add.
- Choice 3: User will be prompted to enter the name of the Quiz Pool they'd like to use. Following, the will enter desired number of quiz attempts, number of multiple choice, true false and free response answers. This will generate a new text file with the desired specifications. 

An example test of this is shown in the screenshot above.
 
 ## Testing
 > How was your project tested/validated? If you used CI, you should have a "build passing" badge in this README.

 Tests were ran using GoogleTest.
 Each team member created a testing file for each of the .hpp files and wrote unit tests to verify methods were performing as they should and producing the correct results. 

 
 
