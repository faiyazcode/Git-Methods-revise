# How to remove node_modules from git repository
Git methods
#How to remove node_modules from git repo.

1. Check for an existing .gitignore file in the project directory
```
ls -a
```

2. If your project directory has a .gitignore file -skip step 3. Otherwise, continue with:

create .gitignore file in the git repository
```
touch .gitignore
```
# Remove the node_modules directory
3.Open up the .gitignore and add the following line to the file
```
**/node_modules
```
4. Remove the node_modules folder from the git repository
```
git rm -r --cached node_modules (it take some time to clean up)
```

# Commit All changes
5- finally Commit all changes
```
git commit -m "Removed node_modules folder"
```
6- Push the chnages to the remote repo
```
git push origin main
```
7-Commit the .gitignore file
```
git add .gitignore
git commit -m "Updated the .gitignore file"
git push origin main
```
