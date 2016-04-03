# [Hack Oregon](http://www.hackoregon.org/) - Urban Development project
# Getting started as a contributor

**Table of Contents**

1. <a href="#introduction">Introduction</a><br>
2. <a href="#motivation">Motivation</a><br>
3. <a href="#workflow">Work flow</a><br>
4. <a href="#process">Process description</a><br>
5. <a href="#glossary">Glossary</a><br>
6. <a href="#references">References</a>

## <a name="introduction">1. Introduction</a>
The purpose of this document is to help you get started as a contributor for [Hack Oregon](http://www.hackoregon.org/)'s Urban Development project. "Contributor" often means one who writes code, but technical writers and business analysts may also be contributing documents, so "contributor" is more general and more appropriate in this case than "software developer" or "programmer". Team membership is always in a state of flux with people coming and going, each with their own unique history of development experience. We hope this documentation will provide consistency over time as team membership changes. Another benefit for those of you with little development experience is that this process is widely used by other developers on open source projects and on commercial software projects. So developing with the Urban Development team will prepare you to work on other teams in the future. We did not make this process up, so we are going to point you off to documents that have already been written by other teams that follow this process.

## <a name="motivation">2. Motivation</a>

You might be wondering why it has to be so complicated to contribute code. There would be a lot less overhead if you could just clone the repository, make changes, and then push the changes to the _origin_ repository. That works great when you are working by yourself or with only a couple of other people with whom you have a close relationship. However, working on a big team with the team membership changing frequently requires a different process, in order to assure a quality process for maintaining the code.

## <a name="workflow">3. Work flow</a>

There are two independent aspects to the workflow we follow for contributing code to the project. The first part is the branching policy, which gives guidelines for when to make new branches and when to merge branches. The blog post by Vincent Driessen, [A successful Git branching model](http://nvie.com/posts/a-successful-git-branching-model/), provides good diagrams that exemplify the process for branching and merging. Atlassian documentation of [Gitflow Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) is also quite good.

The second part of the process is the steps that are necessary because we use GitHub for our central repository. There is no standard "pull request" in Git, so each of the major repository hosting vendors, e.g. [GitHub](https://github.com/) and [Bitbucket](https://bitbucket.org/), have their own way of implementing pull requests. In the steps below, we refer to GitHub documentation for managing workflow within a team.

## <a name="process">4. Process description</a>

The specification of [Git workflow](https://wiki.diasporafoundation.org/Git_workflow) for the Diaspora* Project is an excellent explanation of the mechanics of using Git in the way that we do it for the Urban Development project. Read that document first, starting with the [Step-by-step (the short version)](https://wiki.diasporafoundation.org/Git_workflow#Step-by-step_.28the_short_version.29) section and then come back here if you still need more explanation, especially if you are new to Git and/or GitHub.

Follow the links to articles that describe each step in detail. See the Glossary for definitions of italicized words and phrases.

1. Sign up for a [GitHub](https://github.com/) account.

2. [Fork](https://help.github.com/articles/fork-a-repo/) a Hack Oregon _project repository_ into your _personal GitHub repository_.

3. Clone your _personal GitHub repository_ to your local development machine. We call that cloned repository your _local repository_. By convention, Git refers to the original repository as the 'origin' for your _local repository_. See the explanation in the GitHub Guide ["Fork a repo"](https://help.github.com/articles/fork-a-repo/).

4. Configure your _local repository_ to reference the Hack Oregon _project repository_ as your 'upstream' remote repository. See the explanation in the GitHub Guide ["Fork a repo"](https://help.github.com/articles/fork-a-repo/).

5. Starting from the 'develop' branch in your _local repository_, create a new branch when you are ready to make changes to existing files or create new material. Name that new branch something descriptive for the feature you are adding, such as "read-config-files".

6. Commit your changes on that branch as often as necessary until you have completed your unit of work.

7. [Synchronize your _local repository_](https://help.github.com/articles/syncing-a-fork/) with the Hack Oregon ('upstream') repository. Other development may have been committed to the _project repository_ while you have been working on your branch, so you will want to merge from the _project repository_ master to your branch, in order to keep in-sync.

8. Push the branch from your _local repository_ to 'origin', your _personal GitHub repository_.

9. [Create a pull request](https://help.github.com/articles/using-pull-requests/) from the branch in your _personal GitHub repository_ to the 'develop' branch in the _project repository_.

10. Someone in the project with "committer" privileges will review your pull request. They may merge it as-is or they may suggest changes to you. If necessary, return to step 6 to keep improving your contribution and update your pull request.

## <a name="glossary">5. Glossary</a>

A _[pull request](https://help.github.com/articles/using-pull-requests/)_ is a process where you request another developer to review a branch of your code to be merged into the 'develop' or 'master' branch of the central repository for your project.

A _repository_ holds code as it is developed. There are three interconnected repositories as you contribute to the Urban Development project.

* _local repository_ is the term we use in this documentation as the git repository on your local, personal development machine. It is cloned from your _personal GitHub repository_, which in Git is called, 'origin', by convention.

* _personal GitHub repository_ is the repository associated with your GitHub account. It is forked from the _project repository_.

* _project repository_ is the repository in Hack Oregon's GitHub account which holds the history of all work that has been done. Git conventions call this the 'upstream' repository of your _local repository_. Code from this repository is deployed to the different deployment environments, such as testing, staging, and production.
  * Urban Development [front end](https://github.com/hackoregon/urbandev-frontend) repository
  * Urban Development [back end](https://github.com/hackoregon/urbandev-backend) repository

## <a name="references">6. References</a>

### GitFlow references
The Diaspora* Project. [Git workflow](https://wiki.diasporafoundation.org/Git_workflow). Accessed 2016-03-02.

Atlassian. [Gitflow Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow). Accessed 2016-03-02.

GitHub help. [Fork A Repo](https://help.github.com/articles/fork-a-repo/). Accessed 2016-02-27.

GitHub help. [Syncing a fork](https://help.github.com/articles/syncing-a-fork/). Accessed 2016-02-27.

GitHub help. [Using pull requests](https://help.github.com/articles/using-pull-requests/). Accessed 2016-02-27.

GitHub Guides. [Understanding the GitHub Flow](https://guides.github.com/introduction/flow/). Accessed 2016-02-27.<br>"This guide explains how and why GitHub Flow works."

Vincent Driessen. 2010. [A successful Git branching model](http://nvie.com/posts/a-successful-git-branching-model/). Accessed 2016-02-27.<br>This is the original blog post that introduced the GitFlow model.

### Other references for using [git](https://git-scm.com/)

GitHub Guides. [Mastering Markdown](https://guides.github.com/features/mastering-markdown/). Accessed 2016-02-27.<br>The document that you are reading is formatted with Markdown syntax. So if you are going to edit this document, you should learn to use Markdown.

[Git Reference Manual](https://git-scm.com/docs). Accessed 2016-02-27.

Scott Chacon and Ben Straub. 2014. [Pro Git](https://git-scm.com/book/en/v2), 2nd edition. Accessed 2016-02-27.

[How to undo (almost) anything with Git](https://github.com/blog/2019-how-to-undo-almost-anything-with-git). Accessed 2016-03-02.
