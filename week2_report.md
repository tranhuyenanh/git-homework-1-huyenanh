# BAO CAO BAI TAP TUAN 2 - HUYEN ANH

## PART A

# A1: Create week2.md, commit, create and switch to week2 branch
touch week2.md
git add week2.md
git commit -m "Add week2.md"
git checkout -b week2

# A2: Simulate working on branch
echo "Noi dung 1" >> week2.md
git commit -am "working 1"
echo "Noi dung 2" >> week2.md
git commit -am "working 2"

# A3: Add line, commit, switch to master
echo "Noi dung 3" >> week2.md
git commit -am "Add new text line"
git checkout master
# Observation: File week2.md on master branch does not contain the new lines added in week2 branch because changes have not been merged yet.

# A4: Create week2b with 1 command, 3-way merge, delete week2
git checkout -b week2b
git merge --no-ff week2 -m "3-way merge week2 into week2b"
git branch -d week2

