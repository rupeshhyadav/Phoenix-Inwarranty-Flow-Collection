# Postman API automation integratrion with GitHub Actions #

This repository is a demonstration for POC for integrating postman tests with github actions. The test are written in postman and are executed on VM with the help of newman and newman-reporter-htmlextra.
Github actions will trigger the project execution on every push to the main branch. You can also use workflow_dispatch to run the project manually. The project runs on a scheduled time with the help of the cron job.

The HTML report is archieved and generated in the artifact section for the team to download it. Along with that they can view the report directly from the github page : https://rupeshhyadav.github.io/Phoenix-Inwarranty-Flow-Collection/.
The latest report is mailed to the team members using gmail SMTP

## Tech Stack ##
1. Postman
2. Newman
3. Java Script
4. NodeJS
5. Newman-Reporter-Htmlextra
6. GitHub Actions
7. Gmail SMTP
8. AWS EC2 for self hosted github runner

## Test Coverage ##
1. Happy flow testing
2. Negative and Edge case testing
3. Token testing
4. Data driven testing using CSV
5. Schema Validation
6. Secrets management with GitHub secrets

## HTML Report
![POSTMAN REPORT](https://github.com/rupeshhyadav/Phoenix-Inwarranty-Flow-Collection/blob/static-content/newman-report.png)

## GitHub Pages ##
You can directly view the test report at the GitHub Page : https://rupeshhyadav.github.io/Phoenix-Inwarranty-Flow-Collection/

## Project Structure ##


```
postman
├─ .DS_Store
├─ Inwarranty-flow-collection.postman_collection.json
└─ QA.postman_environment.json

```

## How to run the project ##
To run the project on your local, please follow below steps : 
1. Clone the project on your local : https://github.com/rupeshhyadav/Phoenix-Inwarranty-Flow-Collection.git
2. Install nodejs and npm from https://nodejs.org/en/
3. Install newman using the command : ``` npm install -g newman ```
4. Install newman reporter htmlextra using the command : ``` npm install -g newman-reporter-htmlextra ```
5. Run the newman command : 
           ```newman run 'Inwarranty-flow-collection.postman_collection.json' \
              -e QA.postman_environment.json \
              -r cli,htmlextra \
              --reporter-htmlextra-export ./newman/index.html```



     
