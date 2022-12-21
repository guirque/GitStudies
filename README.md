# Testing

<h1>Remote Rep -> Local Machine</h1>
<hr>
<h2><code>git clone</code></h2
Copies files from remote repository to local machine.

<h1>Local Machine</h1>
<hr>
<h2><code>git status</code></h2>
Gives info about changes that haven't been comitted yet.
Shows the ones that have been modified and untracked for those not known
(possibly added files). 

<h2><code>git add</code></h2>
To add files to github. Use _git add ._ to add all of the untracked files listed
and to save changes. One may as well use _git add filename_ to add individual files.

<h2><code>git commit -m "aString" -m "anotherString</code></h2>
Dash m stands for message. Along with the commit, an initial message is obligatory.
The second one is optional and fits inside the description box.

<h1>Local Machine -> Remote Rep</h1>
<hr>

<h2><code>git init</code></h2>
Uploads the current directory to a new git remote repository. Only works if the repository exists and an origin has been added with <code>git remote add origin [address specified]</code>.

#if it already exists
<h2><code>git push origin branchName</code></h2>
Saves to remote repository what is held on the local machine. If an origin and branch is mentioned, updates are made accordingly. Otherwise, it is all done regarding a default location, which can be set with <code>git push -u origin branchName</code>.