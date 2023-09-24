# Introduction

This entry will go over the workflow tools in GitHub, assigning a task from the issue list, and branching from the main 
to complete the issue then create a pull request.

# Workflow

We were given the task this week to decide on a standard team workflow that we should follow as a group when we work on
a GitHub issue, import the list of issues appointed to us into our group project, assign an issue to each person in
the group and complete it with the team workflow. Our standard team workflow is to create a branch to make changes to a
file or multiple files and then create a pull request to make sure everything is correct if any errors arise then the
changes can be reviewed and then the changes can be merged into the main branch. When we established the team workflow
we imported the list of issues into our group project, each issue is similar to the other, and the issues are formatted
like 'As a system administrator, I want to maintain reference values for (blank)'. Some examples are 'equipment types',
'continents', 'system types' etc. The goal for each issue is to be able to print the values out. Once the issues are
imported, an issue is then assigned to a person within the group and is moved from the to-do column in the task board to
the in-progress column. I then created changes within our repository in a branch that I created for me to fix the issue 
within and then once I created the solution I then made a pull request to later be merged into the main branch.

# Screenshots

<figure>
<img src="https://github.com/Guy-GC/GuyGCPortfolio/blob/main/images/Issue.PNG"
width="100%" alt="drawing"/>
<figcaption <b>Fig.1 - The Assigned Issue</b>
</figcaption>
</figure>

\
This screenshot shows the issue I was assigned, my profile picture is on the top left of the image which shows that it
was personally assigned to me and this task is in the 'in-progress' column. My issue is to maintain reference values
for alert types. Here is the [link](https://github.com/users/wardliii/projects/1/views/1) to the task board with the issue 
I was given.

<figure>
<img src="https://github.com/Guy-GC/GuyGCPortfolio/blob/main/images/Branch.PNG"
width="100%" alt="drawing"/>
<figcaption <b>Fig.2 - New Branch from Main</b>
</figcaption>
</figure>

\
This screenshot shows that I have used a different branch within our GitHub repository which is part of the standard team
workflow of creating a branch to make edits to the files within the repository and then making a pull request to eventually
merge the branches.

# Reflection

There are a few things looking back that I or the group could have done differently. Here are some changes looking back
that I would have done differently.

## Assigning Issues

One problem we ran into was that people were struggling to assign the issue and put the issue in the in-progress column.
This is because most people within the group aren't admins for the GitHub repository meaning they don't have permission
to move the tasks themselves, they need an admin to do it for them. What we could have done is if the admin of the
repository gave admin access to all the members of the group this wouldn't be an issue. However, there could be problems
if every member has admin access, if someone changes the repository it could lead to a lot of work to fix the issue.
If there is more than one admin it means that it doesn't rely on one person to change the issue to a different column.

## Main Branch

One problem we faced was that some people were working in the main branch and it took a long time to fix the main branch
template. An easy resolution is just to make sure everyone in the group is made aware to not change anything in the main
branch when making changes, some people might not know as they don't have a lot of experience with GitHub or it could have
been a mistake.

\
There is a way to automatically close an issue once the person who is assigned a task has merged their branch to the
main branch, this is done by using the keyword 'resolve' in the pull requests description followed up by the task number,
this case for me it is number 23. If the pull request description says resolve #23, it will resolve the issue automatically
once it has merged and you can resolve multiple issues in the one pull request. This can make the process of using the 
task board a lot easier.
