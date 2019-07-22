# How to use this thing
A step-by-step on setting up and using github for this project. 
Covers: 
* virtual environments and package requirements; [Reference](https://medium.com/@boscacci/why-and-how-to-make-a-requirements-txt-f329c685181e)
* branches
* push/pulling, staging/adding and committing changes; GitHub has a lot of [Tutorials](https://www.atlassian.com/git/tutorials/setting-up-a-repository) and [Cheatsheets](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf) if you need them. 


## Setting Up 
For the first time you use this. 
### Configure your git
In command line prompt: <br>
```
    $ git config --global user.name your_name
    $ git config --global user.email your_email
```
**Important:** Make sure that you have `nbdime` installed. This will enable version control of jupyter notebooks easier. You can read about it [here](https://nbdime.readthedocs.io/en/latest/). Use `pip install nbdime` and then `nbdime config-git --enable --global` to set up.<br>

### Create a local repository 
Clone the files to your own local drive. In your command line prompt/terminal: `cd` (change directories) to the place you want to store the repository as a new folder: <br>
```
    $ cd /home/your_username/your_repos/
    $ git init
    $ git clone https://github.com/gerpang/AMLProject_GrabSafety.git
```

### Set-Up virtual environment 
Using virtual environments and requirements.txt ensures that we have all the required packages to run our code, and that the packages are updated. 

To create a new virtual environment, in your command line prompt/terminal:<br>
```
    $ conda create -n aml_proj python=3.6
```

Check existing environments you have - <br>
```
    $ conda env list`
```

Activate the new virtual environment:<br>
```
    $ conda activate aml_proj
``` 
Note: `(aml_proj)` will appear to the left of your command prompt. Repeat this step everytime you start up.  

To deactivate the environment after you are done:<br>
```
    (aml_proj) $ conda deactivate
```

Install packages from the requirements file into this environment with:<br>
```
    (aml_proj) $ pip install --user --requirement requirements.txt
```

To update the requirements file, *WHILE you are in the environment*<br>
```
    (aml_proj) $ pip freeze > requirements.txt
```

### Individual branches
Avoid working on the master branch. 
- `git branch` lists all available branches.
- Create a branch for yourself with `git checkout -b ger_branch`
- Or checkout an existing branch with `git checkout existing_branch` e.g. master

## Making Changes
After setting up, you can work on the files locally. For any changes you make, push them to the remote (shared) repo when you're done. <br>
```
    $ git add -A 
    $ git commit -m 'insert-message-describing-your-changes'
    $ git push
```
<br><br>
`git add -A` adds all files, which is not ideal. If you want to check which files you have changed and push only those, use `git status` then add them individually:<br>
```
    $ git status 
    $ git add *.py 
    $ git add documentation.txt
    $ git push
```
And we're done! 

# tl:dr;
1. First time setting up: 
    - `git init`, `git clone`
    - `source/conda env create` and then `activate`
    - `git checkout -b your_branch_name` to create and checkout 
2. After saving changes:
    - `git add -A` or individual files
    - `git commit -m "message"`
    - `git push`
3. Subsequent uploads
    - `git checkout my_branch`
    - `git pull` to retrieve changes
4. To review all changes 
    - `git checkout branch_name`
