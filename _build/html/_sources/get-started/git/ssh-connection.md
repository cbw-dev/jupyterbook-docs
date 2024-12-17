(ssh-connect)= 
# Setting Up Your SSH Connection

We need to create an SSH connection. You have already set this up if you have been git cloning, pulling from and pushing to GitHub. If you have, continue to [git cloning](git-clone). If you haven't, keep reading!

Essentially, we're doing these steps to be able to update and receive updates from our GitHub repository, with security!

Follow the following 3 main steps. Each of these subheaders links to GitHub's official docs, if you would prefer to follow them instead! (Below is the simplified version of the instructions, if you've already been working with GitHub/SSH connection and want to make a new one, consider using the official docs.) The official docs may be more up-to-date. 

```{note}
*If you do decide to use GitHub's docs,* ***choose the page*** *(the different tabs are clickable at the top of the page) that matches your operating system (Mac/Windows/Linux).*
```
```{tip}
You can do these commands anywhere in your files. You do not need to be in your home directory.
```

```{admonition} **Output VS Commands**
In our instructions (and the GitHub docs), output is prefaced by a "\>" sign.

In the GitHub instructions, commands start with "\$" sign. In Linux, the terminal tends to give you a "\$" to indicate where to run your command. Thus, GitHub uses a "\$" to indicate that what comes after is the command you should run. **The "\$" is not part of the command.** (We do not do this in our instructions).
```

### <a href="https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#generating-a-new-ssh-key)" target="_blank">Generating a new SSH key</a>

1.  Open Terminal.

2.  Copy and paste this text into your terminal. **Replace the email given below with your GitHub email address** (the email address you used to sign up for Github). *Keep the quotations in your command.* Press enter to run the command.

    ```bash
    ssh-keygen -t ed25519 -C "your_email@example.com"
    ```

    You will get this output:
    
    ```
    > Generating public/private ALGORITHM key pair.
    > Enter a file in which to save the key (/Users/YOU/.ssh/id_ALGORITHM):
    ```
    
    Press enter. (This uses a default file and default file location.)
    
    If you have already created a SSH key and you are asked to rewrite another key, look at the <a href="https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#generating-a-new-ssh-key:~:text=Please%20note%20that%20if%20you%20created%20SSH%20keys%20previously%2C%20ssh%2Dkeygen%20may%20ask%20you%20to%20rewrite%20another%20key%2C%20in%20which%20case%20we%20recommend%20creating%20a%20custom%2Dnamed%20SSH%20key.%20To%20do%20so%2C%20type%20the%20default%20file%20location%20and%20replace%20id_ALGORITHM%20with%20your%20custom%20key%20name." target="_blank">GitHub Docs</a> for specific steps.

3.  Type a secure passphrase (make up a password) when prompted with:
    
    ```         
    > Enter passphrase (empty for no passphrase): [TYPE YOUR PASSPHRASE]
    ```
    
    ```{important}
    **Before you freak out,** this passphrase is so secretive that you won't see it being typed. You won't see a cursor moving and you won't see ● instead of the characters you're typing. Rest assured, your computer is receiving your text.
    
    If you make a mistake, it's best to hit the "delete" bar many times, and retype. 
    ```

    ```
    > Enter same passphrase again: [TYPE THE SAME PASSPHRASE]
    ```
    
    ```{tip}
    You should keep note of this passphrase for your own use. We (should) never have to use it again after finishing these steps.
    ```
    
    You will get specific output telling you information about your public key and key fingerprint. This is specific to the SSH connection you just made!
    
### <a href="https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?platform=mac#adding-your-ssh-key-to-the-ssh-agent" target="_blank">[Linux/Mac] Adding your SSH key to the ssh-agent</a>

These are the instructions if you have a Linux or macOS computer. Go [here](windows-add-ssh-key) for the Windows instructions.

1.  In terminal, run the following command:

    ```bash         
    eval "$(ssh-agent -s)"
    ```

    You will get this output:

    ```         
    > Agent pid 59566
    ```
    
    *(Your number will most likely be different than the one above.)*

2.  If you're using macOS Sierra 10.12.2 or later additions, you need to modify your `~/.ssh/config` file.

    1.  Check if you have a `~/.ssh/config` file: Run the following command:

        ```bash
        open ~/.ssh/config
        ```

    2.  If you get the following output:

        ```         
        > The file /Users/YOU/.ssh/config does not exist.
        ```

        Create the file using the touch command: run the command given below

        ```bash         
        touch ~/.ssh/config
        ```

    3.  Edit your `~/.ssh/config` file using the following instructions. (You can use any text editor you would like, such as vim). Below we use nano as a text editor.

        -   Run `nano ~/.ssh/config`
        -   Add the following lines to this file.

        ```         
        Host github.com
         AddKeysToAgent yes
         UseKeychain yes
         IdentityFile ~/.ssh/id_ed25519
        ```

        -   Exit nano: `ctrl + X`
        -   Type "Y" and hit enter to save changes, when asked the following

        ```
        Save modified buffer (ANSWERING "No" WILL DESTROY CHANGES) ?
        ```

3.  Return to terminal. Run the following command:

    ```bash
    ssh-add --apple-use-keychain ~/.ssh/id_ed25519
    ```
    
    (You may be asked to enter your passphrase again. This is the same passphrase as before.)

(windows-add-ssh-key)=
### <a href="https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?platform=windows#adding-your-ssh-key-to-the-ssh-agent" target="_blank">[Windows] Adding your SSH key to the ssh-agent</a>

1. Right click on Windows Powershell (you can search for it in your search bar on your taskbar) and select "Run as administrator".

2. Run the following commands:

    ```bash
    Get-Service -Name ssh-agent | Set-Service -StartupType Manual
    ```
    ```bash
    Start-Service ssh-agent
    ```
3. Open a terminal window (without running as administrator). Run the following command, and **replace YOU with your GitHub username**:

    ```bash
    ssh-add c:/Users/YOU/.ssh/id_ed25519
    ```

### <a href="https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account#adding-a-new-ssh-key-to-your-account" target="_blank">Adding a new SSH key to your account</a>

1.  Copy the SSH public key: Run the following command to copy the content of the \~/.ssh/id_ed25519.pub file to your clipboard:

    **On Mac/Linux:**
    
    ```bash
    pbcopy < ~/.ssh/id_ed25519.pub
    ```
    
    **On Windows:**
    
    ```bash
    clip < ~/.ssh/id_ed25519.pub
    ```


2.  Go to your GitHub account on the <a href="https://github.com/" target="_blank">GitHub</a> website. Click on your profile picture (icon in the upper right). Then, select **Settings**.

3.  Under the "Access" section, click **SSH and GPG keys**.

4.  Click **New SSH key** or **Add SSH key**.

5.  In the "Title" field, add a descriptive label for this key you are creating (ex. if this is your personal laptop, you can call the key: "Personal Laptop").

6.  Leave the type of key as "authentication" (rather than "signing"). For our purposes, selecting authentication is fine.

7.  In the "Key" field, paste (we are pasting what we copied in step 1).

8.  Click **Add SSH Key**.

9.  If you are prompted, confirm access to your GitHub account.

Finally, we're all done! We've created a SSH connection between your device and GitHub!

Thankfully, we only need to do these steps once! Additionally, most security questions are only asked the first time, so when you work on your workshop in the future, you will not have to redo these steps or confirm authentication.