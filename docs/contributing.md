# Contribute

We treat Ansible Lightspeed demos just like we treat the Ansible Project.  Please help us!  Check out the [Issues](https://github.com/ansible/ansible-lightspeed-demos/issues) for a list of what we are working on.

## Table of Contents

- [Contribute](#contribute)
  - [Table of Contents](#table-of-contents)
  - [Pull Requests](#pull-requests)
  - [Create a fork](#create-a-fork)
  - [Stay in Sync](#stay-in-sync)
    - [Configuring Your Remotes](#configuring-your-remotes)
    - [Rebasing Your Branch](#rebasing-your-branch)
    - [Updating your Pull Request](#updating-your-pull-request)
  - [Create a pull requests](#create-a-pull-requests)
  - [Going Further](#going-further)
  - [Getting Help](#getting-help)

## Pull Requests

We take pull requests!  What is a pull request?

>Pull requests let you tell others about changes you've pushed to a branch in a repository on GitHub. Once a pull request is opened, you can discuss and review the potential changes with collaborators and add follow-up commits before your changes are merged into the base branch

More info on PRs: [https://help.github.com/en/articles/about-pull-requests](https://help.github.com/en/articles/about-pull-requests)

## Create a fork

Create a fork on your own Github project (or your personal space)

[Github Documentation on Forking a repo](https://help.github.com/articles/fork-a-repo/)

## Stay in Sync

It is important to know how to keep your fork in sync with the upstream Ansible Lightspeed Demos project.

### Configuring Your Remotes

Configure `ansible/ansible-lightspeed-demos` as your upstream so you can stay in sync

```bash
git remote add upstream https://github.com/ansible/ansible-lightspeed-demos.git
```

### Rebasing Your Branch

Rebase the branch on your fork

```bash
git pull --rebase upstream devel
```

Check your status

```bash
git status
```

### Updating your Pull Request

```bash
git push --force
```

More info on docs.ansible.com: [Rebasing a Pull Request](http://docs.ansible.com/ansible/latest/dev_guide/developing_rebasing.html)

## Create a pull requests

**PULL REQUESTS MUST BE MADE INTO THE `DEVEL` BRANCH**

Make sure you are not behind (in sync) and then submit a PR to the Ansible Workshops.  
[Read the Pull Request Documentation on Github.com](https://help.github.com/articles/creating-a-pull-request/)

Just because you submit a PR, doesn't mean that it will get accepted.  Right now the QA process is manual, so please provide details.

Being more descriptive is better, and has a higher change of getting merged upstream.  Communication is key!  Just b/c the PR doesn't get accepted right away doesn't mean it is not a good idea. We have to balance many different types of users.  Thank you for contributing!

## Going Further

The following links will be helpful if you want to contribute code to the Ansible Lightspeed demos project, or any Ansible project:

- [Ansible Committer Guidelines](http://docs.ansible.com/ansible/latest/committer_guidelines.html)
- [Learning Git](https://git-scm.com/book/en/v2)

## Getting Help

Please [file issues on Github](https://github.com/ansible/ansible-lightspeed-demos/issues).  Please be descriptive and fill out all required information.
