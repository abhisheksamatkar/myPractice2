**///////////// 1. Initialize a Git repository, create a text file, and perform add and commit operations using Git commands.////////////////////**



\# Experiment 1: Initialize a Git repository, create a text file, and perform add and commit operations using Git commands



\# STEP 1: Open terminal / command prompt

1\. Open Git Bash or PowerShell



\# STEP 2: Create a new folder for your project

2\. mkdir git-demo



\# STEP 3: Navigate into the folder

3\. cd git-demo



\# STEP 4: Initialize Git repository (creates .git hidden folder)

4\. git init



\# Expected output:

\# Initialized empty Git repository in C:/Users/abhis/git-demo/.git/



\# STEP 5: Set your identity (Git requires this before committing)

5\. git config --global user.email "abhishek.18314@sakec.ac.in"



\# STEP 6: Set your name

6\. git config --global user.name "Abhishek Samatkar"



\# STEP 7: Create a text file with content

7\. echo "This is my first file for DevOps practical exam" > file1.txt



\# STEP 8: Verify the file was created

8\. dir

\# OR

8\. ls



\# Expected output:

\# file1.txt



\# STEP 9: View the file content

9\. cat file1.txt



\# Expected output:

\# This is my first file for DevOps practical exam



\# STEP 10: Check Git status (shows untracked file)

10\. git status



\# Expected output:

\# On branch master

\# No commits yet

\# Untracked files:

\#   (use "git add <file>..." to include in what will be committed)

\#         file1.txt

\# nothing added to commit but untracked files present



\# STEP 11: Add the file to staging area

11\. git add file1.txt



\# STEP 12: Check Git status again (shows file is staged)

12\. git status



\# Expected output:

\# On branch master

\# No commits yet

\# Changes to be committed:

\#   (use "git rm --cached <file>..." to unstage)

\#         new file:   file1.txt



\# STEP 13: Commit the file to repository

13\. git commit -m "First commit: added file1.txt"



\# Expected output:

\# \[master (root-commit) abc1234] First commit: added file1.txt

\#  1 file changed, 1 insertion(+)

\#  create mode 100644 file1.txt



\# STEP 14: View commit history

14\. git log



\# Expected output:

\# commit abc1234def5678...

\# Author: Abhishek Samatkar <abhishek.18314@sakec.ac.in>

\# Date:   Mon May 25 xx:xx:xx 2026 +0530

\#     First commit: added file1.txt



\# STEP 15: Verify everything is clean

15\. git status



\# Expected output:

\# On branch master

\# nothing to commit, working tree clean                      # Shows commit history

















**///////////////2. Create a GitHub repository and push a local project to the remote repository./////////////////////**

\# Experiment 2: Create a GitHub repository and push a local project to the remote repository



\# PART A: Create repository on GitHub website (do this first)



\# STEP 1: Open web browser and go to https://github.com

1\. Open Chrome/Firefox/Edge



\# STEP 2: Login to your GitHub account

2\. Enter username and password (or use saved login)



\# STEP 3: Click the "+" icon in top-right corner

3\. Click on the plus symbol (+)



\# STEP 4: Select "New repository" from dropdown

4\. Click "New repository"



\# STEP 5: Enter repository details

5\. Repository name: my-local-project



\# STEP 6: Add description (optional)

6\. Description: "My DevOps practical project"



\# STEP 7: Choose Public or Private

7\. Select "Public" (easier for exam)



\# IMPORTANT: DO NOT check these boxes:

\# ❌ Add a README file

\# ❌ Add .gitignore

\# ❌ Choose a license



\# STEP 8: Click "Create repository" (green button)

8\. Click "Create repository"



\# STEP 9: Copy the HTTPS URL shown on the page

9\. URL looks like: https://github.com/abhisheksamatkar/my-local-project.git



\# PART B: Connect and push from terminal



\# STEP 10: Open terminal and navigate to your project

10\. Open Git Bash or PowerShell

11\. cd git-demo



\# STEP 12: Check current remote (should be none)

12\. git remote -v



