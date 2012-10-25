git help
==========

# git problem 403

```bash
  969  git init
  970  touch README.md
  971  git add *
  972  git commit -m "add first"
  973  ll
  974  vi README.md 
  975  git commit -m "add first"
  976  git add *
  977  git commit -m "add first"
  978  git remote add origin https://github.com/buyhome/sRACS.git
  979  git push origin master
  980  git config --global github.user username
  981  git config --global github.user buyhome
  982  git remote add origin git@github.com:buyhome/sRACS.git
```

Problem 403

```bash
git push -u origin master

error: The requested URL returned error: 403 while accessing https://github.com/amalapk/pygame/info/refs

fatal: HTTP request failed

```

# solution 1

The GitHub Remote page mentions the read/write addresses for a repo:

Make sure your clone address is like:

https://github.com/username/yourRepo.git

And that you have defined:

git config --global user.name "Firstname Lastname"
git config --global user.email "your_email@youremail.com"

Should you use a git address (without ssh), you would also need:

git config --global github.user username
git config --global github.token 0123456789yourf0123456789token

(with your token coming from “Account Settings” > Click “Account Admin.”)

# solution 2

It's all in the remote.

Change your current remote from https://github.com/amalapk/pygame.git to git@github.com:amalapk/pygame.git and enjoy.

To do this... (assuming your current remote is called origin)

git remote set-url origin git@github.com:amalapk/pygame.git

