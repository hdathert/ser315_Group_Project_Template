What I still need to cover here:

- How to set up Mermaid editors
  - IDEA
  - Browser
- How to export diagrams as images
  - IDEA
  - Browser

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

[Plugin Link (JETBRAINS Marketplace)](https://plugins.jetbrains.com/plugin/20146-mermaid)

---

[Return to Top](#mermaid-diagram-instructions)

---

### 1.3. Browser

---

[Return to Top](#mermaid-diagram-instructions)

---

## 2. How to Export Diagrams as Images

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

---

[Return to Top](#mermaid-diagram-instructions)

---

### 2.3. Browser

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