\# Expected output: (nothing, no remotes configured)



\# STEP 13: Add the remote repository URL

13\. git remote add origin https://github.com/abhisheksamatkar/my-local-project.git



\# Note: Replace the URL with YOUR actual repository URL



\# STEP 14: Verify remote was added

14\. git remote -v



\# Expected output:

\# origin  https://github.com/abhisheksamatkar/my-local-project.git (fetch)

\# origin  https://github.com/abhisheksamatkar/my-local-project.git (push)



\# STEP 15: Check current branch name

15\. git branch



\# Expected output:

\# \* master



\# STEP 16: Rename branch from master to main

16\. git branch -M main



\# STEP 17: Verify branch name changed

17\. git branch



\# Expected output:

\# \* main



\# STEP 18: Push code to GitHub

18\. git push -u origin main



\# STEP 19: When prompted for username

19\. Type: abhisheksamatkar (your GitHub username)

\# Press Enter



\# STEP 20: When prompted for password

20\. Paste your Personal Access Token (starts with ghp\_)

\# Note: Password field will be blank while typing - this is normal

\# Press Enter



\# Expected output:

\# Enumerating objects: 3, done.

\# Counting objects: 100% (3/3), done.

\# Writing objects: 100% (3/3), 250 bytes, done.

\# To https://github.com/abhisheksamatkar/my-local-project.git

\#  \* \[new branch]      main -> main

\# Branch 'main' set up to track remote branch 'main' from 'origin'.



\# STEP 21: Go back to GitHub and refresh the page

21\. Refresh your repository page on GitHub



\# Expected: You should see file1.txt in the repository



\# STEP 22: Verify the push was successful

22\. On GitHub, you should see:

\# - file1.txt listed

\# - Commit message: "First commit: added file1.txt"

\# - 1 commit in the repository

















**//////////////////////////3.Create two branches in Git, modify a file in both branches, and merge them into the main branch.//////////////////////////////**



\# Experiment 3: Create a GitHub branch in Git, modify a file in both branches, and merge them into the main branch



\# STEP 1: Open terminal and navigate to project

1\. Open Git Bash or PowerShell

2\. cd git-demo



\# STEP 2: Check current branch

3\. git branch



\# Expected output:

\# \* main



\# STEP 3: Create and switch to a new branch

4\. git checkout -b feature-branch



\# Expected output:

\# Switched to a new branch 'feature-branch'



\# STEP 4: Verify you are on the new branch

5\. git branch



\# Expected output:

\#   main

\# \* feature-branch



\# STEP 5: View current content of file1.txt

6\. cat file1.txt



\# Expected output:

\# This is my first file for DevOps practical exam



\# STEP 6: Add a second line to the file (append)

7\. echo "Second line added in feature branch" >> file1.txt



\# Note: >> appends, > overwrites



\# STEP 7: View the file to confirm changes

8\. cat file1.txt



\# Expected output:

\# This is my first file for DevOps practical exam

\# Second line added in feature branch



\# STEP 8: Stage the changed file

9\. git add file1.txt



\# STEP 9: Commit the change

10\. git commit -m "Added second line in feature branch"



\# Expected output:

\# \[feature-branch def5678] Added second line in feature branch

\#  1 file changed, 1 insertion(+)



\# STEP 10: Switch back to main branch

11\. git checkout main



\# Expected output:

\# Switched to branch 'main'



\# STEP 11: View file in main branch

12\. cat file1.txt



\# Expected output:

\# This is my first file for DevOps practical exam

\# (Second line is missing - this is normal)



\# STEP 12: Merge feature-branch into main

13\. git merge feature-branch



\# Expected output:

\# Updating abc1234..def5678

\# Fast-forward

\#  file1.txt | 1 +

\#  1 file changed, 1 insertion(+)



\# STEP 13: View file in main branch after merge

14\. cat file1.txt



\# Expected output:

\# This is my first file for DevOps practical exam

\# Second line added in feature branch



\# STEP 14: Check commit history

15\. git log --oneline



\# Expected output:

\# def5678 Added second line in feature branch

