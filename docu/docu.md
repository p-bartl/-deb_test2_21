## Dependencies

### Backend
- TypeScript
- Express

## Frontend
- Node v14.15.1 (LTS), or more recent
- npm 6.14.8 (LTS), or more recent
- Angular

### AWS / CI/CD
- AWS CLI v2
- AWS EB CLI

## Infrastructure and Deployment-Process
### General Information
- CircleCi listens for changes in the GitHub repo
- By pushing new code to the remote repo we trigger the execution of the CircleCi Pipeline (as configured in the config.yml)
    - Installs Node
    - Installs NPM
    - Checkout the source code
    - Installs AWS CLI
    - Installs EB CLI
    - Installs Frontend dependencies
    - Installs Backend dependencies
    - Builds Frontend  
    - Builds Backend
    - Deploys Frontend
    - Deploys Backend

![Alt text](screenshot/1_new.png?raw=true "Title")

### Backend
- Build Backend
- Upload to Source Code to AWS S3
- AWS updates the environement
- Deploy to EC2

### Frontend
- Build Frontend
- Upload to AWS S3 (Please note that the naming of the S3 bucket is a bit misleading since it does not include the word "frontend")

![Alt text](screenshot/5.png?raw=true "Title")



