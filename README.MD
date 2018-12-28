# WebGoat - A deliberately insecure Web Application

## Introduction

WebGoat is a deliberately insecure web application maintained by [OWASP](http://www.owasp.org/) designed to teach web application security lessons.

**WARNING 1:** *DO NOT DEPLOY THIS APPLICATION*

This project was cloned from https://github.com/WebGoat/WebGoat.git

## Instructions for initial clone from public GitHub
Instructions taken from https://stackoverflow.com/questions/10065526/github-how-to-make-a-fork-of-public-repository-private#30352360:

### 1. Create a new repo 
```
git clone --bare https://github.com/WebGoat/WebGoat.git
cd WebGoat.git
git push --mirror https://github.com/whateverany/web-goat.git
cd ..
rm -rf WebGoat.git
```

### 2. Clone the private repo so you can work on it:
```
git clone https://github.com/whateverany/web-goat.git
cd web-goat
make some changes
git commit
git push origin master
```

### 3. To pull new hotness from the public repo:
```
cd web-goat
git remote add public https://github.com/WebGoat/WebGoat.git
git pull public master # Creates a merge commit
git push origin master
```
