# Postman API Automation Integration with Github Actions #

This repository is a demomnstration for POC for integration postman tests with github actions.The Tests are written  in postman and they are executed on the VNM with the help of newman and newman-reporter-htmlextra.
Github Actions will trigger the project execution on every push to the main branch.You can also execute the project manually using workflow_dispatch. The Projects run on a sechduled time with the help of the cron job.

The Html report is achieved and kept in the artifect section for the team to download it. along with that they can view the report dierectly fro the github page: https://vibha45.github.io/Phoenix-Inwarranty-Flow/.
The latest report is mailed to the team members using GMAIL SMTP.

## About Me ##
Hi My Name is Vibha Gupta. I have 8 years experience in Software testing. My Skillset includes Functional testing, UI Automation with selenium WebDriver and for API Testing using Rest Assured and Postman.
Yo can connect with me over: (https://www.linkedin.com/in/vibha-g-8485a7134/)

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge Case Testing
3. Token Testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Secrets Management with Githhub Secrets
   

## Tech Stack ##
1.Postman
2.Nodejs 22v
3. Newman
4. Newman-Reporter-Htmlextra
5. Github Actions
6. Github Pages
7. Gmail SMTP
8. CSV for Data Driven Testing
9. AWS-EC2 instance for self hosted github runner

## Github Pages ##
you can directly view the latest report of the Postman test at the github Page Link: https://github.com/vibha45/Phoenix-Inwarranty-Flow


## HTML Report ##
The Reprot will created in the newman folder
![Postman Report](https://raw.githubusercontent.com/vibha45/Phoenix-Inwarranty-Flow/static-content/newmanreport.png)

## Project Stracture ##

```
Phoenix Inwarranty Flow
├─ Inwarranty-flow Collection.postman_collection.json # Collection File
├─ QA.postman_environment.json # Envoirnment File
└─ testdata.csvv # Test Data File

```

## How to run the Project? ##
you can run th project on your local system for that:
1. Clone the Project on Local System : https://github.com/vibha45/Phoenix-Inwarranty-Flow.git
2. Install Node.js and NPM from: https://nodejs.org/en
3. Install Newman using ``` npm -g install newmnan ```
4. Install Newman-reporter-htmlextra : ``` npm install -g newman -reporter-htmlextra ```
5. Run the Newman command:

  ```  newman run "Inwarranty-flow Collection.postman_collection.json" \ 
            -e QA.postman_environment.json \
            -d testdata.csv \
            -r cli,htmlextra \
            --reporter-htmlextra-export ./newman/index.html
 ```