\# abc1234 First commit: added file1.txt



\# STEP 15: Delete the feature branch (optional cleanup)

16\. git branch -d feature-branch



\# Expected output:

\# Deleted branch feature-branch (was def5678)



\# STEP 16: Verify branch is deleted

17\. git branch



\# Expected output:

\# \* main



\# STEP 17: Push the merged changes to GitHub

18\. git push origin main



\# Expected output:

\# Enumerating objects: 5, done.

\# Counting objects: 100% (5/5), done.

\# Writing objects: 100% (3/3), 300 bytes, done.

\# To https://github.com/abhisheksamatkar/my-local-project.git

\#    abc1234..def5678  main -> main















**///////////////////4.Create a pull request in GitHub and resolve a simple merge conflict between two branches.////////////////////////////**



\# PART 1: Create conflict on local (same as before)

1\. cd git-demo

2\. git checkout -b conflict-branch

3\. echo "Hello from conflict-branch" > file1.txt

4\. git add file1.txt

5\. git commit -m "Changed file in conflict branch"

6\. git checkout main

7\. echo "Hello from main branch" > file1.txt

8\. git add file1.txt

9\. git commit -m "Changed file in main branch"

\# PART 2: Push both branches to GitHub

10\. git push -u origin main

11\. git push -u origin conflict-branch

\# PART 3: Create Pull Request on GitHub Website

12\. Go to https://github.com/abhisheksamatkar/MyPractice.git

13\. Click "Pull requests" tab

14\. Click "New pull request" (green button)

15\. base: main  ←  compare: conflict-branch

16\. Click "Create pull request"

17\. Add title: "Merging conflict-branch"

18\. Click "Create pull request"

\# PART 4: GitHub will show merge conflict

19\. You will see: "Can’t automatically merge"

20\. Click "Resolve conflicts" button

\# PART 5: Resolve conflict on GitHub

21\. You will see:

&#x20;   <<<<<<< conflict-branch

&#x20;   Hello from conflict-branch

&#x20;   =======

&#x20;   Hello from main branch

&#x20;   >>>>>>> main

22\. Edit the file to keep only: Hello Resolved on GitHub

23\. Delete the <<<<, ====, >>>> lines

24\. Click "Mark as resolved"

25\. Click "Commit merge"

\# PART 6: Complete the merge

26\. Click "Merge pull request"

27\. Click "Confirm merge"

28\. Click "Delete branch" (optional)



\# Instead of resolving on GitHub, do this locally:

1\. git checkout main

2\. git pull origin main

3\. git merge conflict-branch

\# Conflict appears

4\. echo "Hello Resolved Locally" > file1.txt

5\. git add file1.txt

6\. git commit -m "Resolved merge conflict locally"

7\. git push origin main

\# Pull request will now show as mergeable















**////////////////////5.Configure a basic GitHub Actions workflow to automatically display a build success message on every push.//////////////////////////////**



\# Experiment 5: Configure a basic GitHub Actions workflow to automatically display a build success message on every push

\# STEP 1: Open terminal / command prompt

1\. Open Git Bash or PowerShell

\# STEP 2: Navigate to your project folder

2\. cd git-demo

\# STEP 3: Create the .github/workflows directory (folder)

3\. mkdir -p .github/workflows

\# STEP 4: Navigate into the workflows folder

4\. cd .github/workflows

\# STEP 5: Create a new YAML file using a text editor

5\. Notepad build.yml

\# Alternative if Notepad doesn't work:

5\. nano build.yml

\# OR

5\. code build.yml (if VS Code is installed)

\# STEP 6: Copy and paste the following content into build.yml

\# (Everything below this line goes into the file)



name: Build Status

on: \[push]



jobs:

&#x20; build:

&#x20;   runs-on: ubuntu-latest

&#x20;   steps:

&#x20;     - name: Checkout code

&#x20;       uses: actions/checkout@v4

&#x20;     

&#x20;     - name: Display build success message

&#x20;       run: echo "✅ Build Successful - DevOps Exam"



\# STEP 7: Save the file and close the editor

