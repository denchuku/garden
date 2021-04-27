# Pipenv
Allows to manage multiple environemnts and their requirements.

![[Python Installation#Install pipenv]]

## Environments
Environments allow to have different project with different dependencies (and python versions).

### Create environment 
Typically create environment directly in the root of a project. This onyl has to be done once.
```shell
cd prj-root
pipenv install
```

### Enter environment
Enter environment shell to be sure to have specified versions.
```shell
cd prj-root
pipenv shell
```

### Exit environment
(When in environment shell:)
```shell
exit
```

### Environment location
Output Python interpreter information
```shell
pipenv --py
```
/Users/dennis/.local/share/virtualenvs/md-mkdocs-material-helper-suciZAwh/bin/python

Output Python interpreter information
```shell
pipenv --venv
```
/Users/dennis/.local/share/virtualenvs/md-mkdocs-material-helper-suciZAwh

### Install packages in environment
(When in environment shell:)
```shell
pipenv install pyyaml
```

Packages only needed for development
```shell
pipenv install --dev pytest
```

Uninstall package
```shell
pipenv uninstall package_name
```

### Git considerations
- commit the **Pipfile** to GIT
- The lock file **Pipfile.lock** can be committed to GIT or added into your **.gitignore**

Good example of readme.md (from https://mattgosden.medium.com/pipenv-for-easier-virtual-environments-69e1e520cde8):

```markdown
# Developers
Instructions for installing this project on your local machine and getting it running in its own virtual environment.
1.  Clone this project into a new directory - click the clone button above on GitHub to get the link and command to use
2.  Ensure you have `pipenv` installed on your machine - installation documentation can be found here - https://docs.pipenv.org/en/latest/install/
3.  From the project root directory run `pipenv install --dev --pre` to create your virtual environment and install all the packages
4.  Activate your virtual environment at any time using `pipenv shell` - note only do this from the project directory root
5.  You can now run the program using `python main.py` or the tests using `python -m pytest`
6.  Deactivate your virtual environment at any time using `exit`

```



### Ressources
- https://mattgosden.medium.com/pipenv-for-easier-virtual-environments-69e1e520cde8
- https://python.land/virtual-environments/pipenv


 