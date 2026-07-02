# Getting Started with Git & GitHub

This tutorial will walk you through:

1. Checking if `git` is already installed
2. Installing `git` (Mac, Windows, Linux)
3. Creating a GitHub account
4. Configuring `git` with your identity

Make sure to follow the steps that apply to your computer's operating system. 

---

## 1. Checking for `git`

Most Mac and Linux machines come with `git` pre-installed. Windows usually does not, so you'll likely need to install it.

1. Open a terminal (Mac/Linux) or command line application (Windows — see note below).
2. Type the following command and press enter:

```
git --version
```

3. Check the result:
   - If you see something like `git version 2.42.0`, git is already installed. You can skip to [Section 3](#3-creating-a-github-account).
   - If you see an error like `command not found` or `'git' is not recognized`, you'll need to install it — continue to [Section 2](#2-installing-git).

**How do I launch a terminal?**
- **Mac:** Open the `Terminal` app (search for it with Spotlight — `Cmd + Space`, then type "Terminal").
- **Linux:** Open your distribution's terminal application (varies by desktop environment, often `Ctrl + Alt + T`).
- **Windows:** Open `PowerShell` or `Command Prompt` (search for either in the Start menu). After installing git (below), you'll also have the option to use `Git Bash`, which may be more intuitive since it uses the same commands as Mac/Linux.

---

## 2. Installing `git`

Follow the instructions for your operating system.

### macOS

You have a few options — pick whichever is easiest for you.

**Option A: Xcode Command Line Tools (simplest)**

1. In Terminal, run:
   ```
   xcode-select --install
   ```
2. A pop-up will appear — click "Install" and accept the license agreement.
3. Once it finishes, verify with `git --version`.

**Option B: Homebrew (if you already use or want to use Homebrew)**

1. If you don't have [Homebrew](https://brew.sh/) installed, install it first by running the command on their homepage.
2. Then run:
   ```
   brew install git
   ```

### Windows

1. Download the installer from [git-scm.com/download/win](https://git-scm.com/download/win) (the download should start automatically).
2. Run the downloaded `.exe` file.
3. Click through the installation wizard. The default options are fine - just keep clicking "Next" and then "Install."
   - One setting worth noting: when asked to choose the default editor used by git, pick something you're comfortable with (e.g., Notepad or VS Code).
4. Once installation finishes, open **Git Bash** (search for it in the Start menu) or Command Prompt/PowerShell, and verify with:
   ```
   git --version
   ```

### Linux

Installation depends on your distribution's package manager.

**Debian / Ubuntu (`apt`):**
```
sudo apt update
sudo apt install git
```

**Fedora (`dnf`):**
```
sudo dnf install git
```

**Arch Linux (`pacman`):**
```
sudo pacman -S git
```

After installation, verify with:
```
git --version
```

---

## 3. Creating a GitHub account

GitHub is a website that hosts `git` repositories online so you can back up, share, and collaborate on code.

1. Go to [github.com](https://github.com) and click **Sign up**.
2. Enter your email, create a password, and choose a username.
   - Pick a username you'd be comfortable showing to a future employer — many researchers end up linking this account to their CV.
3. Verify your email address using the code or link GitHub sends you.

---

## 4. Configuring `git` with your identity

Before making commits, tell `git` who you are. This information gets attached to every change you save. Run these two commands in your terminal, replacing the name and email with your own (use the same email as your GitHub account):

```
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
```

You only need to do this once per computer.

### Authenticating with GitHub

When you try to push code later, GitHub will ask you to authenticate. The easiest method for beginners:

1. Install the [GitHub CLI](https://cli.github.com/) (`gh`), **or** use the credential manager that comes bundled with Git for Windows/Mac.
2. Run:
   ```
   gh auth login
   ```
   and follow the prompts (choose GitHub.com, HTTPS, and log in via your browser).

Alternatively, GitHub will prompt you to log in through a browser window automatically the first time you push — follow the on-screen instructions if that happens.
