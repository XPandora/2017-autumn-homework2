#Git Workflow

![](http://nvie.com/img/git-model@2x.png)

#INTRODUCTION
##Workflow
>A workflow consists of an orchestrated and repeatable pattern of business activity enabled by the systematic organization of resources into processes that transform materials, provide services, or process information. It can be depicted as a sequence of operations, declared as work of a person or group, an organization of staff, or one or more simple or complex mechanisms.(from Wikipedia)

##Git workflow
- Git workFlow is a workflow for branching that can be used for doing development work.
- Centralized Workflow
- Feature Branch Workflow
- Gitflow Workflow
- Forking Workflow

##Branches(in Git-flow)
###Historical Branches
- The main branch is the core branch of all development activities.

![](http://upload-images.jianshu.io/upload_images/54009-70ef16000c0832b0.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#####Master Branch
- The storage on the master branch should be the code in Production Ready state.
#####Develop Branch
- Develop branch is the branch to save the latest development results.


###Assistant Branches
- Assistant branch is the branch which is used to organize solving kinds of specific problems in software development activities
![](http://upload-images.jianshu.io/upload_images/54009-7265a72025bddb1a.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#####Feature Branch
- Feature branch is usually used when developing a new software funtion.

#####Release Branch
- Release branch is designed for publishing new product versions.

#####Hotfix Branch
- In addition to being created outside of the plan, the hotfix branch is very similar to the release branch: both can produce a new version of the software available for deployment in the production environment.

#WHY GIT?
1. Ability to document version control and multi person collaborative development
2. It has strong branch characteristics, so it can be flexibly developed with different workflow
3. A distributed version control system, even if the collaboration server downtime, can continue to submit code or file to the local warehouse, when the collaboration server returned to normal work, then the local warehouse to warehouse remote synchronization
4. When a member of a team completes a function, it notifies other team members through the pull request operation, and the other team members can merge the code after review code


#HOW WORK?
###For Centralized Workflow
1. From central repository clone to local repository — git clone
2. Edit files and submit updates in the local repository— git add&git commit
3. fetch updated commit in central repository to local repository and rebase onto updated commit - git fetch&git rebase/git pull --rebase
4. push local master branch to central branch

![](http://www.techug.com/wordpress/wp-content/uploads/2015/07/6941baebjw1esuqsmka98j20tm0yagmx.jpg)

###For Feature Branch Workflow
1. Use central repository and main branches to record the history of official projects
2. Developers create a new branch every time they develop new functions — git checkout -b
3. Push Feature branches to central repository - git push
4. Send pull request to ask the administrator to merge to the main branch
5. Publish new function to central repository

![](http://www.techug.com/wordpress/wp-content/uploads/2015/07/6941baebjw1esuqskspf8j20yg0byq3h.jpg)

###For Forking Workflow
1. There is an official public repository on the server
2. The developer fork official repository creates its copy, and then stores it on the server
3. When developers are ready to publish local commit, they push commit into their own public repository
4. Send a pull request to the official repository in your own public repository
5. The maintainer pull contributor's commit to his own local repository
6. Review the code to make sure it doesn't destroy the project and merge it into the master branch of the local repository
7. Push master branch to offcial repository on the server
8. Other developers should synchronize with the official repository

![](http://www.techug.com/wordpress/wp-content/uploads/2015/07/6941baebjw1esuqs7u6n5j20wy0eswfv.jpg)


#Conclusion
> If you’re fighting Git’s defaults, ask why. 
> 
> Treat public history as immutable, atomic, and easy to follow. Treat private history as disposable and malleable.
> 
> The intended workflow is:
> 
> 1.Create a private branch off a public branch.
> 
> 2.Regularly commit your work to this private branch.
> 
> 3.Once your code is perfect, clean up its history.
> 
> 4.Merge the cleaned-up branch back into the public branch.

 
