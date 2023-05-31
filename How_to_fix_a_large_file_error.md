# How to fix a "large file error"


git add .<br /><br />
git commit -m "added content"<br /><br />
git push<br /><br />
nano .gitignore   I added the directories with the large files<br /><br />
git commit -a -m "Remove large files from repository"<br /><br />
git filter-branch --force --index-filter "git rm --cached --ignore-unmatch static/current_project/Demo_of_MyTube_Flask_App.mp4 static/current_project/Demo_of_MyTube_Flask_App2.mp4" --prune-empty --tag-name-filter cat -- --all<br /><br />
git push origin --force --all<br /><br />

