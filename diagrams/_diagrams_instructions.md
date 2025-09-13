# Mermaid Diagram Instructions

Description goes here

### Contents

1. [How to Set Up Mermaid Editors](#1-how-to-set-up-mermaid-editors)
   1. [VSCode](#11-vscode)
   2. [IDEA](#12-idea)
   3. [Browser](#13-browser)
2. [How to Export Diagrams as Images](#2-how-to-export-diagrams-as-images)
   1. [VSCode](#21-vscode)
   2. [IDEA](#22-idea)
   3. [Browser](#23-browser)
3. [How to Embed Diagrams to MarkDown files](#3-how-to-embed-diagrams-to-markdown-files)
   1. [As Images (Recommended)](#31-as-images-recommended)
   2. [As Code](#32-as-code)

---

## 1. How to Set Up Mermaid Editors

In this section I'll go over three common and easy methods for getting
Mermaid set up for editing. The first two, VSCode and IntelliJ IDEA, are
the easiest to set up in my opinion. Other IDEs and editors no doubt have
support, and should be also very straight-forward to set up. I've also
included a Browser option through the Mermaid website if that is what
you'd prefer, but being able to work on the whole project from one central
program seems to be a worthwhile endeavor to set up.

### 1.1. VSCode

![Full Workspace](/img_resources/InstructionImages/mermaid_vsCode_preview2.png)

VSCode is a free code editor by Microsoft which is increasingly popular
due to its free nature and broad extendability through its Extensions
marketplace. One of these extensions is the official Mermaid Charts
extension, linked below:

> [Mermaid Charts Extension (VSCode Marketplace)](https://marketplace.visualstudio.com/items?itemName=MermaidChart.vscode-mermaid-chart&ssr=false#overview)

Boot up your copy of VS Code and install this extension. It will give you
the ability to code in `.mmd` files with syntax highlighting and some
basic intellisense features (but those are extremely limited without
logging in). Logging in is not necessary to get the features we need.

![Command Palette](/img_resources/InstructionImages/mermaid_vsCode_preview.png)

To get started once installed, simply create a new file with the `.mmd`
file extension, or open one of the examples in the `/examples/` folder.
Here, you can see and edit the source for a chart. to see a preview of
the chart rendered, open the Command Palette (`Ctrl+Shift+P` by default),
and type in at the top of the screen "Mermaid Preview" and the option to
open a Mermaid preview window should appear.

---

[Return to Top](#mermaid-diagram-instructions)

---

### 1.2. IDEA

![Full Workspace](/img_resources/InstructionImages/mermaid_idea_overview.png)

IntelliJ IDEA is a full-fledged IDE created by JetBrains. It is geared
specifically towards Java development, and is widely lauded as a smart and
efficient workspace for development. It isn't free, but for students a
free educational license can be acquired easily that will grant access
to all of their products, which only needs to be updated every year. I
would strongly suggest picking it up- its easily cross-platform and works
great. It, like VSCode, supports extensions via Plugins. A Mermaid plugin
developed by the IntelliJ team is linked below:

[Plugin Link (JETBRAINS Marketplace)](https://plugins.jetbrains.com/plugin/20146-mermaid)

Boot up IDEA and install this plugin. It will give you syntax
highlighting, autocomplete, and a nice preview window that usually will
open automatically, but if it doesn't, you can click on the button marked
below (in the top-right corner of the workspace, middle button):

![Preview Button](/img_resources/InstructionImages/mermaid_idea_previewbutton.png)

The preview will automatically update as you type, just like the VSCode
preview window.

---

[Return to Top](#mermaid-diagram-instructions)

---

### 1.3. Browser

![Mermaid Live Editor Overview](/img_resources/InstructionImages/mermaid_live_overview.png)

An alternative option is to just use the Mermaid.Live editor. This browser
solution gives you a small code editor and chart preview window, and
includes features for saving and editing charts as you go.

[Mermaid.Live Browser Editor](https://mermaid.live)

> NOTE: Because this is browser based, there is no simple method for
> tracking via Git. You'll have to copy from Git into the live editor,
> and paste back to save changes to the Repo.

On the left hand side of the screen you have a code editor, which features
syntax highlighting and some autocomplete, but I have noticed in my
testing that the feature is finicky and can be error prone. Styling of
the chart can be managed in the `Config` tab over the code window.
Styling is outside of the scope of this overview, but there are plenty
of resources on how to change the look and feel of a chart.

Chart rendering is done on the right-hand side. You can zoom in and out,
moving the view around with mouse functions.

---

[Return to Top](#mermaid-diagram-instructions)

---

## 2. How to Export Diagrams as Images

The best way to get these diagrams into your deliverables is to save them
as images and embed them into your MarkDown document. Below describes the
methods for doing that on different platforms.

### 2.1. VSCode

On the Diagram Preview Window, there is a download button in the top-right
corner of the window. Click this, and a dropdown menu will show you
options for exporting the chart to a `.png` or a `.svg` file. For our
purposes, we'll select `.png`. A standard file explorer will ask you
where to save the image. Make sure you save it in a folder tracked by Git
and with a descriptive name.

![VSCode Mermaid Export](/img_resources/InstructionImages/mermaid_vsCode_export.png)

Once this is done, an image will be saved of the chart which can be
embedded into MarkDown or any other document editor you may want to use.
For example:

![Use Case Diagram Example](/img_resources/InstructionImages/mermaid_vscode_exportExample.png)

> Note: The export image size and dimensions are based off of the preview
> window size. If you have too much whitespace, change the size of the
> preview window, and export again. Alternatively, you can crop the image
> in any other image editor (photoshop, GIMP, Krita, etc)

---

[Return to Top](#mermaid-diagram-instructions)

---

### 2.2. IDEA

Unfortunately, the IDEA Mermaid plugin does not contain any built-in
functionality for directly saving diagrams as images. However, you can use
any screen capture tool to do this anyway.

On Windows, the default keybind for taking a screen capture is
`Windows+Shift+S` which brings up the screen snip tool. This saves to
your clipboard and can be pasted into your file explorer in IDEA directly.
Alternatively, you can open the Screen Snip application which functions
similarly, and that allows you to do some basic editing and save out
directly to a file.

On Mac, you can screen snip with the key command `Shift+Cmd+4` or
`Shift+Cmd+5`. Screenshots should be saved to the desktop by default,
which can be moved later to your Git project directory.

Linux users have access to screen snipping tools, but depend on the distro
and window environment, which should be easy to find documentation on,
but do to the variety of tools and methods, is outside of the scope of
this document.

---

[Return to Top](#mermaid-diagram-instructions)

---

### 2.3. Browser

The Mermaid Live Editor has support for directly saving charts out to
images.

![Mermaid Live Actions Tab](/img_resources/InstructionImages/mermaid_live_Actions.png)

Under the code window, there is an Actions tab. You might have to click on the tab to make it appear. From here, you can export to all sorts of
formats, and even can embed the diagram directly into MarkDown using the
`Copy MarkDown` button.

To save an image, you can click on the `PNG` or `SVG` buttons, as well as
copy the image. I've found for best results that hitting the button to
open the diagram in the browser gives the most accurate image render to
download. This is the button right next to the `PNG` button:

![Mermaid Live Export](/img_resources/InstructionImages/mermaid_live_export.png)

From there, you can save the image to disc like any other image from a
browser directly into your Git repository.

---

[Return to Top](#mermaid-diagram-instructions)

---

## 3. How to Embed Diagrams to MarkDown Files

There are two main ways to embed Mermaid diagrams into a MarkDown
document.

### 3.1. As Images (Recommended)

To add a diagram to a MarkDown file as an image, you will first need to
have the image saved in a visible space relative to the document you're
working with. In other words, the image must be in the main workspace
folder.

The syntax for adding an image to a MarkDown file is:

`![Image Alt Text](Image Link)`

There are two main components to this:

- The image alt text is just a way to identify the image- best used to
  describe what the image is.
- The Image Link is the directory path from the root directory to the
  image. For example, for the default image used in this repository,
  the relative path is: `/img_resources/default_image.jpg`.

This is the recommended way to do this, since the output when viewed is predictable across all MarkDown renderers.

---

[Return to Top](#mermaid-diagram-instructions)

---

### 3.2. As Code

Alternatively, you can embed Mermaid source directly into MarkDown. This
is not supported on all platforms or devices, so this is not recommended
for this project.

To embed Mermaid into MarkDown, you use the following syntax:

![Mermaid Embedded Code](/img_resources/InstructionImages/mermaid_embed_code.png)

With the ` ``` ` surrounding normal Mermaid syntax, with mermaid after the
opening triple-backtick, which in some editors will render as:

```mermaid
flowchart LR
Area-->Place
Place-->Area
```

Like mentioned before, this is not supported behavior on every MarkDown
renderer, and probably should not be used, but it is an option.

---

[Return to Top](#mermaid-diagram-instructions)

---
