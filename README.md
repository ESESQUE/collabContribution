# CollabContribution 

CollabContribution is a VSCode extension that tracks the contribution of each collaborator on a project. It provides metrics for lines of code written, test cases scores, and error scores. The extension then combines these into a final normalized score for each user, allowing instructors to have a clear and fair assessment of each collaborator's contribution.

## Requirements

The extension requires the installation of node.js, which can be installed from the following [link](https://nodejs.org/en).


## Installation
1. Download Visual Studio Code
2. Download the collabcontribution folder from the github repository
3. Upload the folder into the .vscode/extensions directory
4. Open Visual Studio Code, and you should see it in the extensions tab

Watch the installation guide video for more details:

[![Installation Video](https://i.ytimg.com/vi/yuxHd9tjQl0/hqdefault.jpg?sqp=-oaymwE1CKgBEF5IVfKriqkDKAgBFQAAiEIYAXABwAEG8AEB-AHkBYAC4AOKAgwIABABGCYgXChyMA8=\u0026rs=AOn4CLD4FfTep9wpItIdNMCF87sZ5LI7CA)](https://youtu.be/yuxHd9tjQl0)

## How to Use

The extension can be used by both instructors and students. All interactions with the extension are done through the command palette. To open the command palette, press `Ctrl+Shift+P` or `Cmd+Shift+P` on Mac. 

For students, the extension provides the following commands:
* `Student: Please identify your name (ex: John)` - Used to identify the user's name in order to attribute it to the copies of the code that will be evaluated later.
* `Student: Save current file as a milestone` - Saves a copy of the code that the student is working on. The student should make sure to save the file before running this command. The student should make sure to regularly run this command in order to be evaluated fairly on their contribution to the project. Copies are used later in the evaluation process.

For instructors, the extension provides the following commands:
* `Instructor: Generate a pdf of student contribution report` - Used to generate a pdf report of the contribution of each student. The report is generated in the same directory as the project. The command asks for the path of json file that includes the test cases that the students code is going to be assessed against. The json file should be in the following format where each item in the list is considered a test case:
```
  [
    {
      "input": "3 4",
      "expectedOutput": "7"
    },
    {
      "input": "10 20",
      "expectedOutput": "30"
    },
    {
      "input": "-5 5",
      "expectedOutput": "0"
    }
  ]  
```

Watch the usage guide video for more details:

[![Usage Video](https://i.ytimg.com/vi/HH1bPfeL6R8/hqdefault.jpg?sqp=-oaymwE1CKgBEF5IVfKriqkDKAgBFQAAiEIYAXABwAEG8AEB-AHkBYAC4AOKAgwIABABGGUgUChBMA8=\u0026rs=AOn4CLBAJKmRY3RjzqcoWqXP93kl8SOdRg)](https://youtu.be/HH1bPfeL6R8)

## Testing out the extension

We have provided you with some files to test out the extension and learn how it works. The files are located in the trial_files folder. The files are as follows:
* `exercise.py in exercise_files` - A python file that resembles a sample project that the students are assigned to work on. The file contains a function that the students should work on which adds two numbers together.
* `test.json in test_case` - A json file that contains the test cases that the students code is going to be assessed against. This file resembles the test cases that the instructor provides to evaluate the students' code.

The idea here is that the instructor uploads an exercise_file, which the students download and work on. While working on it, the students will save milestones of the code using the provided command. Once they are done. They will submit the folder to the instructor. The instructor will then run the extension on the folder and generate a report of the students' contribution.


