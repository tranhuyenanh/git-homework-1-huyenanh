# BAO CAO BAI TAP TUAN 2 - HUYEN ANH

## PART A

1: Create week2.md, commit, create and switch to week2 branch
touch week2.md
git add week2.md
git commit -m "Add week2.md"
git checkout -b week2

2: Simulate working on branch
echo "Noi dung 1" >> week2.md
git commit -am "working 1"
echo "Noi dung 2" >> week2.md
git commit -am "working 2"

3: Add line, commit, switch to master
echo "Noi dung 3" >> week2.md
git commit -am "Add new text line"
git checkout master
Observation: File week2.md on master branch does not contain the new lines added in week2 branch because changes have not been merged yet.

4: Create week2b with 1 command, 3-way merge, delete week2
git checkout -b week2b
git merge --no-ff week2 -m "3-way merge week2 into week2b"
git branch -d week2


## PART B
1. Create wip branch, add wip.txt, commit, switch to master and merge week2b:
   git checkout -b wip
   touch wip.txt
   git add wip.txt
   git commit -m "Add wip.txt"
   git checkout master
   git merge week2b

2. Filter merged and unmerged branches:
   git branch --merged
   git branch --no-merged

3. Delete week2b branch:
   git branch -d week2b

4. Rename wip to work-in-progress and push to GitHub:
   git branch -m wip work-in-progress
   git checkout work-in-progress
   git push -u origin work-in-progress


## PART C
1. Add text to wip.txt and commit on work-in-progress:
   git checkout work-in-progress
   echo "Adding new progress content for Part C" >> wip.txt
   git add wip.txt
   git commit -m "Update wip.txt in work-in-progress branch"

2. Command to show branches with upstream and ahead/behind info:
   git branch -vv

3. Push branch and open Pull Request:
   git push origin work-in-progress
   # Created Pull Request from work-in-progress to master on GitHub UI.


## PART D
1. Create experiment branch and make 2 commits:
   git checkout master
   git checkout -b experiment
   touch exp1.txt && git add exp1.txt && git commit -m "Add exp1.txt"
   touch exp2.txt && git add exp2.txt && git commit -m "Add exp2.txt"

2. Switch to master and make 1 commit:
   git checkout master
   touch main_file.txt && git add main_file.txt && git commit -m "Add main_file.txt on master"

3. Rebase experiment onto master:
   git checkout experiment
   git rebase master

4. Explain rebase in week2.md:
   Added linear history explanation to week2.md.

5. Fast-forward merge experiment into master:
   git checkout master
   git merge experiment

6 & 7. Push master branch and week2.md to GitHub:
   git push origin master

