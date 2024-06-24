## balls app
track cricket BALLS

# Generate SSH Key Pair
1. Open terminal or cmd prompt and enter:
`ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`
  - This will generate two keys. a publice key ('id_rsa.pub') and a private key ('id_rsa')
2. Add SSH Key to the SSH Agent
`eval "$(ssh-agent -s)"`
  - Then add your private SSH key to the agent with
`ssh-add ~/.ssh/id_rsa`
3. Add SSH Key to github
`pbcopy < ~/.ssh/id_rsa.pub`  --> for macOS
`cat ~/.ssh/id_rsa.pub | clip`   --> for Windows
4. Go to GitHub Settings > SSH and GPG keys and click on "New SSH key".
5. Paste your SSH key into the "Key" field and give it a descriptive title.

# Cloning the Repo

1. Launch VScode and navigate to the directory you want to the repository to sit on your computer then run the command:
`git init`
2. use the following command to clone the repository:
`git clone git@github.com:username/repository.git`

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

