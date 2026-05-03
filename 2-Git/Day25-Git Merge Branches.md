# Day 25: Git Merge Branches
The Nautilus application development team has been working on a project repository /opt/cluster.git. This repo is cloned at /usr/src/kodekloudrepos on storage server in Stratos DC. They recently shared the following requirements with DevOps team:


Create a new branch devops in /usr/src/kodekloudrepos/cluster repo from master and copy the /tmp/index.html file (present on storage server itself) into the repo. Further, add/commit this file in the new branch and merge back that branch into master branch. Finally, push the changes to the origin for both of the branches.

## 🐛Task


## 🛠️Solution

```ssh natasha@ststor01```

```sudo su -```

```cd /usr/src/kodekloudrepos/```

```git status```

```ls```

```cd cluster/```

```git branch --list```

```git checkout -b devops```

```git branch --list```

```cp /tmp/index.html .```

```git add index.html```

```git commit -m "updateing index"```

```git checkout master```

```git merge devops master```

```ls```

```git push origin master```

```git push origin devops```






---
