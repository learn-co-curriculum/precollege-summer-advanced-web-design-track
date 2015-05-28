# Lecture - Github Pages

## SWBATS
+ Use Github Pages to send their websites to family and friends

## Motivation/Why Should I Care?
Making web pages is really fun, but it's nice to be able to share them with family and friends. Luckily, Github makes it really easy for us to preview our sites using Github Pages!

## Lesson Plan

+ First, we need to initialize a git repository. In the command line from our main project directory, type `git init`. 
+ Next, let's commit our changes.
	+ `git add .` to add all of the files
	+ `git commit -m "a message about our changes"` to make the commit
+ Awesome, let's make a remote repository. 
	+ Go to github.com and click the "+" in the upper right hand corner. 
	+ Give your project the same name as your directory. 
	+ The description is optional.
	+ Choose public
	+ You don't need a README.
+ Nice work! Github now gives us great instructions to add this as a remote repository.
+ The first few lines we've already taken care of, but let's copy the line that begins `git remote add origin` and paste it into our command line.
+ Next, do `git push -u origin master`. We've now pushed our repository up to Github!
+ Lastly, we'll create a branch called `gh-pages`. From the terminal, type `git checkout -b gh-pages`
	+ add and commit your changes on this branch like we did before.
	+ push this branch to your remote repository by doing `git push origin gh-pages`
+ Your site should now be live - nice work! Go to your github repostiory and click settings - you should see a link to the live example. Feel free to share this with your family and friends!

## Conclusion/So What?
In just a few steps, we can publish a live site to the internet to share with family and friends. Nice work! 
