# demo
This is demo to show git activities / Commands
I have cloned repo to win.

This automation script helps to install App environment:
   1. Maven Build Tool
   2. Tomcat App Server
   3. Nginx Web Server
   4. Maria DB Server
   5. Git

Total 2 scripts haveen implemented to complete 3 tier App deployment

First script helps to complete following tasks:

Task-1: update the system and enable security
Task-2: Create devops user and enable password based authentication


Run the script to setup the tools:
**
Login as root user and run the script:**

         $ sudo su -
         $ ./scriptname.sh

Second script helps to complete following tasks:

Task-1:
Task-2: 


------------------------------------------------------------

Jenkins Build Stpe:

Job#1: Setup App Tools

Step-1: Restrict the job on Slave Node
Step-2: Integrate with GitHub repo
Step-3: Add Build Step 'Execute Shell'
         sudo chmod +x install_student_app_tools.sh
         sudo su -c "./install_student_app_tools.sh"

Test the App:
- http://192.168.33.11
- http://192.168.33.11:8080
- mysql -uroot

Job#2: Deploy Student App

Step-1: Restrict the job on Slave Node
Step-2: Integrate with GitHub repo
Step-3: Add Build Step 'Execute Shell'
         sudo chmod +x setup_studentapp.sh
         sudo su devops -c "./setup_studentapp.sh"

Test the App:
- http://192.168.33.11/student/
- http://192.168.33.11:8080/student
- mysql -ustudent -pstudent1