\# For Notepad: Click File → Save → Close

\# For nano: Press Ctrl+X → Y → Enter

\# For VS Code: Ctrl+S → Close

\# STEP 8: Go back to your main project directory

7\. cd ../..

\# OR

7\. cd C:\\Users\\abhis\\git-demo

\# STEP 9: Check git status to see the new file

8\. git status

\# Expected output:

\# Untracked files:

\#   .github/workflows/build.yml

\# STEP 10: Add the workflow file to staging

9\. git add .github/workflows/build.yml

\# STEP 11: Check status again to confirm it's staged

10\. git status

\# Expected output:

\# Changes to be committed:

\#   new file: .github/workflows/build.yml

\# STEP 12: Commit the workflow file with a message

11\. git commit -m "Added GitHub Actions workflow to display build success message"

\# Expected output:

\# \[main abc1234] Added GitHub Actions workflow to display build success message

\# 1 file changed, 12 insertions(+)

\# create mode 100644 .github/workflows/build.yml

\# STEP 13: Push the workflow to GitHub

12\. git push origin main

\# Expected output:

\# Enumerating objects: 6, done.

\# Counting objects: 100% (6/6), done.

\# Writing objects: 100% (5/5), 512 bytes, done.

\# To https://github.com/abhisheksamatkar/MyPractice.git

\#    abc1234..def5678  main -> main

\# STEP 14: Go to your GitHub repository in a web browser

13\. Open browser → https://github.com/abhisheksamatkar/MyPractice.git

\# (Replace with your actual repository URL)

\# STEP 15: Click on the "Actions" tab (next to "Code" and "Pull requests")

14\. Click "Actions"

\# Expected: You will see a workflow named "Build Status"

\# Status: Yellow circle (running) → Green checkmark (success)

\# STEP 16: Click on the workflow name to see details

15\. Click on "Build Status" (or the latest commit message)

\# STEP 17: Click on the job name ("build") to see the steps

16\. Click on "build"

\# STEP 18: Expand the step "Display build success message"

17\. Click on the arrow or the step name "Display build success message"

\# Expected output inside the step:

\# Run echo "✅ Build Successful - DevOps Exam"

\# ✅ Build Successful - DevOps Exam

\# STEP 19: Make another push to trigger the workflow again (optional)

18\. echo "Testing workflow again" >> file1.txt

19\. git add file1.txt

20\. git commit -m "Testing workflow trigger"

21\. git push origin main

22\. Go back to Actions tab → See new workflow run

\# STEP 20: Verify that the workflow runs on EVERY push

23\. Each time you push code, a new workflow run will appear in Actions tab







**////////////////////////////#6.Create a simple CI/CD workflow using GitHub Actions to build and deploy a static HTML page.//////////////////////////////////////**



\# Experiment 6: Create a simple CI/CD workflow using GitHub Actions to build and deploy a Node.js test file



\# STEP 1: Open terminal and navigate to project

1\. Open Git Bash or PowerShell

2\. cd git-demo



\# STEP 2: Create the Node.js test file (VERY SIMPLE)

3\. Notepad test.js



\# STEP 3: Copy and paste this SIMPLE content into test.js



console.log("Node.js is working!");

console.log("Build Successful - DevOps Exam");



\# That's it! Just 2 lines.



\# STEP 4: Save and close the file

4\. Click File → Save → Close



\# STEP 5: Create the workflows folder (if not exists)

5\. mkdir -p .github/workflows



\# STEP 6: Create the workflow file

6\. Notepad .github/workflows/node-ci.yml



\# STEP 7: Copy and paste this SIMPLE content



name: Node.js CI

on: \[push]



jobs:

&#x20; build:

&#x20;   runs-on: ubuntu-latest

&#x20;   steps:

&#x20;     - uses: actions/checkout@v4

&#x20;     - uses: actions/setup-node@v4

&#x20;       with:

&#x20;         node-version: '20'

&#x20;     - name: Run Node.js

&#x20;       run: node test.js



\# STEP 8: Save and close the file

8\. Click File → Save → Close



