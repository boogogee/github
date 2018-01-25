# Git Hub Notes

I needed a place to put all of my notes on how to get started and use GitHub.

## Getting Started

First step it to actually install git on your machine.  For this writeup I will be using Debian/Ubuntu. Run the following command in your terminal.

`sudo apt-get install git`

You can verify that it's installed by running the following;

`which git` <- shows the location of the git command

Output: ```/usr/bin/git```

or

`git --version` <- shows the version of git installed

Output: ```git version 2.7.4```

Now you need to set the user and the email in the config file.  You can do this with these two commands.

```
git config --global user.name "Your Name"

git config --global user.email "youremail@example.com"
```

END
