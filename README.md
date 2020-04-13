## What is version control?

Version control allows you to keep track of your work and helps you to easily explore the changes you have made, be it data, coding scripts, notes, etc. You are probably already doing some type of version control, if you save multiple files, such as `Dissertation_script_25thFeb.R`, `Dissertation_script_26thFeb.R`, etc. This approach will leave you with tens or hundreds of similar files, making it rather cumbersome to directly compare different versions, and is not easy to share among collaborators. With version control software such as [Git](https://git-scm.com/), version control is much smoother and easier to implement. Using an online platform like [Github](https://github.com/) to store your files means that you have an online back up of your work, which is beneficial for both you and your collaborators.

Git uses the command line to perform more advanced actions and we encourage you to look through the [extra resources we have added at the end of the tutorial later](#command_line), to get more comfortable with Git. But until then, here we offer a gentle introduction to syncing RStudio and Github, so you can start using version control in minutes.

## What are the benefits of using version control?

Having a GitHub repo makes it easy for you to keep track of collaborative and personal projects - all files necessary for certain analyses can be held together and people can add in their code, graphs, etc. as the projects develop. Each file on GitHub has a history, making it easy to explore the changes that occurred to it at different time points. You can review other people's code, add comments to certain lines or the overall document, and suggest changes. For collaborative projects, GitHub allows you to assign tasks to different users, making it clear who is responsible for which part of the analysis. You can also ask certain users to review your code. For personal projects, version control allows you to keep track of your work and easily navigate among the many versions of the files you create, whilst also maintaining an online backup. 

## How does version control work?

### What is a repository?

You can think of a repository (_aka_ a repo) as a "master folder", everything associated with a specific project should be kept in a repo for that project. Repos can have folders within them, or just be separate files.

You will have a local copy (on your computer) and an online copy (on GitHub) of all the files in the repository.

### The workflow

The GitHub workflow can be summarised by the "commit-pull-push" mantra.

1. Commit
	* Once you've saved your files, you need to commit them - this means the changes you have made to files in your repo will be saved as a version of the repo, and your changes are now ready to go up on GitHub (the online copy of the repository).
2. Pull
	* Now, before you send your changes to Github, you need to pull, i.e. make sure you are completely up to date with the latest version of the online version of the files - other people could have been working on them even if you haven't.
3. Push
	* Once you are up to date, you can push your changes - at this point in time your local copy and the online copy of the files will be the same.

Each file on GitHub has a history, so instead of having many files like `Dissertation_1st_May.R`, `Dissertation_2nd_May.R`, you can have only one and by exploring its history, you can see what it looked at different points in time.

## GitHub etiquette

If you'll be sharing the repository with collaborators and even for your own benefit, it's a good idea to define some rules on how to use the repository before we start working within it - for example what GitHub and coding etiquette should people be following? Is there a prefered folder structure, file naming system?

We can't repeat it enough: __always `Pull` before you `Push`.__ `Pull` means that you are retrieving the most recent version of the Github repository onto your local branch - this command is especially useful if several people are working within the same repository - imagine there was a second script examining soil pH along this elevation gradient, and your collaborator was working on it the same time as you - you wouldn't want to "overwrite" their work and cause trouble. In this case, you are the only one working on these files, but it's still good to develop the practice of pulling before you push. Once you've pulled, you'll see a message that you are already up to date, you can now push! Click on `Push`, wait for the loading to be over and then click on `Close` - that was it, you have successfully pushed your work to Github!

## Potential problems

Sometimes you will see error messages as you try to commit-pull-push. Usually the error message identifies the problem and which file it's associated with, if the message is more obscure, googling it is a good step towards solving the problem. Here are some potential problems that might arise:

### Code conflicts

While you were working on a certain part of a script, someone else was working on it, too. When you go through commit-pull-push, GitHub will make you decide which version you want to keep. This is called a code conflict, and you can't proceed until you've resolved it. You will see arrows looking like `>>>>>>>>>` around the two versions of the code - delete the version of the code you don't want to keep, as well as the arrows, and your conflict should disappear.

### Pushing the wrong files

If you accidentally push what you didn't intend to, deleted many things (or everything!) and then pushed empty folders, you can revert your commit. You can keep reverting until you reach the point in time when everything was okay. This is an easy way out if you're the only person working in the repository - __be aware that if there are other people that have committed to the repository, reverting will also undo all of their work, as reverting refers to the repository as a whole, not just your own work in it.__

Using these "undo" commands can be daunting, so make sure you read up on the different commands before you attempt anything that may delete work permanently: [here's a starter](https://www.atlassian.com/git/tutorials/undoing-changes/git-revert). It's a good idea to regularly back up your repository to an external hard drive _juuuust_ in case!

### Sync and interact with your repository through the command line
{: #github4}

Traditionally, Git uses the command line to perform actions on local Git repositories. In this tutorial we ignored the command line but it is necessary if you want more control over Git. There are several excellent introductory guides on version control using Git, e.g. [Prof Simon Mudd's Numeracy, Modelling and Data management guide](http://simon-m-mudd.github.io/NMDM_book/#_version_control_with_git), [The Software Carpentry guide](https://swcarpentry.github.io/git-novice/), and this [guide from the British Ecological Society Version Control workshop](https://github.com/BES2016Workshop/version-control). For more generic command line tools, look at this [general cheat sheet](https://www.git-tower.com/blog/command-line-cheat-sheet) and this [cheat sheet for mac users](https://github.com/0nn0/terminal-mac-cheatsheet). We have also created a table and flow diagram with some basic Git commands and how they fit into the Git/Github workflow. Orange lines refer to the core workflow, the blue lines describe extra functions and the green lines deal with branches:
