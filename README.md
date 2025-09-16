## Work in progress.

What I need to cover here:

- Basic Git
  - Fork, Clone, collaborate
  - Commit, Push, Pull

# ASU SER315 Group Project Template

Introduction

### Contents

1. [What Is This Repository](#1-what-is-this-repository)
2. [Why This Exists](#2-why-this-exists)
3. [File Structure](#3-file-structure)
4. [How to Use This](#4-how-to-use-this)
5. [Basic Git](#5-basic-git)
   1. [Project Setup](#51-project-setup)
      1. [Set Up Git User and SSH Key](#511-set-up-git-user-and-ssh-keysh-key)
      1. [`git fork`](#512-git-fork)
      1. [`git clone`](#513-git-clone)
   2. [Collaboration](#52-collaboration)
      1. [`git pull`](#521-git-pull)
      2. [`git commit`](#522-git-commit)
      3. [`git push`](#523-git-push)
   3. [Further Git Resources](#53-further-git-resources)

---

## 1. What Is This Repository

This repository is a template for your group project in SER315, containing
overviews of all the artifacts you'll be creating over the rest of the course,
as well as some tutorials on how to use tools and technologies you may be
unfamiliar with. It is set up with group collaboration in mind, with all
covered and recommended tools being specifically chosen to maximize the
ability for your team to work as one to complete this design.

All of the tutorials and guides contained here are very surface level and only
provide you with the minimum set of tools needed to complete this project, but
they are all extremely powerful in their own right, widely used in the
industry, and are worth learning further.

One special mention is [Git](https://git-scm.com/), the tool that GitHub is
built around. Git is a version control software that is nigh-on ubiquitous in
use, and using this template will give you an opportunity to get some very
basic familiarity with it before it comes into broader use in SER316 and
beyond.

The additional tools that will be covered here are
[Markdown](https://www.markdownguide.org/) and
[Mermaid](https://mermaid.js.org/), with more specific instructions on each
for [VSCode](https://code.visualstudio.com/) and
[IntelliJ IDEA](https://www.jetbrains.com/idea/).

---

[Return to Top](#asu-ser315-group-project-template)

---

## 2. Why This exists

This template was built because we identified a need in a collaborative
workflow for this courses project. In previous iterations, Astah UML was the
program of choice for this project, and deliverables were created and shared
over Google Docs. While Google Docs was great for collaboration, Astah was
most certainly not. Teams would end up splitting up the diagramming work, and
as a result, members would be missing whole diagrams at a time, and if any
needed to be updated, then that one member with the diagram would have to do
it. That single point of failure is not great, and it can cause some tensions
that we really want to avoid.

Since the refresh of this course by Dr. Mehlhase and Dr. Jain, additional
elements were added to the project that included coding features of the
design. This felt like a great opportunity to give students a resource for
managing that, along with a set of guides that would enable collaboration and
unify how we think about working together on software into our future courses.

Ultimately, this template and repository exists to familiarize you with tools
and workflows that you will be incorporating more officially in future
courses, while also giving you a solid and tested workflow for collaboration.

---

[Return to Top](#asu-ser315-group-project-template)

---

## 3. File Structure

This project is organized out of the box into four directories:
`/deliverables`, `/diagrams`, `/img_resources`, and `/src`. Additionally, this
README is in the root of the directory and serves as your entry point into
the project. There is also a `.gitignore` file that filters unnecessary files
from being uploaded to this repository.

#### [`/deliverables`](/deliverables/)

Inside this directory there are templates for all four of the deliverables
you will be responsible for over this course. They include sections for each
of the elements you are tasked to provide for that deliverable, with space for
your reflections.

These are all Markdown files which can be edited in any code editor, including
Notepad, VSCode, IntelliJ IDEA, etc. Included in this folder is a file
called
[`_deliverables_instructions.md`](/deliverables/_deliverables_instructions.md)
that contains more information on each section of the deliverable documents,
as well as a brief overview of Markdown, basic syntax, and features useful
to this project (embedding images, exporting PDFs).

#### [`/diagrams`](/diagrams/)

This directory contains a file
[`_diagrams_instructions.md`](/diagrams/_diagrams_instructions.md) and a
sub directory [`/examples/`](/diagrams/examples/).

The instructions file contains instructions and guides for creating the
various UML diagrams you will need for this project using Mermaid. Mermaid
is a code-based diagraming tool that can render a wide variety of charts
and diagrams from a few lines of code. What makes that nice is that it plays
well with our version control systems like Git, and it is easily edited and
maintained by the whole team at all stages of the project. The instructions
also contain guides on how to export the diagrams to images
for later embedding into the deliverables.

The `examples` folder contains example diagrams for the three types of
diagrams required for this project for you to learn from.

#### [`/img_resources`](/img_resources/)

This directory contains images that are used in these guide documents, but
can also be used to store your deliverable's images as well.

#### [`/src`](/src/)

This directory comes with two files to start:
[`README.md`](/src/README.md) and
[`src_instructions.md`](/src/src_instructions.md). `README.md` is a file you
will fill out for later deliverables to explain to the instruction staff how
to set up and run your software.

`src_instructions.md` contains guides for setting up a Java project from
scratch without IDE assistance or starter code snippets, and also contains
guides on easier ways to manage building and running your code as you develop
it, with a focus on VSCode and IDEA workflows, but those are absolutely
optional.

---

[Return to Top](#asu-ser315-group-project-template)

---

## 4. How to Use This

You will be creating a copy of this template into your own GitHub account
by [forking](#511-git-fork) it. Then, you and your team mates will collaborate
on the many artifacts required for the project, by using a variety of
[basic git](#5-basic-git) features.

There are two basic ways to interact with the repository: local editing
(recommended), and through the GitHub interface in your browser (not
recommended).

---

### 4.1 Local Editing

To work on this project by having a copy on your local machine, you will first
need to install [Git](https://git-scm.com/downloads). This will come with
the CLI tools for Git (and importantly for Windows, Git Bash).

Optionally, you can install a Git GUI client such as
[GitHub Desktop](https://github.com/apps/desktop) that will give you an easy
interface for using Git and GitHub.

I personally recommend getting comfortable with the command line interface
for Git when starting out to get a feel for what these UIs are abstracting
away, but even I use UI implementations (VSCode and IDEA both have Git UI
implementations that are really great).

Once that is done, you'll [`git clone`](#512-git-clone) the project from
GitHub onto your local machine for editing.

The benefit here is that you can edit and create diagrams, code, and
deliverables from your IDE or editor of choice, and in future classes you will
100% be required to have a local install and setup for Git, so might as well
'git' it going now!

---

[Return to Top](#asu-ser315-group-project-template)

---

### 4.2 Browser Editing

I don't recommend going this route, but you can also edit files and make
commits straight from the GitHub file viewer. The upside to this is you can
make small or simple changes from the browser as needed, but the downside is
you don't have the benefits of any tools and are limited to editing raw text
files.

While it is theoretically possible to complete most parts of this group
project strictly through GitHub's browser editors, I would not recommend it
as it is honestly more complicated and cumbersome than taking the time to get
things properly set up locally.

---

[Return to Top](#asu-ser315-group-project-template)

---

## 5. Basic Git

From here on, this guide will be assuming two things: that you're going to
work off of a local repository, and that you will be using a version of
the Bash shell (very common shell syntax). On Windows, Git Bash shell is installed when you install Git automatically.

This section will give you a bare-bones set of commands in Git to get you
going. The software has incredible depth, but for most people, you'll only
really interact with a handful of commands for any project unless you want
to become a power-user.

---

### 5.1 Project Setup

This section will relate to setting up your project for the first time.

We will assume you already have a GitHub account created. If not, do so now.

This section will be important to read and execute in order!

---

#### 5.1.1 Set up Git User and SSH Key

We'll start by creating an SSH key that we can use to access and work with
private Git repos on GitHub. This process requires some command line work,
but ultimately isn't too complicated and can be completed in a few steps.

We'll start by configuring your local install of Git to use your GitHub
email address.

Open your Bash shell and type in:

`git config --global user.name "[Your GitHub Username or Your Name]"`

Then type in:

`git config --global user.email "your.email@example.com"`

This will set your global Git settings to sign off with your username and
email that was supplied. This will be important for connecting to your
GitHub account when working on private repositories.

We'll be connecting to and working with GitHub from our local machine using
SSH, which is "Secure Shell Protocol". It allows us to connect to outside
systems from our command line securely, and by using a cryptographic key, we,
and GitHub's servers, can verify our identities.

To get this set up, we need to first generate an SSH Key locally.

Open your Bash shell and type in:

`ssh-keygen -t ed25519 -C "your_email@example.com"`

This creates a new SSH Key, using the provided email as a label. When you're
prompted to "Enter a file in which to save the key", press `Enter` to accept
the default location. If you have other keys made, this will overwrite them,
so consider giving this a more intentional name if you have other SSH keys you
work with.

At the next prompt, type in your password. It will ask you to enter it again
afterwards. The key is now created!

By default, keys are stored in `~/.ssh/`, where the `~` is your home User
folder. If you navigate to that, you'll see a `id_ed25519` and an
`id_ed25519.pub` file. They may have different names if you chose a different
key name. The `.pub` file is your public key, and the other is your private
key. Make sure to keep that safe, if it becomes lost, so does your access
with this keyset.

The next step is to add it to your GitHub account. Navigate to your account
settings, and from the left-side menu, click on "SSH and GPG Keys". Click on
the green "New SSH Key" button.

![GitHub SSH Key](/img_resources/InstructionImages/git_sshkey.png)

Enter a Title for this SSH Key. I called mine "ASU ID". In the Key textbox,
copy and paste the contents of your `.pub` file. You will want to make sure
to open that file with a text editor. On Windows, the `.pub` extension is for
Office Publisher, and will try to open it that way if you just double-click
on it.

Click the "Add SSH Key" button, and you're all set to work with private
repositories you have access to!

---

[Return to Top](#asu-ser315-group-project-template)

---

#### 5.1.2 `git fork`

> **CRITICAL NOTE:** Only one team member per team should fork this
> repository!!!

In Git, you can "fork" any repository. This effectively makes a copy of the
project that **you** own and can make changes to, that will not effect the
original. This is the behavior we want for making our own version of this
template.

There are two ways to do this, but we'll focus on the easier and more common
use for now: GitHub forking.

On the main repository page, there will be a series of buttons along the top
like this:

![GitHub Forking Button](/img_resources/InstructionImages/git_fork_button.png)

Go ahead and click the "Fork" button. This will take you to a page that looks
like this.

![GitHub Create Fork](/img_resources/InstructionImages/git_create_fork.png)

Change the name of the repository to
`SER315_[SEMESTER/YEAR][A/B/C]_[GROUPNAME]`. For example,
`SER315_FALL25C_SCHATTENWALD`.

Then click "Create fork".

That will create a copy of this repository into your personal GitHub, however,
we will need to add collaborators to let other people edit this repository
as well.

![Github Settings](/img_resources/InstructionImages/git_github_settings.png)

From the repository page, click on the Settings button, and from the left-side
menu, click on Collaborators. GitHub will have you sign in again, and you
will then see a button to "Add people". Go ahead and get/invite the GitHub
accounts of your teammates, and also invite `ser316asu` to give instructors
access. Now all parties can make changes to the group project.

Forked projects by their nature can not have different visibility settings
from their original. This means that we can't make the project private as it
stands. In order to change that, we need to go back to General Settings,
which is on the top of the left-hand menu. Scroll all the way down to the
"Danger Zone", and click "Leave Fork Network". This will disconnect this
repository from the original, but will also mean we can change its visibility.

![GitHub Danger Zone](/img_resources/InstructionImages/git_dangerzone.png)

Detaching the repo will take a second. Refresh after a few seconds, and
"Change Visibility" will be an option. Click that, and select "Change to
Private". It will ask you a series of questions. Click through them all,
and your copy of the repository will now be made private for your team and
instruction staff.

Congratulations, you've got your own copy of this
template!

---

[Return to Top](#asu-ser315-group-project-template)

---

#### 5.1.3 `git clone`

So we have a copy of the repository, how do we get that onto our machine for
editing? We use the `git clone` command!

Open up your Bash shell in the folder you want to be working from. I suggest
keeping this folder with all of your other SER315 files, and keeping it in a
Group Project folder of some kind, but you can place it wherever you want.

![GitHub Clone](/img_resources/InstructionImages/git_clone_github.png)

When you have your Bash open, go to the main repository page, and click the
green "Code" button. Make sure to select "SSH", and then go ahead and copy
the link provided. This can easily be done by clicking the 'copy' button next
to the link, or the two squares.

Onces that's copied, go to your Bash shell, and type in the following:

`git clone [URL THAT WAS COPIED]`

You will be prompted for your SSH passcode, and then you will download the
repository folder to the folder you're currently in. The terminals output
should look similar to below:

![Bash `git clone` example output](/img_resources/InstructionImages/git_clone_bash.png)

You now have a local working copy of your repository for you to edit and
make changes to as you see fit!

---

[Return to Top](#asu-ser315-group-project-template)

---

### 5.2 Collaboration

---

#### 5.2.1 `git pull`

---

[Return to Top](#asu-ser315-group-project-template)

---

#### 5.2.2 `git commit`

---

[Return to Top](#asu-ser315-group-project-template)

---

#### 5.2.3 `git push`

---

[Return to Top](#asu-ser315-group-project-template)

---

### 5.3 Further Git Resources

---

[Return to Top](#asu-ser315-group-project-template)

---
