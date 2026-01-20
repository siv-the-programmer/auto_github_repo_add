Git Auto Push Script
---

![Shell Script](https://img.shields.io/badge/Shell-Bash-4EAA25?logo=gnu-bash&logoColor=white)

This Bash script automates the process of uploading files to GitHub by guiding you through selecting a file, entering a commit message, and pushing the changes to your repository. It is designed to simplify frequent commits and is currently used within the Python-lab
 repository.

Features
-

Lists all files in the current directory for selection.

Automatically detects the active Git branch.

Pulls the latest changes from the remote repository before committing.

Commits the selected file with a custom message and pushes it to GitHub.

Example 1
-
<img width="797" height="437" alt="Screenshot 2025-10-24 141448" src="https://github.com/user-attachments/assets/6f7ac523-b9ae-4fbf-86c8-5bac939452a7" />

Requirements
-

Git must be installed and configured on your system.

The repository should already be initialized (git init) and linked to a remote GitHub repository.

You should have valid authentication (e.g., SSH key or GitHub CLI login).

Usage
-

Save the script in your project directory as git_auto_push.sh.

Make it executable:
```
chmod +x git_auto_push.sh

```


Run the script:
-
```
./git_auto_push.sh

```
Example 2
-
<img width="865" height="705" alt="Screenshot 2025-10-24 141541" src="https://github.com/user-attachments/assets/c1aa2cb2-1369-486e-887d-6fd91f7839ba" />

Follow the prompts:
-

Choose the file you want to upload from the displayed list.

Enter your commit message when prompted.

The script will automatically pull, commit, and push your changes.

Example Workflow
-
```
$ ./git_auto_push.sh
Files in current directory:
1. script.py
2. notes.txt
Select the file number you want to upload: 1
Enter commit message: Update script with new function
Pulling latest changes from remote...
[main 1234abc] Update script with new function
 1 file changed, 10 insertions(+)
Pushed to branch 'main'
'script.py' successfully committed and pushed to 'main'!
```

Customization
-

The script automatically detects the current branch.

To include hidden or nested files, modify the find command in the script.

For multiple file selection, the script can be extended to handle comma-separated inputs.

Repository
-

# This script was originally created for the Python-lab
# project to streamline file updates and GitHub commits during Python learning and experimentation.
