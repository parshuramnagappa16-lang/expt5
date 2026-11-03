sudo apt update
sudo apt install openssh-server git -y
sudo systemctl enable --now ssh
sudo systemctl status ssh

hostname -I
whoami

cd ~
mkdir -p dharam
cd ~/dharam
pwd
ls

# Transfer file using FileZilla

ls
cat parshuram.txt

git init
git config --global user.name "parshuram"
git config --global user.email "parshuramnagappa16@gmail.com"

git config --global --list

git status
git add .
git commit -m "First commit"

git branch -M main
git status

git remote add origin https://github.com/parshuramnagappa16-lang/rahul.git
git remote -v

git push -u origin main

# Only if push is rejected because GitHub has existing commits
git pull origin main --no-rebase --allow-unrelated-histories

# After a successful pull/merge
git push -u origin main

git status
git log --oneline

# For future file updates
git add .
git commit -m "Updated files"
git push
