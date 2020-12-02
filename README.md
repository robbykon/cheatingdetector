# Cheating Detector
This project involves creating a cheating detector for exams run on a Linux system. Functionalities are detailed below

List of Functionalities implemented:
#	Check unique IP addresses
o	Detects if a student has multiple IPs open, and logs using date command in violations file
o	Outputs to the terminal so professor can always see who is cheating 
o	Continuously runs every 2 seconds so cheaters can easily be found
#	Collect file versions
o	Creates a directory studentfiles for copy storage
o	Allows professor control over which files to search for (bash scripts, python files, etc.)
o	Retrieves the current file and version number for each student and outputs to terminal, stating that there are none if no current file exists. Formatted to find files starting with the username of the student for retrieval and copying purposes
o	Checks for differences between student’s personal file and the current studentfiles copy, creating an updated file if there are differences
o	Creates a new file if there are no current files in the studentfiles directory and a file exists in the student’s directory
o	Continuously loops every 7 seconds for constant updates
#	Check wildcard results
o	Creates a myfiles directory
o	Reads solution from solution file, can be easily manipulated and changed for reuse on different questions and executes the command into myfiles
o	Stores the correct ls output of files into a correct file for easy access
o	Stores the ls output of a student’s myfiles folder into stu_output for comparison
o	Compares correct file and stu_output for differences, outputting and logging any wrong answers derived from differences into wildcard_wrong
