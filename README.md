# git_assignment_HeroVired (by Revanth)




Greetings,

Assignment is completed based on understanding/knowledge I aquired so far. 

Repository Path -> https://github.com/iamrevanth/git_assignment_HeroVired

Respective program files will be, CalculatorPlus.py and geoCalc.py.

Commands used for respective activity are documented below. 



=== Question 1 - CalculatorPlus  =====

git branch
git branch dev
git checkout dev # go to branch folder
git commit -m "Rev Calc python code"
git push 

git checkout -b feature/sqrt
-- make changes to .py file
git add .\CalculatorPlus.py
git push 
git commit -m "sqrt code added"

-- pull request from feature/sqrt to dev



=== Question 2 - LFS  =====

-- AHF-LINUX_v24_7.zip

git lfs install
git lfs track "*.tar"
git lfs track "AHF-LINUX_v24_7.zip"

git add AHF-LINUX_v24_7.zip

git commit -m "AHF-LINUX_v24_7.zip"
git push

-- optional --

git add .gitattributes *.zip *.tar
git lfs ls-files


---- output -----
git_assignment_HeroVired> git commit -m "AHF-LINUX_v24_7.zip"
[lfs 766cf1b] AHF-LINUX_v24_7.zip
 1 file changed, 3 insertions(+)
 create mode 100644 AHF-LINUX_v24_7.zip
PS D:\Revanth\Hero Vired Cloud-Devops Certificate Program\Devops\GitHu

git push
---- output -----
git_assignment_HeroVired> git push
Uploading LFS objects: 100% (1/1), 308 MB | 2.9 MB/s, done.
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 458 bytes | 458.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To github.com:iamrevanth/git_assignment_HeroVired.git
   cdd2ee5..766cf1b  lfs -> lfs
   


=========== Task 3 - geometry-calculator ========


git branch -b geometry-calculator
git add README.md
git push --set-upstream origin geometry-calculator
git add geo-calc.py
git commit -m "Geo Commit"

-- make changes to .py file
git stash

git pull origin geometry-calculator

\git_assignment_HeroVired> git stash        
Saved working directory and index state WIP on feature/circle-area: dfc98db GeoCal

PS D:\git_assignment_HeroVired> git stash list
stash@{0}: WIP on feature/circle-area: 46b8f28 Geo Calc

git_assignment_HeroVired> git stash
Saved working directory and index state WIP on feature/rectangle-area: e5a6754 Rectangle Area

PS D:\git_assignment_HeroVired> git stash list
stash@{0}: WIP on feature/rectangle-area: e5a6754 Rectangle Area
stash@{1}: WIP on feature/circle-area: 46b8f28 Geo Calc

git stash apply 1

git_assignment_HeroVired> git push --set-upstream origin feature/circle-area
To github.com:iamrevanth/git_assignment_HeroVired.git
 ! [rejected]        feature/circle-area -> feature/circle-area (non-fast-forward)
error: failed to push some refs to 'github.com:iamrevanth/git_assignment_HeroVired.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
