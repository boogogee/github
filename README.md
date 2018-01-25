# Git Hub Notes

I needed a place to put all of my notes on how to get started and use GitHub.  I am not a GitHub master by any means, I am writing this to solidify the few things that I know and to learn a lot more.  The object is to do 90% from the command line.  

## Prerequisites

Create a GitHub account and log in.  Make sure you use a strong password and enable 2FA.  Also, add your SSH pub key so that we can make pull/push/clone/etc requests using SSH not HTTPS.   

## Getting Started

First step it to actually install git on your machine.  For this writeup I will be using Debian/Ubuntu. Run the following command in your terminal.

`$ sudo apt-get install git`

You can verify that it's installed by running the following;

`$ which git` <- shows the location of the git command

Output: ```/usr/bin/git```

or

`$ git --version` <- shows the version of git installed

Output: ```git version 2.7.4```

Now you need to set the user and the email in the config file.  You can do this with these two commands.

```
$ git config --global user.name "Your Name"

$ git config --global user.email "youremail@example.com"
```

## First Repository

Navigate to your home directory and create a directory to house all of your repos.

```
cd

mkdir repos

cd repos

mkdir test

cd test
```

Now that you have a home for your repository it's time to log in to GitHub and add one.  Technically you could do this using the API but for simplicity we will create it from your profile in GitHub.  Create a public repository named `test`.  Now lets set it up from the command line.  
END
