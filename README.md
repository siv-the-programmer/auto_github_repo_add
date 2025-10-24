Git Auto Push Script
---
This Bash script automates the process of uploading files to GitHub by guiding you through selecting a file, entering a commit message, and pushing the changes to your repository. It is designed to simplify frequent commits and is currently used within the Python-lab
 repository.

Features
-

Lists all files in the current directory for selection.

Automatically detects the active Git branch.

Pulls the latest changes from the remote repository before committing.

Commits the selected file with a custom message and pushes it to GitHub.

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

This script was originally created for the Python-lab
 project to streamline file updates and GitHub commits during Python learning and experimentation.
