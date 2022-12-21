# Git Studies

<h1>Remote Rep -> Local Machine</h1>
<hr>
<h2><code>git clone [remoteRepositoryURL].git</code></h2>
Copies files from remote repository to local machine. May use HTTP or SSH. 

<h2><code>git pull origin [branchName]</code></h2>
Updates the local machine code with the one present remotely. If no <code>origin branchName</code> has been specified, it uses the upstream. 

<h1>Local Machine</h1>
<hr>
<h2><code>git status</code></h2>
Gives info about changes that haven't been comitted yet.
Shows the ones that have been modified and untracked for those not known
(possibly added files). 

<h2><code>git add</code></h2>
To stage files (get them ready to be commited). Use <code>git add .</code> to add all of the untracked files listed
and to save changes. One may as well use <code>git add filename</code> to add individual files.

<h2><code>git reset</code></h2>
Unstages everything. 
If it is wished to unstage a single file, use <code>git reset [fileName]</code>.
In order to undo commits, use <code>git reset HEAD~1</code>. HEAD is a pointer to the last commit, and tilde is followed by a number that indicated how further back we want our last commit to be. 1 means that we want to return to the commit made before HEAD. 
To go back to a specific commit, type in <code>git reset [commitHash]</code>. The hash may be obtained with <code>git log</code>.
To make sure that what is undone is also undone on the files, and not just unstaged, use <code>git reset --hard [commitHash]</code>.

<h2><code>git commit -m "aString" -m "anotherString</code></h2>
Saves files to a commit (under a branch name).
Dash m stands for message. Along with the commit, an initial message is obligatory.
The second one is optional and fits inside the description box.
It is also possible to add and commit at the same time with <code>git commit -am "aString" -m "anotherString"</code>, but it only works with modified files (not untracked ones).

<h2><code>git log</code></h2>
Displays submitted commits, with info such as author name and associated hash (unique commit indetifier). Press space to load more and 'q' to leave. 

<h1>Local Machine -> Remote Rep</h1>
<hr>

<h2><code>git init</code></h2>
Uploads the current directory to a new git remote repository. Only works if the repository exists and an origin has been added with <code>git remote add origin [address specified]</code>.

#if it already exists
<h2><code>git push origin branchName</code></h2>
Saves to remote repository what is held on the local machine (all the commits yet to be pushed). If an origin and branch is mentioned, updates are made accordingly. Otherwise, it is all done regarding the currently set upstream (-u), which can be set with <code>git push -u origin [branchName]</code> (u stands for upstream). When creating new branches and pushing to them, it is necessary to take the upstream into consideration.

<h2><code>git pull</code></h2>
Makes a pull request.

<h1>Branches</h1>
<hr>
Allow for commits to be stored separately. Usually divided into <i>main</i>, <i>features</i> and <i>hotfix</i>.
Once done with the code of a certain branch, one may merge it with the main one.

<h2><code>git branch</code></h2>
Displays existing branches. The one the user is currently in will be shown with an asterisk next to it. 
If one wishes to delete a branch, use <code>git branch -d branchName</code>

<h2><code>git checkout [branchName]</code></h2>
Switches between branches. If one wishes to create a new branch, use <code>git checkout -b branchName</code>.

<h2><code>git diff [branchName]</code></h2>
Shows differences between the current branch and branchName. Press 'q' to leave.

<h2><code>git merge [branchName]</code></h2>
Merges the current branch with branchName. 
