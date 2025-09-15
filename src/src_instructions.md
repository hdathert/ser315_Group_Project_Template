# Source Code Instructions

This document will cover basic project setup, IDE and code editor tools to
make coding and testing easier, and how to fill out the
[README file](/src/README.md) in this directory that will be required for
submission with your code.

For the scope of this project, we won't need to make use of complicated build
tools or fancy tech to make this code work. We're only going to be
implementing a handful of features, and without a GUI, so we can keep things
really simple.

That being said, most projects you will have done to this point will have
started from an established code base, or, if nothing else, a starter file.
This might be the first time you've had to start a project from scratch, and
this section will help you understand how simple it can be!

### Contents

1. [Basic Project Setup](#1-basic-project-setup)
   1. [File Structure](#11-file-structure)
   2. [Build Commands](#12-build-commands)
   3. [Run Commands](#13-run-commands)
   4. [Arguments](#14-arguments)
2. [Project Tools](#2-project-tools)
   1. [VSCode](#21-vscode)
      1. [Build Tasks](#211-build-tasks)
      2. [Run Tasks](#212-run-tasks)
   2. [IDEA](#22-idea)
      1. [Build Configurations](#221-build-configurations)
      2. [Run Configurations](#222-run-configurations)
   3. [Build Systems](#23-build-tools)
3. [Filling out the README](#3-filling-out-the-readme)

---

## 1. Basic Project Setup

With a basic Java installation (which you should have at this point in the
course and degree), its really easy to set up a project from scratch, and this section will walk you through the basic steps.

This section will expect some level of familiarity in the Command Line
Interface, or console.

---

### 1.1 File Structure

The first thing you will need is a folder to work in. This one, `src`, was created for this purpose and you can keep all of your source files here.

Next, begin making the files you will need, which should be described in your
class diagrams. Don't forget to include a `Main` method in whatever class you
want to be the 'entry' class. `Main` can be in any class file you'd like, it
does not need to be in a `Main.java` file.

If you'd like to organize your classes into folders, that is fine too!
Whatever makes the most sense for you and how you want to structure this, but
given that you may only have 4-6 source files, this isn't required.

From here, go ahead and begin your implementation.

---

[Return to Top](#source-code-instructions)

---

### 1.2 Build Commands

To test your application through development, you'll have to build, or compile
it.

To begin, open your CLI (command line interface) into the folder where your
source files are. Depending on your system, there a variety of ways to do
this- for Linux, you can right-click inside the folder and an option to open
a terminal in the folder will be an option. If you have Git Bash on Windows,
you can also right-click and "Open Git Bash Here" will be an option. On Mac,
you should be able to `Ctrl-Click` on the folder and select "Open in Terminal"
through the menu.

Now that you are in your main source folder, you can start the compile or
build process.

Depending on your file structure, this can be very simple or slightly more
complicated. Either way, it will still be one command, broken down below.
For a simple compile of all `.java` files in the current directory, you can
use:

`javac *.java`

If you want to specify what files to compile, you can deliberately list them
like so:

`javac Main.java ClassOne.java ClassTwo.java`

If your files are organized into folders, you have to specify where `javac`
needs to look for files. There are a few methods for this.

For a recursive search through the current directory and all sub-directories
you can use:

`javac **/*.java`

If that doesn't work (it is system and console dependant), you can also
specify each directory to search like so:

`javac *.java src/*.java utils/*.java`

This will grab all the `.java` files in the current directory, and search the
listed sub-directories for all `.java` files contained in them.

Once your program is compiled, you are now good to run and test it!

---

[Return to Top](#source-code-instructions)

---

### 1.3 Run Commands

To run your program after compilation, you can simply type in the following:

`java [main]`

Where `[main]` is replaced with the name of the class that contains your
`main()` method.

This must be done in the same folder you did your compilation in, since Java
will look for the compiled class of that name.

---

[Return to Top](#source-code-instructions)

---

### 1.4 Arguments

You can supply arguments to your program to change behavior when you start it.
Those arguments will be in your `String[] args` array that are passed into the
`main()` method. How you choose to use those arguments is up to you, but to
pass them into your program, you supply each argument after your main class
when calling `java` in CLI:

`java [MainClass] argument1 argument2 argument3`

These arguments on their own won't do anything in your program unless you
choose to do things with them. In other words, if arguments are supplied to
your program but you don't use them, then they are discarded like they don't
exist.

This is optional, and can be useful if you want to demonstrate different
automated processes for showing off a feature, such as passing in a number
for how many users are generated, or a boolean for if the program will 'run
automatically', or a boolean for if debug messages will be displayed.

There are a lot of cool uses for arguments, and its up to you if you think
they will be useful for your project or not.

---

[Return to Top](#source-code-instructions)

---

## 2. Project Tools

There are a variety of tools out there to help with some of these processes,
so you don't have to type out commands in the terminal just to build and run
your program every time you need to test it. We'll cover VSCode and IDEA
workflows for building and running your code with a key press or button
click, and then also briefly mention build tools, which are outside the scope
of this project but will be used in future projects in this degree (SER316 in
particular).

---

### 2.1 VSCode

VSCode is a free code editor by Microsoft. Its a very light-weight and
extendable code editor that is incredibly popular in the development
community.

Built-in, it has its own terminal interface embedded, and has official
extensions for most high-use and popular languages that adds support for
autocomplete and 'intellisense'. It also has a set of tools for defining
build and run tasks so that you can automate the process of compiling your
code and running it without even having to touch a terminal.

To get VSCode set up for Java development, make sure you get the
[official Java coding pack](https://code.visualstudio.com/docs/languages/java)
and install it to get started!

VSCode uses configurable Tasks to execute operations, and stores them in a
`.vscode` directory in your root workspace. The tasks are JSON objects that
define properties of the task, and are stored in `.vscode/tasks.json`.

---

#### 2.1.1 Build Tasks

The Tasks JSON file is fully configurable and can be quite powerful, but for
our purposes, we don't need anything too crazy.

Create the `.vscode` directory in your workspace root if it hasn't already
been created for you, and create a `tasks.json` file.

![VSCode dot folder](/img_resources/InstructionImages/src_vscode_dot_folder.png)

If there is an existing task file, great! If not, you'll need to start the
file yourself by creating a blank task file:

```
{
	"version": "2.0.0",
	"tasks": []
}
```

Tasks will have a straight-forward JSON object structure. A basic example
build task looks like this, and will go into the `"tasks"` array:

Task:

```
{
	"type": "shell",
	"command": "javac",
	"args": [
		"*.java",
		"util/*.java"
	],
	"group": "build",
	"problemMatcher": [],
	"label": "build java project with wildcard"
}
```

This task has a variety of fields, and there are many more optional ones
available, but this should be enough to get the basic functionality across.

- `"type"`: Type of task. For our case, use `"shell"`, since these are command
  line tasks.
- `"command"`: The shell command we're executing. In this case, `javac`.
- `"args"`: The arguments supplied to the command, separated into an array.
- `"group"`: What task group does this belong to. There are two, `build` and
  `test`. For our cases in this project, we will only be using `build`
  group tasks.
- `"problemMatcher"`: This is a program that scans the output from builders
  and compilers for error messages, and repackages them for display in
  VSCode. There is no default one for `javac` so we've left it blank.
- `"label"`: The name applied to this task, is displayed in the Run Task
  menus.

In the `tasks.json` file:

```
{
	"version": "2.0.0",
	"tasks": [
		{
			"type": "shell",
			"command": "javac",
			"args": [
				"*.java",
				"util/*.java"
			],
			"group": "build",
			"problemMatcher": [],
			"label": "build java project with wildcard"
		},
		{
			"type": "shell",
			"command": "javac *.java util/*.java",
			"group": "build",
			"problemMatcher": [],
			"label": "build java project with explicit command"
		}
	]
}
```

This file shows two build tasks, one like the one described above, and one
that embeds all of the arguments into the `command` field. If VSCode is
struggling with the `*` wildcards for finding files, this is a valid
workaround.

To run your task, click on Terminal from the top menu, and then select Run Task.

![VSCode Terminal Menu](/img_resources/InstructionImages/src_vscode_terminalMenu.png)

VSCode will then display a list of tasks for you to choose from. Select the
task you want, and VSCode will open a terminal and execute it for you.

![VSCode Run Tasks](/img_resources/InstructionImages/src_vscode_selecttask.png)

You can set a default build task by going to the Terminal menu, and selecting
Configure Default Build Task. Like before, it will give you a menu of all
tasks to select from. Select the task you'd like to be default, and VSCode
will bind the hotkey combo `Ctrl+Shift+B` to run your default build task.

---

[Return to Top](#source-code-instructions)

---

#### 2.1.2 Run Tasks

Run tasks are semantically the same as build tasks in VSCode. The only
difference for our case is that we're calling on a different command line
application- `java` instead of `javac`.

Here is an example "run task":

```
{
	"type": "shell",
	"command": "java",
	"args": [
		"Main",
		"DEBUG",
		"24"
	],
	"group": "build",
	"problemMatcher": [],
	"label": "run java from Main class"
}
```

The only changes here are changing the `command` field from `javac` to `java`,
and the arguments are the name of the class that contains the `main()` method,
and any other arguments that might be needed. For this example, a `DEBUG` flag
and the number `24`.

You can execute this task in the same way as the build task: click on Terminal
from the top menu, click Run Task, and then select the task from the menu
that appears.

This allows you to run your built program very quickly and easily without
engaging directly with the command line.

---

[Return to Top](#source-code-instructions)

---

### 2.2 IDEA

IntelliJ's IDEA is a commercial IDE for Java development, with a free
student license available. I personally really like it for my Java
development, and I've found the license to be really easy to get and renew
over the last few years.

Like VSCode, it has a system for handling building and running of your
projects that is highly configurable and meant to be easy to set up and run
from a single button. In this section, I'll go over how to set that up for
a simple project.

To get IDEA set up for your project, start by navigating to the root
directory, right-clicking, and select "Open folder as IDEA Project". This will
open the whole folder as a project for IDEA to work in. This also allows you
do work on your diagrams and deliverable files from one program, which is
great!

But this doesn't set up the project as a Java project by default. To get IDEA
recognizing our project and telling it where our code is, we need to click on
the Main Menu button:

![IDEA Main Menu](/img_resources/InstructionImages/pdf-idea-menu.png)

From there, select Project Structure. This will open a new window with a ton
of options, but we're only interested in one. Select the `Modules` tab on the
left. This will show you your directory, and allow you to change where IDEA
looks for files. From the directory area, select the `src` folder, and click
`Sources` from the `Mark As:` list. Click apply, and this will make the `src`
folder the space that IDEA will look for source files.

![IDEA Project Structure Tab](/img_resources/InstructionImages/src_idea_proj_struct.png)

You're all set up for basic, bare-bones development in IDEA now!

---

#### 2.2.1 Build Configurations

IDEA handles building for you, and you don't need to manually configure
anything by default. If you've configured your Source directory correctly,
IDEA will automatically build everything from that folder into the `out`
directory whenever you run your program from the IDE, so we can move on to
the next section.

You can manually build the project if you'd like by hitting the hotkey
`Ctrl+F9`.

---

[Return to Top](#source-code-instructions)

---

#### 2.2.2 Run Configurations

To run your program, navigate to the class that has the `main()` method. You
should see a small green 'run' triangle next to the method. You can click this
to run your code!

![IDEA Simple Run](/img_resources/InstructionImages/src_idea_simple_run.png)

If you have arguments to supply, you can make changes to the Run configuration
by clicking on the area above the coding window with that green 'run'
triangle. You should see a dropdown with the name of the class that contains
your `main()` method. Click that, select "Edit Configurations", and you'll be
greeted with the following window:

![IDEA Run Configurations](/img_resources/InstructionImages/src_idea_run_config.png)

From here, you can make a dizzying amount of changes to how IDEA runs your
program, but for the scope of this project, the only things you may want to
do are change the arguments being passed into the program.

To do that, just type them into the "Program Arguments" text area as you would
if this were a console. You can rename and save configurations if you need to
test multiple different argument set ups as well- this kind of feature is
great for when you use arguments to define behavior, and want to quickly
switch between program contexts. You might not use this feature for this
project, but I assure you, it will make your life much easier in future
coursework!

---

[Return to Top](#source-code-instructions)

---

### 2.3 Build Tools

Build Tools are suites of tools and methods for building complicated projects
in many languages. In Java, the big three are Ant, Gradle, and Maven. These
are all extremely configurable, have methods for importing and plugging in
outside libraries, and have great support for testing/checking tools. They
are also great for building programs that target a variety of platforms,
and generally make development life much easier when you're working on larger
projects with lots of dependencies.

They are so far beyond the scope of this course and project that I'm only
mentioning them to let you know they exist and are really great for
bootstrapping a project, but are so complicated and large that for what we're
asking you to make, would be much more trouble than its worth. If you're
curious, here is some information about
[Maven](https://maven.apache.org/what-is-maven.html),
[Gradle](https://gradle.org/), and
[Ant](https://ant.apache.org/).

Gradle will be used extensively in SER316, and IDEA in particular has great
support for it out of the box. Take a look, read into it a bit, but don't
expect to understand it until you dive into it in 316.

---

[Return to Top](#source-code-instructions)

---

## 3. Filling out the README

The [README.md](/src/README.md) in this directory will serve as your
instructions for the course instructors and graders on how to use your
program. It is structured similarly to these instruction documents and also
your deliverable documents, so it should be pretty easy to fill out.

The key sections that will be critical for your instructors to be able to
evaluate your work is to explain to them the **WHAT**, **HOW**, and **WHY**
of your project:

> #### WHAT
>
> What does your project do? What is the goal or problem you're trying to
> solve?
>
> #### HOW
>
> How do we run this program? What specifically are the commands we need to
> type into our terminal to run it? What dependencies might we need? (_In
> this case, what version of Java SDK are you using?_)
>
> #### WHY
>
> What are the features you're trying to demonstrate? What should we as
> instructors be doing to see that functionality? Why is it important to
> solving the problems laid out in this project's requirements? What design
> choices led here?

Each section in the document has some basic explanation on what is expected
in there, and should be easy to follow. Make sure you're approaching the
writing of this document like we're someone who has no idea what this project
is. Make sure to provide some examples of how to run the program. Add some
images if you feel like that would be helpful. This is your chance to show what you've built and make it easy for others to see it in action!

---

[Return to Top](#source-code-instructions)

---
