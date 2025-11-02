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
    ```
    vim config
    ```
    - add the below content
    ```
    HOST github.com-<name identifiable to repo/project>
      HOSTNAME github.com
      User git
      IdentityFile ~/.ssh/<key name>
      IdentitiesOnly yes
    ```
    ````
    eg: 
    
    HOST github.com-githubactions
      HOSTNAME github.com
      User git
      IdentityFile ~/.ssh/github-actions
      IdentitiesOnly yes
    ````


    > **Note:** The same name given for HOST in the config file should be added in the ssh url of the repo while cloning it

    - save it
    ```
    :wq
    ```
    - copy the content of public key
    ```
    cat {keyName}.pub
    ```

* Github account --> settings --> SSH and GPG keys --> click `New ssh key`
    - give a name identifiable with project or repo
    - paste the public key content
    - click `Add SSH key` to save it

* In the terminal, change the directory to clone the repo 
```
git clone <ssh url of the repo>
```
> **Note:** Add the same name given for HOST in the ssh config file in ssh URL (eg : the ssh url of the repo looks like `git@github.com:udemyDevops/github-actions.gi`). After adding the host name while cloning it looks like (eg: `git@github.com-{name used for HOST}:udemyDevops/github-actions.git`)

> eg: 

    git clone git@github.com-githubactions:udemyDevops/github-actions.git


