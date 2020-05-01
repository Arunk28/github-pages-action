This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Github Actions + Github Pages + Create react app

## Steps to create github pages
1.install the create react app from npm 
refer the link
https://github.com/facebook/create-react-app

2.add branch gh-pages from master

3.go to profile > settings > create personnal token and copy that 

4.create to the repo settings > secrets > paste the token in value and name it for the token as KEY

5.goto package.json and add the value in  that file
as  "homepage": "https://username.github.io/repo name"

6.go to actions > select node js template and paste the code which is mentioned below link
https://gist.github.com/Arunk28/21bdb8e11902c98c84f61edb18ed4964#file-githubpages-deploy

and made a commit

build will be in process 

that's it 

you can see your github page... :)
