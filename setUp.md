# Pre-session setup instructions

## GitHub

Please either check you can log in or set up a [GitHub](https://github.com/) account. We will use this host during the session to work with an example remote repository. I suggest you use an email you can take with you should you leave Bath.

## Git Installation & Verification

### 1. Check if Git Is Already Installed (All Operating Systems)

Before installing anything, check whether Git is already available on your machine.

**Open a command line:**

- **Windows**  
  - **Git Bash** (if already installed) **Command Prompt** or **PowerShell** from start menu
- **macOS**  
  - Open **native Terminal** (Applications → Utilities → Terminal) or **VS Code Terminal** (then Terminal → New Terminal)
- **Linux**  
  - Open your preferred terminal

**Run:**

```bash
git --version
```

**Possible outputs:**

If Git is installed:

```bash
git version 2.x.x
```

- Git is already installed  
- No need to reinstall, but never a bad idea to update to the most recent release
- **Windows:** confirm that Git Bash is available  
- **macOS / Linux:** proceed to configuration in Section 3

If Git is not installed (errors):

```bash
command not found
```

or on Windows:

```bash
'git' is not recognized as an internal or external command
```

In this case, follow the instructions below for your OS.

### 2. Installing Git (Based on the official [Git SCM book](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git))

#### 2.1 Windows

The simplest way to download git is to go to the official Git for Windows [download page](https://git-scm.com/download/win).

This distribution is known as Git for Windows and is technically a separate community project from git itself but is well maintained. It also contains **Git Bash** which is where we will interact with git from.

Most of the default install options are sensible or certainly should be kept.

If you have strong text editor preferences you may wish to change that (default Vim is fine).

I do suggest you **change the default initial branch name** to "main" which is the suggested override option when that window comes up.

**Verify your install:**

Open Git Bash (Start menu → Git Bash) and in this terminal run

```bash
git --version
```

If this outputs the latest version number, i.e.

```bash
git version 2.52.0
```

you have successfully installed git and Git Bash.

#### 2.2 macOS

Again there are several ways to go about this (git even comes as default on many macs) but the recommended way is to try to run git from the terminal (e.g. `git --version`).

If this command is not found it will prompt you to install the Xcode Command Line Tools which are useful and comes with git.

It is also possible to use a more specific installer (e.g. the hombrew package manager). Instructions for this may be found [here](https://git-scm.com/install/mac).

**Verify your install:**

Open a new terminal instance and run

```bash
git --version
```

If this outputs the latest version number, i.e.

```bash
git version 2.52.0
```

you have successfully installed git.

#### 2.3 Linux

The package management tool on your Linux system will suffice to download git. For a Fedora or similar system (e.g. CentOS) use `dnf`,

```bash
dnf install git-all
```

while for a Debian based system (i.e. Ubuntu) use `apt`

```bash
sudo apt-get install git
```

Further options with specifics for different distributions are available [here](https://git-scm.com/install/linux).

**Verify your install:**

Open a new terminal instance and run

```bash
git --version
```

If this outputs the latest version number, i.e.

```bash
git version 2.52.0
```

you have successfully installed git.

### Configuration

Before we go ahead and use git it's useful to configure the details you would like used in commit messages. The `config` command sets these parameters via `git config --global <key> <value>`. git options can be configured globally (--global) or locally
in a repository (--local). Initially I suggest setting the below two options.

```bash
git config --global user.name "Paul Dirac"
git config --global user.email "paul@grumpygenius.com"
```

Their correct setting can be checked by

```bash
git config --global -l
```

## Congratulations

You are now ready to learn the basics of version control using `git`!