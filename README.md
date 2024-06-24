## balls app
track cricket BALLS

# Generate SSH Key Pair
1. Open gitbash/vscode terminal in the directory you want to clone the repo and enter:
`ssh-keygen -t ed25519 -C "your_email@example.com"`
  - This will generate two keys. a publice key ('id_ed25519.pub') and a private key ('id_ed25519')
  - When you're prompted to "Enter a file in which to save the key", just press Enter to accept the default file location
2. Add SSH Key to the SSH Agent
  - In an admin elevated powershell window, start the ssh-agent manually with:
`Get-Service -Name ssh-agent | Set-Service -StartupType Manual` 
`Start-Service ssh-agent`
3. In your vscode terminal window without elevated permissions, add your private SSH Key to the ssh-agent with:
`ssh-add c:/Users/YOU/.ssh/id_ed25519`
4. Now Add SSH Key to github
  - Go to GitHub Settings > SSH and GPG keys and click on "New SSH key".
  - Paste your SSH key into the "Key" field and give it a descriptive title.

# Cloning the Repo

1. Launch VScode and navigate to the directory you want to the repository to sit on your computer then run the command:
`git clone git@github.com:username/repository.git`
  - type git clone and then navigate to the blue code button in the repo on the website and click copy under SSH, This is what you will paste into terminal after typing git clone

# Pushing and Pulling Changes to the repository
1. Pull the latest changes before making any edits. You can do this through the following command:
`git pull origin main`
  - This command pulls and merges changes from the main branch to your local computer branch
2. Creating a working branch to work on your changes is useful when you are working on code that may not work yet you want to log the changes while also not affecting the main branch. Use the command:
`git checkout -b <branch_name>`
  - Replace <branch_name> with a descriptive name for your branch (for instance 'balls/the_left_one')
3. Staging and Committing Changes:
 - Staging Changes
`git add .`
 - Commit Changes with a message:
`git commit -m "added ____ feature"`
4. Pushing Changes to main branch:
`git push origin <branch_name>`