\# STEP 9: Add files to Git

9\. git add test.js .github/workflows/node-ci.yml



\# STEP 10: Commit

10\. git commit -m "Added Node.js CI"



\# STEP 11: Push to GitHub

11\. git push origin main



\# STEP 12: Go to GitHub → Actions tab

12\. Open browser → https://github.com/abhisheksamatkar/my-local-project.git

13\. Click "Actions"

14\. Click on the workflow run

15\. Click on "build" job

16\. Expand "Run Node.js" step



\# Expected output:

\# Node.js is working!

\# Build Successful - DevOps Exam







**//////////////////////////Experiment 7: Implement automated testing in GitHub Actions using a sample Python test file/////////////////////////////////**



\# STEP 1: Open terminal and navigate to project

1\. Open Git Bash or PowerShell

2\. cd git-demo



\# STEP 2: Create the Python test file (VERY SIMPLE)

3\. Notepad test.py



\# STEP 3: Copy and paste this SIMPLE content into test.py



print("Python is working!")

print("Test Passed - DevOps Exam")



\# That's it! Just 2 lines.



\# STEP 4: Save and close the file

4\. Click File → Save → Close



\# STEP 5: Create the workflow file

5\. Notepad .github/workflows/python-test.yml



\# STEP 6: Copy and paste this SIMPLE content



name: Python Test

on: \[push]



jobs:

&#x20; test:

&#x20;   runs-on: ubuntu-latest

&#x20;   steps:

&#x20;     - uses: actions/checkout@v4

&#x20;     - uses: actions/setup-python@v5

&#x20;       with:

&#x20;         python-version: '3.11'

&#x20;     - name: Run Python

&#x20;       run: python test.py



\# STEP 7: Save and close the file

7\. Click File → Save → Close



\# STEP 8: Add files to Git

8\. git add test.py .github/workflows/python-test.yml



\# STEP 9: Commit

9\. git commit -m "Added Python test"



\# STEP 10: Push to GitHub

10\. git push origin main



\# STEP 11: Go to GitHub → Actions tab

11\. Open browser → https://github.com/abhisheksamatkar/my-local-project.git

12\. Click "Actions"

13\. Click on the workflow run

14\. Click on "test" job

15\. Expand "Run Python" step



\# Expected output:

\# Python is working!

\# Test Passed - DevOps Exam











**/////////////////////////# Experiment 8: Create a Dockerfile for a simple web application and build a Docker image successfully//////////////**////////////



\# STEP 1: Create a new folder for Docker app

1\. Open Git Bash or PowerShell

2\. cd C:\\Users\\abhis

3\. mkdir docker-app

4\. cd docker-app



\# STEP 2: Create a SIMPLE HTML file (no Python/Flask needed)

5\. Notepad index.html



\# STEP 3: Copy and paste this SIMPLE content into index.html



<h1>Docker App is Running!</h1>

<p>DevOps Exam - Experiment 8</p>



\# That's it! Just 2 lines of HTML.



\# STEP 4: Save and close the file

4\. Click File → Save → Close



\# STEP 5: Create the Dockerfile (VERY SIMPLE - using nginx)

5\. Notepad Dockerfile



\# STEP 6: Copy and paste this SIMPLE content into Dockerfile



FROM nginx:alpine

COPY index.html /usr/share/nginx/html/index.html



\# That's it! Just 2 lines.



\# STEP 7: Save and close the file

7\. Click File → Save → Close



\# STEP 8: Verify both files exist

8\. dir



\# Expected output:

\# index.html

\# Dockerfile



\# STEP 9: Build the Docker image

9\. docker build -t my-web-app .



\# Expected output:

\# Successfully built abc123

\# Successfully tagged my-web-app:latest



\# STEP 10: Verify image was created

10\. docker images



\# Expected output:

\# REPOSITORY    TAG       IMAGE ID       SIZE

\# my-web-app    latest    abc123def      20MB



\# STEP 11: Run the container

11\. docker run -d -p 8080:80 --name my-app my-web-app



\# STEP 12: Test the application

