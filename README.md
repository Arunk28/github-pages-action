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
as  "homepage": "https://username.github.io/reponame"

6.go to actions > select node js template and paste the code which is mentioned below 

```
name: Build CI
on:
  push:
    branches:
      - master
jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout 🛎️
        uses: actions/checkout@v2
        with:
          persist-credentials: false

      - name: Install and Build 🔧
        run: |
          npm install
          npm run build
      - name: Deploy 🚀
        uses: JamesIves/github-pages-deploy-action@releases/v3
        with:
          GITHUB_TOKEN: ${{ secrets.<token key name here> }}
          BRANCH: gh-pages # The branch the action should deploy to.
          FOLDER: build # The folder the action should deploy.
          CLEAN: false
          
          ```
          

and made a commit

build will be in process 

that's it 

you can see your github page... :)
