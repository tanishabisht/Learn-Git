# Set up name and email address


## 1. Setting up name and email address
Let git know your name and email address.
```
git config --global user.name "Tanisha"
git config --global user.email "agamyatani@gmail.com"
```

To see what email id you have configured your git with:
```
git config user.name
git config user.email
```



## 2. Installation Options line endings

Line endings are the special characters that tell the text editors "this is the end of the line". 

Windows and MacOS have different special characters.

Yes it's fine to convert them, it's just Visual Studio pointing out an inconsistency between the file and the operting system you're using and not converting them shouldn't cause any problems either.

```
git config --global core.autocrlf true
git config --global core.safecrlf warn
```



## 3. Create a git repository
`git init`: this creates an empty local repository in the current directory where the command was written.



## 4. Add and commit the changes
`git add .`: to stage the changes
`git reset .`: to unstage changes
`git commit -m "initial commit"`: to make use of version control and save the snapshot of current code in history



## 5. Check the status of the repository
`git status`: to check where the files are: i.e. local directory, staging area, local repository.