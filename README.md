# GitHub Quick Start

I needed a place to put all of my notes on how to get started and use GitHub.  I am not a GitHub master by any means, I am writing this to solidify the few things that I know and to learn a lot more.  I want to provide the commands to run but also explain why you are running them.  The object is to do 90% from the command line.  

## Prerequisites

Create a GitHub account and log in.  Make sure you use a strong password and enable 2FA.  Also, add your SSH pub key so that we can make pull/push/clone/etc requests using SSH not HTTPS.   

## Getting Started

First step it to actually install git on your machine.  For this writeup I will be using Debian/Ubuntu. Run the following command in your terminal.

`$ sudo apt-get install git`

You can verify that it's installed by running the following;

`$ which git` <- shows the location of the git command

Output: `/usr/bin/git`

or

`$ git --version` <- shows the version of git installed

Output: `git version 2.7.4`

Now you need to set the user and the email in the config file.  You can do this with these two commands.


`$ git config --global user.name "Your Name`   <- Sets your name in the config

`$ git config --global user.email "youremail@example.com"`   <- Sets your default email in the config

## First Repository

Navigate to your home directory and create a directory to house all of your repos.

`cd`    <- Move to your home dir

`mkdir repos`  <- Create a dir in your home

`cd repos`   <- Move to the new dir

`mkdir test`  <- Create a dir for your first repo

`cd test`   <- Move to the new dir

Now that you have a home for your repository it's time to log in to GitHub and add one.  Technically you could do this using the API but for simplicity we will create it from your profile in GitHub.  Create a public repository named `test`.  On the next screen you should see a "Quick setup" section, save the SSH link to this new repo.  It will look something like this: `git@github.com:username/test.git`.  Now lets set it up from the command line, you should be in your `test` dir.

`$ git init`  <- Creates an empty Git repository

We need to add a new remote so we can make pull/push requests. We will use the `git remote add` command and pass two arguments with it, the remote name (typically `origin`) and the SSH link you saved from when you made the repo.  The command should look like this:

`$ git remote add origin git@github.com:username/test.git`

You can see if it worked by running:

`$ git remote -v` <- Verbose output showing the remote url after name

Output Should look like this:

```origin	git@github.com:username/test.git (fetch)

origin	git@github.com:username/test.git (push)
```

Now we need content to push to the repo.  We will start with a simple `README.md` file.  Use your favorite text editor to create the file (vim, vi, nano, etc)

`$ nano README.md`

Now that you made the file lets add some content, you can add anything you want or just copy and paste the following:

```
# Hello World

Testing my first repository

## GitHub uses markdown to format text.

You can create a new line by adding a blank line after blocks of text.

Like this.

You can also add `code` with back ticks and blocks with triple back ticks.
```

END
