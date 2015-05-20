### Objective
Students will understand the purpose of git and github, understand how to commit locally and push to a remote repository

###SWABTS

+ GIT - `add` and `commit` files to local repository
+ GITHUB - `push` and `commit` to a remote repository
+ GITHUB - Submit a pull request

### Motivation / Why Should You Care?
It’s time to bring all of your individual pieces of the student project together. To do that we are going to need to track your progress locally in `git`, then push up your code to Github so we can add all of your individual submissions to our directory.

### Lesson Plan
+ Git and Github aren't the same thing
  * Github: where we save our code in the cloud, while `git` is a version control system that lives on your computer.
  * You use `git` from the command line, like when you cloned a lab to your computer using `git clone`
+ in terminal, enter `git status`. Like saying "hey git whats up?"
  * Any files edited will show up in red
+ Want all files to go on Github, so `git add file_name`.
  * If it's a lot of files `git add .` will add everything
  * The `.` means everything in the current directory
+ Enter `git status`: now says files that are ready to be committed.
  * we call this the "staged" files
+ Commiting is like taking a snapshot of your entire codebase
  * Video game analogy: when you hit a certain level, your level is saved, so when you die you don't end the game, you just roll over to that level. commits save the state of your code, so when it breaks you can rewind back to the working version
+ In terminal: `git commit -m "summary of work"`
  * Summary is helpful because lets future you and other developers your working with understand why you made a change
+ `git remote -v`: tells us where on Github.com the code will live
+ In terminal `git push`. Sends code to Github. Go to the repository on Github and it will show all the code
+ Pull request: Jr. Devs can't submit code without review.
  * To submit a pull request, shout “PULL REQUEST” at the top of your lungs. Github will then submit a pull request for you. Make sure you shout loud, because github is not based in New York City.
  * Click the `Pull Request` button in the top right corner and confirm.
  * Sends a notification to the owner of the repo that you have new content you would like them to review and `pull` into their version

### Conclusion / So What?
This is the exact workflow for developers at every tech company. Every time you get work done, you git add, commit and push to save the state of your work. Then to get your code pulled into a master code base we have to get it approved. This means sending a notification. Look [real world projects use this flow](https://github.com/jquery/jquery/pull/2268)

### Useful Metaphors
+ Airplane analogy: Process of putting code on Github is similar to a plane taking off: first individual passengers get on, then plane pulls away from the terminal, then takes off
