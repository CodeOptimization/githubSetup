# SSH Connection Setup
Using the SSH protocol, you can connect and authenticate to remote servers and services. Users could eliminate typing ID & password by setting up ssh connection with github. Here are steps that I used to set up my Mac.

## Pre-request:
Have git software installed on your mac.(This also lead to me another problem).

## Establishing Connections:

1. Checking for existing SSH keys.
  * Open Terminal.
  * Enter __$: ls -al ~/.ssh__ to see if existing SSH keys are present:
  * Check the directory listing to see if you already have a public SSH key. If not, Step 2, else step 3.

2. Generating SSH Key.
  * Terminal command: __$: ssh-keygen -t rsa -b 4096 -C "your_email@example.com"__
  * __Enter a file in which to save the key (/Users/you/.ssh/id_rsa): [Press enter]__
  * __Enter passphrase (empty for no passphrase): [Type a passphrase]__
  * __Enter same passphrase again: [Type passphrase again]__
  
3. Adding your SSH key to the ssh-agent.
  * __$: eval "$(ssh-agent -s)"__
  * If you're using macOS Sierra 10.12.2 or later, you will need to modify your ~/.ssh/config file to automatically load keys into the ssh-agent and store passphrases in your keychain.
        Host *
         AddKeysToAgent yes
         UseKeychain yes
         IdentityFile ~/.ssh/id_rsa
  * Add your SSH private key to the ssh-agent and store your passphrase in the keychain. If you created your key with a different name, or if you are adding an existing key that has a different name, replace id_rsa in the command with the name of your private key file.
    __$ ssh-add -K ~/.ssh/id_rsa__
4. Adding a new SSH key to your GitHub account.
  * __$ pbcopy < ~/.ssh/id_rsa.pub__, this means "Coping the contents of the id_rsa.pub file to your clipboard"
  * In the upper-right corner of any page, click your profile photo, then click __Settings__.
  * In the user settings sidebar, click __SSH and GPG keys__.
  * Click __New SSH key__ or __Add SSH key__.
  * In the "Title" field, add a descriptive label for the new key. For example, if you're using a personal Mac, you might call this key "Personal MacBook Air".
  * Paste your key into the "Key" field.
  * Click __Add SSH key__.
  * If prompted, confirm your GitHub password.
5. Testing your SSH connection.
  * Terminal command: __$ ssh -T git@github.com__, then you may see some warnings, type "yes", you will have it connected.
  
## What If You Have Two Github Accounts.

## Updating Repository

## About My Mac's Problem
Before I set up my SSH connection with GitHub, I had installed Git months ago. I left my previous Github account ID and email to the Git setting information. So by this time, after I pushed any updates, the __git log__ and webpage file show that was finished by my previous account.

  * Solution: I just simply updated my ID and email information 
        you can also see your Git username in the Git configuration file in your HOME directory on Unix systems, i.e., this file:

        1. Terminal $ vim ~/.gitconfig
        2. The out put will be:
            ...
            name = PreviousID
            email = PreviousEmail@gmail.com
            ...
        3. Update, then save your update.

  
### Reference: 
  * https://help.github.com/articles/connecting-to-github-with-ssh/
  * https://help.github.com/articles/setting-your-commit-email-address-in-git/
  * https://alvinalexander.com/git/git-show-change-username-email-address
  * https://www.atlassian.com/git/tutorials/learn-git-with-bitbucket-cloud
  * https://unix.stackexchange.com/questions/10525/how-to-use-which-on-an-aliased-command
  