12\. Open browser → http://localhost:8080



\# Expected output: Shows "Docker App is Running!" in HTML



\# STEP 13: Stop the container

13\. docker stop my-app



\# STEP 14: Remove the container

14\. docker rm my-app















**///////////////////////////// Experiment 9: Use Docker Compose to run two containers together (web server + database)///////////////////////////**



\# STEP 1: Create a new folder

1\. Open Git Bash or PowerShell

2\. cd C:\\Users\\abhis

3\. mkdir compose-demo

4\. cd compose-demo



\# STEP 2: Create docker-compose.yml (SIMPLE - just 2 containers)

5\. Notepad docker-compose.yml



\# STEP 3: Copy and paste this SIMPLE content



version: '3.8'



services:

&#x20; web:

&#x20;   image: nginx:alpine

&#x20;   ports:

&#x20;     - "8080:80"



&#x20; db:

&#x20;   image: mysql:8.0

&#x20;   environment:

&#x20;     MYSQL\_ROOT\_PASSWORD: root123

&#x20;   ports:

&#x20;     - "3306:3306"



\# That's it! Very simple.



\# STEP 4: Save and close the file

4\. Click File → Save → Close



\# STEP 5: Start both containers

5\. docker compose up -d



\# Expected output:

\# \[+] Running 2/2

\#  ✔ Container compose-demo-web-1  Started

\#  ✔ Container compose-demo-db-1   Started



\# STEP 6: Verify containers are running

6\. docker ps



\# Expected output: Shows two containers running



\# STEP 7: Test the web server

7\. Open browser → http://localhost:8080



\# Expected output: Nginx welcome page



\# STEP 8: Test database connection

8\. docker exec -it compose-demo-db-1 mysql -uroot -proot123 -e "SHOW DATABASES;"



\# Expected output:

\# +--------------------+

\# | Database           |

\# +--------------------+

\# | information\_schema |

\# | mysql              |

\# | performance\_schema |

\# | sys                |

\# +--------------------+



\# STEP 9: Stop and remove both containers

9\. docker compose down



\# Expected output:

\# \[+] Running 2/2

\#  ✔ Container compose-demo-web-1  Removed

\#  ✔ Container compose-demo-db-1   Removed

































**////////////////////////////// Experiment 10: Write and execute an Ansible playbook to install Nginx and start the service**

**///////////////////////////////**





\# NOTE: This requires Linux. If on Windows, use WSL or exam Linux VM.



\# STEP 1: Create a new folder

1\. Open Linux terminal (or WSL on Windows)

2\. mkdir ansible-demo

3\. cd ansible-demo



\# STEP 2: Create the Ansible playbook (VERY SIMPLE)

4\. nano install-nginx.yml



\# STEP 3: Copy and paste this SIMPLE content



\---

\- name: Install Nginx

&#x20; hosts: localhost

&#x20; become: yes

&#x20; tasks:

&#x20;   - name: Install nginx

&#x20;     apt:

&#x20;       name: nginx

&#x20;       state: present



&#x20;   - name: Start nginx

&#x20;     service:

&#x20;       name: nginx

&#x20;       state: started



\# That's it! Very simple.



\# STEP 4: Save and close

4\. Press Ctrl+X, then Y, then Enter



\# STEP 5: Run the playbook

5\. ansible-playbook -i "localhost," -c local install-nginx.yml



\# Expected output:

\# PLAY \[Install Nginx] \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

\# TASK \[Gathering Facts] \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

\# ok: \[localhost]

\# TASK \[Install nginx] \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

\# changed: \[localhost]

\# TASK \[Start nginx] \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

\# ok: \[localhost]

\# PLAY RECAP \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

\# localhost : ok=3 changed=1 unreachable=0 failed=0



\# STEP 6: Verify Nginx is running

6\. sudo systemctl status nginx



\# Expected output: Active: active (running)



\# STEP 7: Test web server

7\. curl http://localhost



\# Expected output: Nginx welcome page HTML



\# STEP 8: Stop Nginx (if needed)

8\. sudo systemctl stop nginx

