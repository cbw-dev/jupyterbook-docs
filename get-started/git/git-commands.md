(git-commands)=
# Git Commands

Now we have a bunch of files locally! We can now make local edits, and then use **git commands** to get and receive updates from the repository on GitHub.

```{important}
Run these commands in your Terminal. You should navigate to **inside** your project folder (what you git cloned).

You will know that you're inside the correct folder if your *[pretext that appears before the command you write, forgot what it's called]* begins with the name of your workshop (and not "CBWGithub", for example).
```

```
git pull
```

This updates the edits that are on the repository on GitHub (online) into your local project. You are "pulling" updates from the GitHub.

For example, if someone on your workshop team made edits that are on the GitHub, you want those edits to already be made once you start making edits (or else we run into merge conflicts!). Thus, run `git pull`, and the edits will be made in your local folder!

```{dropdown} Ok, so how do we make edits and put them onto GitHub?
You will need to use all 3 of the following commands in consecutive order!
```

```
git add -A
```

`git add -A` "stages" **A**LL of your edits. This means that git is taking into account all your edits, such as new files, file edits, and deleted files.

```{note}
If you delete a file locally and use this command, it will also be deleted on GitHub, once you finish these 3 commands.
```

```
git commit -m "clear and concise summary of actions"
````

This command **commits** your changes. You can think of it as another step of "officializing" your edit. The text in quotations after `-m` is a message that is connected to this update you are about to make onto GitHub. You should put a concise and clear explanation of the edits you made!

```
git push
```

Finally, this confirms your changes and "pushes" them onto the GitHub. Now, everyone on your team can see your changes!

```{warning}
This puts your changes onto GitHub, but this won't update your live website - more on this in [](deploy).
```