## The correct answer is to create an orphan branch. 

 
 Before starting, upgrade to the latest version of GIT. To make sure
 you’re running the latest version, run
 
     which git
 
 If it spits out an old version, you may need to augment your PATH with
 the folder containing the version you just installed. 
 
 Ok, we’re ready. After doing a cd into the folder containing your git
 checkout, create an orphan branch. For this example, I’ll name the
 branch “mybranch”.
 
     git checkout --orphan mybranch
 
 Delete everything in the orphan branch
 
     git rm -rf .
 
 Make some changes
 
     vi README.txt
 
 Add and commit the changes
 
     git add README.txt
     git commit -m "Adding readme file"
 
 That’s it. If you run
 
     git log
 
 you’ll notice that the commit history starts from scratch. To switch
 back to your master branch, just run
 
     git checkout master
 
 You can return to the orphan branch by running
 
     git checkout mybranch
