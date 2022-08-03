# Student Reports
Generate personalized student reports in an open and secure manner. 
With one-click updates through Gradescope. 

## Updating
To update the student reports simply click `regrade all submissions` under the appropriate Gradescope assignment. 

## Initial Setup
### Requirements 
Ensure you have python3 and pandas install. 
```pip install pandas```

### Gradescope Setup
Create a new `Programming Assignment` under Gradescope. If you don't wish to publish the assignment yet set the release date for far in the future. 

### Clone/Fork This Repository 
```git clone git@github.com:CS70/student-reports.git```

### Setup the Config File
Create a file called `config.json`. This file will contain all the information needed to setup your report.
```

```
### Create a Google Sheet with Reports
Create a copy of the following [Sample Report Google Sheet](https://docs.google.com/spreadsheets/d/1GIKOwPHVBjgTgT8Vk2qeg1hEDeVSpu_syy2WC9XdZVQ/edit?usp=sharing). 
Ensure that the Google sheet is [viewable](https://support.google.com/docs/answer/2494822?hl=en&co=GENIE.Platform%3DDesktop) to anyone with a link. 

Copy this viewable public link over to the `Sheet: ` attribute in the `config.json` file. 
In the second sheet copy the same SALT that you have in your config file. 

#### Structure of Sheet
The script will only pull the very first sheet. This is your report. 
You may add additional sheets to you spreadsheet, to help organize and process for the first sheet. 

### Add a hash function 
You can paste the following code to create a hash function to ID all the entries for the report. 
This will use the SALT provided. 
 
### Enter Your Data
Fill out the data. 

### Compress the Source Directory
Compress the contents of the `source/` directory. 
This is the script that Gradescope runs to "grade" the students' "submission" and allows us to display the report as their autograder report. 

IMPORTANT: Do not compress the directory itself, just the contents. So, this means you should select all the files inside of the `source/` directory and then compress those. 

### Setting Up Autograder
Upload this compressed file under Gradescope to setup the autograder. 

## Documentation
TODO

## Explanation
It is a frequent need to share general information with student, where the structure and format may be identical but data is different across students--think grade reports, attendance, exam format, etc. 
This allows to do this using the [Gradescope Autograder](https://gradescope-autograders.readthedocs.io/en/latest/)
### Alternative
You can always use mail merge to email these personalized reports out. 
This has the drawback that to update them you have to resend emails. 
