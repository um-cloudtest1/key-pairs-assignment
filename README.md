Resources for this assignment:
1. https://docs.github.com/en/authentication/connecting-to-github-with-ssh/about-ssh
2. https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
3. https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account
4. https://docs.github.com/en/authentication/connecting-to-github-with-ssh/testing-your-ssh-connection
5. https://docs.github.com/en/authentication/connecting-to-github-with-ssh/testing-your-ssh-connection

You should already have a GitHub account and you should have joined the GitHub organization "UM-cloud-computing".

We assume that you have access to a git command line environment.  
If you are using MacOS or Linux, this is built-in. (You might need to install git.)

Here is a link to download Git for Windows.  https://git-scm.com/download/win
This should enable git commands in Windows PowerShell which you are encouraged to use instead of a GUI.

The first part of your assignment is to create an ssh ed25519 key pair and add the public key to your GitHub account.
Directions are provided in links 2 and 3 below.  The default file names for your newly created key pairs
$HOME/.ssh/ed25519 (private) and $HOME/.ssh/ed25519.pub (public).

Test your key according to the procedure given in resource item 4 above.

As an additional test, do an ssh clone of your version of this repository by first making sure that
your key is added to the ssh agent as in item 2, and then doing:

git clone git@github.com:UM-cloud-computing/key-pairs-assignment-<your_github_username>.git

For example, the username of my test account is "ahalwright1", and the command is:
git clone git@github.com:UM-cloud-computing/key-pairs-assignment-ahalwright1.git

This will create a local copy of your repository in a subfolder of the directory where you do the git clone command.

Deliverable:  Include your public key file in your git repository for this account, commit it,
and push it to GitHub.  The name of this public key file should be .ssh/ed25519.pub which is 
in the subfolder .ssh of your home directory.  To do this in the command line, do the following steps:
1.  Copy your public key file (probably $HOME/.ssh/ed25519.pub) into your repository folder.
2.  Add the file to git with "git add ed25519.pub".
3.  Do a commit with the command "git commit -a -m "Commit of file ed25519.pub"
4.  Do "git push origin".  (This will push this change to the GitHub version of the repository.)

When you have successfully done step 4, you have completed the second and final part of this assignment.

