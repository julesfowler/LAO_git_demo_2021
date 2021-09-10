# Git Demo Outline 

Most of this is based on the [Software Carpentry Materials](http://swcarpentry.github.io/git-novice/) for git -- which I
highly reccomend in one of those courses or just following along yourself. 

## Set up git on your machine 

```
$ git
```

```
$ git config --global user.name "Mr. Sir"
$ git config --global user.email "mrsir@iloveholes.com"
$ git config --global core.editor "vim/emacs/nano"
```

Would highly reccomend setting up your account with [SSH
keys](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh) and 
[Two Factor
Authentification](https://docs.github.com/en/github/authenticating-to-github/securing-your-account-with-two-factor-authentication-2fa/accessing-github-using-two-factor-authentication), instructions on that here: 


## Explore a repository you've cloned

```
$ git clone https://github.com/julesfowler/LAO_git_demo_2021.git
$ cd LAO_git_demo
$ git log
$ git status
$ touch dummy_file.txt
$ git status 
```

## Make your own repository 

```
$ cd my_fantastic_project
$ git status 
$ git init
$ git status
```

## Change your repository and record that change

```
$ touch dummy_file.txt 
$ echo "Some fantastic content in my new project!" >> dummy_file.txt
$ git status
$ git add dummy_file.txt
$ git status
$ git commit -m "No dummies here, only version control MASTERS."
$ git status
$ git log 
```


## Connect your repository to a remote via GitHub

```
$ # some fiddling on the GitHub side
$ git remote add <link_to_your_new_repo> 
$ git branch -M main
$ git push -u origin main
```

## Work with a collaborator

``` 
$ # invite your collaborator via GitHub
$ git checkout -b new_feature_dom
$ touch smart_file.txt
$ echo "VITAL content for this project!"
$ git add smart_file.txt
$ git commit -m "Important update for this demo!"
$ git push origin new_feature_dom
```


