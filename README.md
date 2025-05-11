## this file was created for learning purposes only

## Clone 
### via HTTPS
```sh
git clone https://github.com/BENCHINE01/git-learning-path.git
cd git-learning-path
```

### via SSH
First, generate the SSH key using `keygen` command and follow the steps...
```sh
$ ssh-keygen -o
$ cat ~/.ssh/id_rsa.pub
```
Then create a new SSH key in https://github.com/settings/keys and paste the key from terminal. <br>
Once set up, you can clone the project locally via SSH 

```sh
git clone git@github.com:BENCHINE01/git-learning-path.git
cd git-learning-path
```

### via GitHub CLI 
First, install GitHub CLI from the official website `https://cli.github.com/` <br> 
Once installed, login to your GitHub Account using the following command...
```sh
gh auth login
```
Then follow the steps
```sh
? Where do you use GitHub? GitHub.com
? What is your preferred protocol for Git operations on this host? HTTPS
? Authenticate Git with your GitHub credentials? Yes
? How would you like to authenticate GitHub CLI? Login with a web browser

! First copy your one-time code: D382-ACF3
Press Enter to open https://github.com/login/device in your browser... 
✓ Authentication complete.
- gh config set -h github.com git_protocol https
✓ Configured git protocol
! Authentication credentials saved in plain text
✓ Logged in as BENCHINE01
```

Now you can clone your repo locally using the command...
```sh
gh repo clone BENCHINE01/git-learning-path
```
<table>
    <thead>
        <tr>
            <th>ID</th>
            <th>Last Name</th>
            <th>First Name</th>
            <th>Email</th>
            <th>Phone Number</th>
        </tr>
        <tr>
            <td>1</td>
            <td>BENCHINE</td>
            <td>Abdelilah</td>
            <td>benchine@gmail.com</td>
            <td>0614422367</td>
        </tr>
    </thead>
</table>

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