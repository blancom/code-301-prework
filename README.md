# Code 301 Pre-work: Intermediate Software Development

## Computer Setup

## Install Atom

If you haven't already, install [Atom](https://atom.io). If you have used an advanced text editor like Sublime Text, then Atom will feel familiar to you. Atom is free, open-source, cross-platform, and has a wide array of useful plug-ins available. Please use Atom during Code 301. (If you are proficient with another text editor that you *love*, you may use that instead, but please note that your instructional team may not be able to assist with debugging any issues with your editor)

[Atom's documentation](https://atom.io/docs/latest) is top-notch. Review it now to familiarize yourself with the basics. Make sure you're looking at the docs for the latest version. If you find that you are unable to call atom in the terminal, you may need to enable shell commands through Atom by first opening it through your graphical desktop interface, and selecting `Install Shell Commands` in the drop-down menu.

----

## Install Node

*Note*: If you get an error while installing these packages such as "try again as root/administrator", you may need to use the `sudo` command to get administrator access. For example `sudo apt-get install nodejs`.

#### Linux instructions

  To install Node, open your Terminal and copy and paste the following line, then hit Enter:

  `sudo apt-get install nodejs`

  Afterwards, you'll want to install Node Package Manager (NPM).

  `sudo apt-get install npm`

  If you run into issues trying to install Node from these steps, please contact your instructor.

#### Mac instructions

  If you took Code 201, you should already have Homebrew installed. If you have not, follow the guide on [this page](https://github.com/codefellows/code-201-prework/blob/master/prework/mac/2_homebrew.md#install-homebrew).

  To install Node, open your Terminal, and enter:

  `brew update && brew install node`

#### Windows instructions

  To install Node, go [here](https://nodejs.org/en/download/), and then download and run the Windows Installer. Make sure you do not deselect any of the Node components such as NPM during the installation.

### Verify the Node installation
Now let's verify that it is installed. Enter the following into your terminal:

`node -e 'console.log("works")'`

You should get a response that says "works". If not, try reinstalling Node again. If you are still having issues, please contact your instructor.

----

## Install eslint and live-server Node packages

Now that you have Node installed, you can install Node packages using its package manager, **NPM**. Open your Terminal (Git Bash on Windows) and enter:

`npm -g i eslint live-server git-open`

You should see a lot of feedback as it installs.

### Verify the Node packages installation
Now let's verify that it is installed. Enter the following into your terminal:

`npm list -g --depth=0`

You should get a list back that includes `live-server` and `eslint`.

![](http://i.imgur.com/1ITioP1.png)

----

### What is this linter thing?

Linting is the process of running a program that will analyze code for potential errors. It is an important part of the quality assurance process.

> `lint` was the name originally given to a particular program that flagged some suspicious and non-portable constructs (likely to be bugs) in C language source code. The term is now applied generically to tools that flag suspicious usage in software written in any computer language.

That means the linter is your friend! It will help you write syntactically correct code, so you can catch errors in your text editor, rather than having to hop over the browser, refresh your page, and search for errors. Faster feedback makes for happier developers (that's you!).

## Install linter and linter-eslint Atom packages

For this next part, you will have Atom's package manager **apm** install some packages. Go [here](https://atom.io/docs/v0.194.0/using-atom-atom-packages#command-line) to verify it's enabled. Once you have verified that apm commands will work, enter this on your Terminal:

`apm install linter linter-eslint`

You should get two success messages while it installs the linter and linter-eslint packages.

### Verify the Atom packages installation

Enter the following into your Terminal:

`apm ls`  
You should get back a long list, and at the end you should receive a list of packages you installed for Atom.   
Linter and linter-eslint should be on that list, like in this screen shot:

 ![screen shot 2016-05-28 at 11 33 31 pm](https://cloud.githubusercontent.com/assets/12869788/15631728/a816191c-252c-11e6-8cb4-5c757f240a50.png)

 ----

## Install PostgreSQL Database Software
*Please note that if you have a previously installed version of PostgreSQL on any operating system, you should be aware of any username and password that you've set for that installation. If you're unsure please uninstall and reinstall a fresh copy, which will also install the latest stable version. Additionally, if you are using a version before 9.5, you should uninstall and reinstall. You will be unable to complete certain labs if you are using version 9.4 or previous!*


For both Windows and Linux users, please follow the default installation instructions taking care not to change values such as the default port numbers (You may be prompted to change them, but should also be given default values).

### Windows

*For reference, these instructions are taken from the following documentation: http://www.postgresqltutorial.com/install-postgresql/*

**NOTE: If you are running Windows 8 or 10, you need to create a Windows user with administrator role e.g., postgres and use this user to run the installation file.**

- Your **Default** database super user is: *postgres*
- You will be asked to enter and confirm a database password.
- **Be sure you document your default user and password**, as you will need them later in the course. We are working securely on your computer, so a simple password like `1234` will suffice, and there's no need to change the default user.

**There are three steps to complete the PostgreSQL installation**:

1. Download PostgreSQL installer for Windows
1. Install PostgreSQL
1. Verify the installation

**Downloading the installer**

- Go to the PostgreSQL [official website](http://www.postgresql.org/download/windows/).
- Click on the [download installer from EnterpriseDB](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads#windows). Choose the latest version to download. It takes a few minutes to complete the download.

**Installing**

Double click on the installer file. An installation wizard will appear and guide you through multiple steps where you can choose different options that you would like to have in PostgreSQL. For now, just select default values.

**Verify Installation**

When you installed PostgreSQL, the installer also installed some extra tools. One of them is psql (it may be called SQL Shell).

- Launch psql.
- When it prompts you for input, just hit enter to select default values until it asks for a password. You will put in the password you entered during installation.
- You should have a window that [looks like this](http://www.postgresqltutorial.com/wp-content/uploads/2012/08/psql.png).
- In this window, you can enter SQL statements, which must all end with semicolons. Congratulations, you've installed correctly!

**If you are having issues with the installation, please contact your instructor.**

### Linux

*For reference, these instructions are taken from the following documentation: https://www.postgresql.org/download/*

- If asked to provide or set a username and password, **be sure to document the username and password**, as you will need them later in the course.
- `sudo apt-get install postgresql`
- You will be prompted with the message that a certain amount of disk space will be used and asked if this is OK. Type `y`, then hit enter.
- Several commands will automatically run, this may take a few minutes.
- **You will likely NOT be prompted for a default username or password.** You will need to set one in psql if this is the case.

**Verifying Installation And Setting A Password**
- You should be able to run the command `sudo -u postgres psql`. You will be asked for your administrator password - this is what you usually enter when you run `sudo` commands. This will log you into the psql prompt as the user postgres.
- You should now have a prompt that looks like `postgres=#`. You can run SQL commands from here, which must end in semicolons.
- If you were not prompted for a default user or password, we will set one using psql. If you type `\du`, you can get a list of users associated with PostgreSQL. You should see a single user, `postgres`. In order to give this user a password, enter the following command: `ALTER ROLE postgres PASSWORD 'your-password-here';`, replacing "your-password-here" with whatever you want it to be. Remember that your password must be wrapped in quotes. *Don't forget the semicolon*.
- If successful, you will receive the feedback `ALTER ROLE`.

**If you are having issues with installation, please contact your instructor.**

### MacOS

You should have already verified during the Node installation that you have Homebrew installed. Please see that section above for more details if not.

To install PostgreSQL, open your Terminal, and enter:
`brew update && brew install postgresql`

This will create a user for you, that matches your logged in user account. Run the `whoami` command in the terminal if you aren't sure what that is. This user has a blank password set as the default.

*You will need to run this command whenever you first start your computer and open up the terminal in order to start your Postgres server:*

`pg_ctl -D /usr/local/var/postgres/ -l /usr/local/var/postgres/server.log start`

Since that's rather verbose, we can set it as an alias!

`alias pgstart='pg_ctl -D /usr/local/var/postgres/ -l /usr/local/var/postgres/server.log start'`

However, aliases are temporary. You would need to set that alias each time you opened up a new terminal window. Instead, we can tell our system to always set that alias whenever a terminal is opened. Find your **.bashrc** or **.bash_profile** file - it will probably be in your home (~) directory. Run `atom .bashrc` or `atom .bash_profile` to open it up, then on a new line, paste this in:

`alias pgstart='pg_ctl -D /usr/local/var/postgres/ -l /usr/local/var/postgres/server.log start'`

Now, whenever you first start up your computer, you just have to run `pgstart` to get your Postgres server running.

If, for some reason, the `pgstart` command is not available when you open a new window, you should be able to run `source .bashrc` or `source .bash_profile` (wherever you put the alias), then `pgstart` should be available.

## ALL USERS: Startup and Create some databases

1. Login to psql.
  - For Mac, run your new `pgstart` alias, then type `psql`.
    - If the response is, "Can't find database *yourUserName*", run `createdb -U yourUserName`, then run `psql` again.
  - For Windows, open up your psql program (SQL Shell)
  - For Linux, run `sudo -u postgres psql`
2. You should be at a prompt that looks like `postgres=#`
3. Enter the following command: `CREATE DATABASE kilovolt;`. *Note the semicolon. If you forget it, your prompt will go to a new line and look like* `postgres-#`. *This means you have an unterminated command and the prompt will just keep going to new lines until you enter a semicolon*.
  - You should receive the feedback "CREATE DATABASE".
4. Now enter: `CREATE DATABASE portfolio;`. This should mirror the above step.
5. Verify that your databases were created by running `\l` (no semicolon). You should see a list of databases, including `kilovolt` and `portfolio`. You should be able to connect to a database by running `\c DATABASE_NAME`, e.g. `\c kilovolt` or `\c portfolio`.

Congrats! You're all done. Well, except for your class-specific directory instructions :wink:
