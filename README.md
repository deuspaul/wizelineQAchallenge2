# wizelineQAchallenge2
QA Challenge #2

Todoist API with Postman and Newman


Bonus:

1. A file called setenv.sh was created with the script to create the environment variable that contains the API key. This file was excluded from the repository in the .gitignore file. A git push command was used to validate that the file with the environment variable script is not pushed to the remote repository.


2. Reporter was used to generate the results of the execution of the main collection with all the CRUD requests from the assignment as well as a second one with the results of the creation of several tasks with a csv file.
newman run ./collection/todoisPmCollection.json -e ./envVariables/todoistPmVariable.json -r htmlextra 
--reporter-htmlextra-export './todoistApiTestsReport.html'

3. A csv file was used to create several tasks through the command line.
newman run './tests/backend/collection/todoistSeveral.json' -e './tests/backend/envVariables/todoistPmVariables.json' -d several.csv -r htmlextra --reporter-htmlextra-export './todoistApiTestsReportSeveral.html'
