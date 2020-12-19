## instructions on how to fork this repo

1. Log in to GitHub with your credentials (or someone elses!)

2. Navigate to https://github.com/robarnoldio/forkthisprojectsite/

3. Use the `fork` button in the upper right corner to get a project of your own that is based on this one.

Congratulations, you now have a publicly viewable project site. Your next task is to make it your own.

## instructions on how to modify it to be your own

### method one: online edits

This is the shortest, simplest way to get a working project page published publicly.

Every page is editable "through-the-browser." Click the icon that looks like a pencil, make changes to your pages.

When you're done, you'll commit those changes to the `master` branch by clicking the green *Commit Changes* button at the bottom of the edit page.

You can add new files to your project repo through the browser as well. From the root of your project site, click the *Add Files* button to upload a file of your choice (good for images) or edit a new fie (typically a markdown file with .md extension).

### method two: local edits and git push

This method gives you a local clone of your project repo. You can edit it with tools of your choice (VS Code is superb) and when you're done, push changes back to GitHub where they will be publicly viewable.

0. You may have new SSH keys--install your current *public* key on your GitHub profile:
 - click your profile icon in upper right
 - click settings
 - click SSH and GPG keys
 - Click the *New SSH Key* button
 - paste your public key in the window and submit by clicking the *Add SSH key* button

1. Create a directory on your system to hold this repo. I suggest ~/github/reponame.

2. `git init` in that directory to initialize the git repo.

3. Clone your forked project repo. Grab the URL for it by clicking the green *Code* button, then copying the URL in the https tab.

Then `cd` into your local project directory and `git clone URL` in your terminal

4. Make changes to your local copy!

Excellent material to add:
 - screenshots with descriptive captions
 - lessons learned
 - YAML files that you've commented
 - diagrams of your setup
 - your thoughts on CIA triad in this project
 - how you worked in a team
 - how you solved problems or escalated issues in this project
 - references you found valuable
 - I could go on all day...

5. If you have added files, you need to add them with `git add (names of new files)`

6. Commit your changes to the master branch locally with `git commit -m some comment`

7. Make it live on your GitHub profile with `git push`.

### super bonus: same as above, but in VS Code

Complete steps 0-3 just as shown above.

Then open files in VS Code and make your desired changes there.

VS Code needs to know your GitHub credentials--it should ask for that on the fly when you do a push.

Overview of the VS Code + GitHub workflow:

 - open your local files and make changes
 - save those changes locally. VS Code tracks those changes!
   - you will see unsaved changes as a blue badge on the explorer icon at upper left
 - commit your saved chages, with a comment, by clicking the Source Control icon at left
   - it looks like the git logo
   - uncommitted changes show as a blue badge on the source control icon
 - push your changes to GitHub by clicking the synchronize changes icon in the toolbar at bottom left
 - you may get prompted for credentials the first time

The sync button looks like this, and indicates the number of unsynced changes:
!["sync button"](/images/sync.png "sync button")

### Brief recap of steps to make changes with VS Code:
 - change it
 - save it
 - commit it (requires a commit message)
 - sync it