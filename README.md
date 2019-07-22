# MkDocs Documentation deployment to Azure WebApp through the Travis CI.

This is demo source code to setup your static website on azure webapp using MKDocs and Travis CI as build tool.

**MkDocs installation:**
MkDocs is static site generator framework which work on base of python. For building site on local you need to install python by downloading from https://www.python.org/ ^v.3.6 in your computer. After python installation make sure that you have added its path to env variables.
For MkDocs installation you can follow the steps mention on https://www.mkdocs.org/#installation. Once MkDocs installation is complete you can clone and setup your repo.


Repository setup commands

git clone https://github.com/path-to-repo.git
cd repo name
git checkout branch_name

Now repository is set on your machine. You can do your changes in .md files now. To run and preview changes on local you can run MkDocs server on local by using the following commands.

mkdocs serve

**Setup Travis** 
Travis is the build tool we are using the build and deploy our site to gh-pages branch. For this we have integrated the Travis with our git-hub account. There is an web-hook added by Travis in git-hub for this repository which will get called on commit to master branch.

Got to https://travis-ci.org and login with your git-hub account. Travis will fetch list of all your git-hub repo. Now enable the switch in line of Documentation repository.
Go to repository settings in Travis and environment variable called 'git_token'. This variable is used in build process. This token need to be generated in git-hub under developer settings.
After commit to staging & master Travis build job should get triggered. Or you can find issues in build logs
Commit to staging will deploy site to git-hub pages and commit to master will deploy site to live ie azure webapp.
