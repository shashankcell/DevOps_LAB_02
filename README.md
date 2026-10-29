# Experiment 02 — GitHub remotes, clone, and push

**Student:** [Your name]  
**Register number:** [Your register number]  
**Course:** Collaborative Development and DevOps

## Aim

Connect a local Git repository to a GitHub remote, clone it, and synchronize commits with `push` and `pull`.

## Requirements

- Git installed and a GitHub account.
- Create an empty practice repository on GitHub, then copy its HTTPS URL.

## Procedure

1. In a local folder, create and commit a file:
   ```sh
   mkdir remote-lab
   cd remote-lab
   git init
   printf "# Remote lab\n" > README.md
   git add README.md
   git commit -m "Initialize remote lab"
   ```
2. Connect the repository you created. Substitute its URL:
   ```sh
   git branch -M main
   git remote add origin https://github.com/YOUR-USER/YOUR-REPO.git
   git remote -v
   git push -u origin main
   ```
3. Clone the GitHub repository into another folder:
   ```sh
   cd ..
   git clone https://github.com/YOUR-USER/YOUR-REPO.git remote-lab-copy
   cd remote-lab-copy
   ```
4. Make a change in the clone and push it:
   ```sh
   printf "\nCloned and updated.\n" >> README.md
   git add README.md
   git commit -m "Update README from clone"
   git push
   ```
5. In the original folder, retrieve and inspect the update:
   ```sh
   cd ../remote-lab
   git pull
   git log --oneline --decorate -n 5
   ```

## What to record

Record the output of `git remote -v`, the first push, and the pull. Explain the roles of `origin`, `push`, `fetch`, and `pull`. Use your own repository URL; never put a password or token in a remote URL.

## Result

Complete this section after performing the commands. Do not report output you did not observe.

## Reference and attribution

The reference repository [DevOps_LAB_02](https://github.com/Smirk1308/DevOps_LAB_02) contained student metadata but no experiment instructions or implementation. This remote workflow is independently authored.