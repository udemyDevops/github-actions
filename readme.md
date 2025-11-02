* In this section we will be learning GitHub actions, a built-in CI/CD workflow in GitHub. In short it is a CI/CD platform built into GitHub.
* Github repo --> actions --> can configure workflow (CI/CD pipeline in github actions is called workflow)
    - The workflow will be written in YAML format ([_sample workflow_](sample-workflow.yaml))
    - The workflow should have the name as `main.yml` or 'main.yaml' and should be located in the `.github/workflows` folder inside the repo (this exercise do not have this folder)
    - Can automate the tasks -- testing, building, deployment, notifications...

1. Introduction

![alt text](images/what-is-github-actions.png)

![alt text](images/why-github-actions.png)

![alt text](images/core-concepts.png)

![alt text](images/common-use-cases.png)

* we can use plugins available in marketplace (https://github.com/marketplace) --> actions --> all actions
    - search for specific action --> click on it to see the usage

2. [_quickstart_](quickstart) --> uses source code in [_vprofile-project folder_](vprofile-project)
    - when doing the practice make sure the directories of source code and .github/workflows/ are in the root directory of the repo (to avoid any path issues in the workflow)