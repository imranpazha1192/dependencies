# dependencies
Installing Global Dependencies
‍
Node.js

Download Node.js from https://nodejs.org/en. The “main” LTS version is what we recommend.
Run the installer you just downloaded, and follow the prompts to install.
Node Version Manager (NVM)

Running the CLI app to contribute to the ceremony requires node version 16.20.

We’ll install nvm to change node versions by downloading a shell script using the following command in the terminal:

curl -sL https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.0/install.sh -o install_nvm.sh
This command downloads a file and might look like nothing happened.

Next we’ll install NVM by entering the following command in the terminal:

sh install_nvm.sh
You may need to accept license terms. If it tells you this is required, you will need to run the command it tells you in the terminal; on a mac this will likely be

sudo xcodebuild -license
You will need to follow the prompts, and then repeat the sh install_nvm.sh command again.

If it successfully installs, it will ask you to restart the terminal. If you have any other terminal windows open, first finish your work in them. Now, close the terminal (e.g. with ⌘Q), and re-open it by the same process as before (press ⌘<space>, type “Terminal” into the Spotlight Search bar that this opened, press <enter>).

‍

‍

Contributing to the Ceremony
‍
Step 1 - Create a temporary directory
‍

The first thing to do is to create a temporary directory (folder) to run the ceremony from. I’m going to name it ~/p0tion-tmp in these commands (i.e. a folder named p0tion-tmp in your home directory), but you’re welcome to choose a different name if you prefer.

In the terminal, type

mkdir ~/p0tion-tmp
then hit <enter>. That made your directory, now navigate into it, by typing in the terminal

cd ~/p0tion-tmp
‍

Step 2 - Switch to node v16.20
‍

Before we contribute let’s switch to node v16.20 which the ceremony relies on.

First install the version by entering the following command:

nvm install 16.20
Then use that version by entering:

nvm use 16.20
‍

Step 3 - Install phase2cli
‍

Now you will install the tool that runs the ceremony. Continuing in the terminal, type

npm i @p0tion/phase2cli
‍

Step 4 - Authenticate with GitHub
‍

As described above a GitHub account which meets certain conditions is required to contribute. To authorize your account enter the following command:

npx phase2cli auth
This will copy an authentication code to your clipboard, open your web browser, and take you to a GitHub site asking to give p0tion permission to use the “Gists” feature of your GitHub. Paste the contents of your clipboard into this website and click the button to authorize. GitHub will tell you “Congratulations, you’re all set!” and you can return to the terminal.

‍

Step 5 - Contribute!
‍

You’re ready to contribute to the ceremony. Back in the terminal, enter:

npx phase2cli contribute
You’ll be asked which ceremony to contribute to.

RISC Zero STARK-to_SNARK Prover ceremony should already be highlighted, so press <enter> to select it.

Now, you’ll be asked to choose how to add entropy — this is the secret data for you to destroy and forget (or ideally never know) to secure the ceremony. You can either have it randomly generated or create it manually.

Once you’ve added your entropy, you’ll be placed in the contribution queue. Contributions take a long time, so leave this running in the background or go do something else. (But don’t let your computer go to sleep, a sleeping computer can’t contribute!)

‍
