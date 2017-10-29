#What is Git?
Git is the most advanced version control system, which has the largest number of users, and manages a large number of practical software projects.Branch is the core concept of Git, and Git Workflow is also based on branch operation.To be exact, Git is a distributed version control system.

#Why we need Git?
If you have written a long article with Microsoft Word, you must have had that experience:

Want to delete a paragraph, and fear of the future want to recover, can not find how to do?There is a way to save the current file as "save as"......" A new Word file, and then changed to a certain extent, and then "save as"......" A new file, so it changes all the way, and finally your Word document becomes like this:
<center>![](https://www.liaoxuefeng.com/files/attachments/0013848606651673ff1c83932d249118bf8fd5c58c15ca2000/0)</center>
After a week, you want to retrieve the deleted text, but it's hard to remember which file was saved before deleting it, so you have to find one file, which is really troublesome.

Looking at a pile of messy documents, want to keep the latest one, and then delete the other, and fear which day will be used, but also dare not delete, really depressed.

Git can solve this problem.

This software works just like this, and it can record every change in the file like this:

<center>![](https://wx3.sinaimg.cn/mw690/006AMixJly1fkzhf1i3e2j30ym06n0t6.jpg)</center>

##The advantage of git
- Version library localization, supporting offline submission, relatively independent, does not affect collaborative development.
- The contents are stored in metadata, and the library is completely cloned.
- It supports fast switching branch, facilitates merging, and has better combination performance.
- Distributed version library, without single point of failure, content integrity is good.

#How does it work?
Workflow or flow, which means water, is a metaphor for a project that flows smoothly and naturally like water, without shocks, collisions, or even eddies. Just like this:

<center>![](https://wx2.sinaimg.cn/mw690/006AMixJly1fkzhf1ftgaj30go04k0sk.jpg)</center>

There are two main features of it:

First, there are two long-term branches of the project.

>- master branch
>- develop branch

<center>![](https://wx1.sinaimg.cn/mw690/006AMixJly1fkzhf1i2v4j30ci0iuglt.jpg)</center>

The former is used to store the released version, which is distributed in a stable distribution at any time. The latter is used for daily development and storage of the latest development version.

Second, there are three short-term branches of the project.

>- feature branch
>- hotfix branch
>- release branch

Once they are developed, they are merged into develop or master, and then deleted.

<center>![](http://img.blog.csdn.net/20150616220653092?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQveWVhc3k=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center)</center>

##The operations of git
Before you use Git, you need to build a repository. You can use an existing directory as a Git repository or create an empty directory. Using your current directory as the Git repository, we just need to initialize it.

>- git init

Use our specified directory as the Git repository.

>- git init newrepro

###Add new file
We have a repository, but nothing. We can add files with the add command.

>- git add filename

You can use add... To continue adding task files.

###Submit version
Now that we've added these files, we want them to actually be stored in the Git repository. To this end, we submit them to the repository.

>- git commit -m "Adding files"

If you don't use -m, an editor will let you write your own annotation information. 

When we modify a lot of files without thinking about each add, and want commit to automatically submit local changes, we can use the -a logo.

>- git commit -a -m "Changed some files"

The -a option of the GIT commit command can submit all the modified or deleted documents that have been managed by git to the repository.

###Release version
We first cloned a repository from the server and uploaded it

>- git clone ssh://example.com/~/www/project.git

Now we can push it to the server after we modify it.

>- git push ssh://example.com/~/www/project.git

###Get files
If you have done the following push, the following command indicates that the current branch is automatically merged with the only one trace branch

>- git pull

Update from the non default location to the specified url.

>- git pull http://git.example.com/project.git

###Delete
If you want to delete files from the repository, we use rm.

>- git rm file

###Branch and merge
The branch is done locally, fast. To create a new branch, we use the branch command.

>- git branch test

The branch command doesn't take us into the branch, just creating a new branch. So we use the checkout command to change the branch.

>- git checkout test

The first branch, or the main branch, is called "master".

>- git checkout master

Changes to other branches are not reflected on the main branch. If you want to submit the changes to the main branch, you need to switch back to the master branch, and then use the merge.

>- git checkout master
>- git merge test

If you want to delete the branch, we use the -d identifier.

>- git branch -d test

#The last
That's all, how about that? Git is a very useful tool which help programmer a lot.










