# Student Notebook Assignment Workflow

1. Go to the github repo link
2. Press 'fork' to create a copy on your own github account:

![fork](http://i.imgur.com/Mz2kkE3.png)

3. Copy the clone URL of your own copy - it should include your github username

![clone url](http://i.imgur.com/6NO0SKN.png)

4. Log in to Jupyter and open a new terminal. Run `git clone <the url you copied>`
5. Complete the assignment. Make sure you save your changes!
6. Commit and push your files:
```sh
git add --all
git commit -m 'your commit message'
git push
```
7. On your fork of the repo on github, press the 'new pull request', then the 'create pull request' button

![new pr](http://i.imgur.com/YDhd71F.png)
![create pr](http://i.imgur.com/NxRqjA2.png)

8. Submit your pull request to complete the assignment! Make sure to set the title of the PR to your name - lastname firstname:

![pr dialogue](http://i.imgur.com/zp5AaDa.png)

9. Your code will be tested automatically, and once it's done will show either a green tick or red cross

![travis test](http://i.imgur.com/hNrYYS8.png)

# Teacher notebook assignment workflow
1. Go to the [AdaNCDS](https://github.com/AdaNCDS) org and press the 'New' button

![new button](http://i.imgur.com/9Q073Dq.png)

2. Add a name and description, and tick 'Initialize this repository with a README'. Create the repo.

![new repo page](http://i.imgur.com/ieaIH9f.png)

3. Copy the clone URL for your new repo

![clone url](http://i.imgur.com/ERkMb9q.png)

4. Open a terminal on Jupyter and clone the repo:
```sh
git clone <your clone url>
cd <assignment-name>
```
5. Create your assignment notebooks. Add instructions to README.md.
7. Add a `.travis.yml` file. Use this template:
```yml
language: python
python:
  - "3.6"
install:
  - "pip3 install --upgrade pip"
  - "pip3 install jupyter"
  - "pip3 install nbconvert"
script:
  - "jupyter nbconvert --to notebook --execute 'some_notebook.ipynb'"
```
If you have more than one notebook to test, duplicate the last line as many times as you need.

7. Back in your terminal (make sure you're in the right folder!), commit and push your changes:
```sh
git add --all
git commit -m 'write the assignment'
git push
```
8. Back on github, check your new files are all there
9. Go to https://travis-ci.org/ and sign in. Press '+' to link your new assignment:

![new travis project](http://i.imgur.com/H7a09DN.png)

10. Choose the AdaNCDS org:

![travis orgs](http://i.imgur.com/Z30sPTy.png)

11. Find your new assignment. If it's not there, you might have to sync your account.

![sync account](http://i.imgur.com/xwkrViw.png)

12. Once you can see your assignment repo, flick the switch to turn on Travis testing

![travis enable switch](http://i.imgur.com/XI2CMPt.png)

13. You're done! Test the assignment yourself, or copy the github url to share with your students.