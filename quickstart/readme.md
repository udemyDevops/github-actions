* Create a repo with visiblity as private
* Use 'ssh' connection with the repo from vscode or terminal (need to create ssh key and share it with github account)
* Open Git Bash (windows) or terminal

    - Run the below command to get into the hidden ssh folder in the user's home directory
    ```
    cd .ssh/
    ```
    - create ssh key (with the name identifiable with the repo or project)
    ```
    ssh-keygen -t rsa -b 2048 -f <key name>
    ```
    > eg: ssh-keygen -t rsa -b 2048 -f github-actions

    - create a config file which will tell the ssh to use the specified private key when the github URL matches with the target repo (in this case 'github-actions')


