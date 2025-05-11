## this file was created for learning purposes only

## Clone 
### via HTTPS
```sh
git clone https://github.com/BENCHINE01/git-learning-path.git
cd git-learning-path
```

### via SSH
```sh
git clone git@github.com:BENCHINE01/git-learning-path.git
cd git-learning-path
```

## Configuration
When Git is first installed in a machine, the user is demanded to configure the email and username to his github account...

```sh
git config --global user.name "BENCHINE"
git config --global user.email "benchine@example.xyz"
```

## Initialization 
When you first create a project and want to link it to a git repository you run the following commands...

```sh
git init 
touch README.md
echo "Hello World" > README.md
git add .
git commit -m "Initial commit"
git push
```

## Add 
When you want to stage a file to be commited you run the add command...

```sh
git add you_file.txt
```

when you commit, only the staged files will be commited.

Use `.` to stage all changed files 

```sh
git add .
```

## Commit 
When changes are staged, they are ready to be commited.
To do so, use the `commit` command with `-m ` flag to add a commit message...
```sh
git commit -m "Added file X to the project"
```

## Log
To view the commit tree, use `log` command with `--list` flag to only show the commit messages...
```sh
git log --list
```

## Reset 
However, if you want to undo commits that haven't been pushed to the remote repo yet, you use `reset` command 

```sh
git add you_file.txt
git reset 
```