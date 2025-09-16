# Deliverable Instructions

This document breaks down the requirements for each project deliverable and
provides instructions for completing and submitting your work. Each
deliverable builds on the previous one, with your team iteratively developing
and refining your software design throughout the semester.

The deliverables include both technical components (diagrams, documentation,
implementation) and reflection sections that help track your progress and
collaboration. Starting with Deliverable 2, you'll also incorporate feedback
from previous submissions.

Each deliverable requires a 2-3 minute screencast explaining your work and
design decisions. The following sections cover the specific requirements for
each deliverable component, along with instructions for the tools and
submission process you'll need.

### Contents

1. [Deliverable Breakdown](#1-deliverable-breakdown)
   1. [Team Reflection](#11-team-reflection)
   2. [Individual Reflection](#12-individual-reflection)
   3. [Meeting Overview](#13-meeting-overview)
   4. [Design](#14-design)
   5. [Review](#15-review)
2. [Basic Markdown](#2-basic-markdown)
3. [Diagrams Overview](#3-diagrams-overview)
4. [Video Overview](#4-video-overview)
   1. [Recording](#41-recording)
      1. [OBS](#411-obs)
      2. [Zoom](#412-zoom)
   2. [Uploading to YouTube](#42-uploading-to-youtube)
5. [GUI Tools Overview](#5-gui-tools-overview)
   1. [Hand Drawn](#51-hand-drawn)
   2. [Figma](#52-figma)
   3. [Pencil](#53-pencil)
   4. [Canva](#54-canva)
6. [How to Export to PDF](#6-how-to-export-to-pdf)
   1. [VSCode](#61-vscode)
   2. [IDEA](#62-idea)
   3. [Other](#63-other)

---

## 1. Deliverable Breakdown

In this section we'll break down each major section of the deliverable
with instructions on how to fill them out. Try to maintain the formatting
choice in the Deliverable template, as it makes these sections easier to
read.

### 1.1 Team Reflection

Fill out each "Answer" section with the teams answer to the question. This
ideally should be done collaboratively! At the end, include a screencast
link (screen-cast information is located [here](#4-video-overview)).

This is a great opportunity to learn and grow from the wins and struggles
from each deliverable cycle! Take good advantage of it, and be honest with
yourselves and each other. We're all in this together!

### 1.2 Individual Reflection

Write a short paragraph that gives an overview of what you accomplished or
worked on for this deliverable, and reflect on your contribution. This
doesn't have to be long, but take the time to introspect on how things are
going, even if you don't write that down. Reflecting on the process, both
personal and as a group, is how we identify things to work on and improve!

### 1.3 Meeting Overview

This section keeps track of meetings, attendance, and what was discussed.
This doesn't need to be extremely detailed, but a broad overview of the
discussion is good for tracking group progress and cohesion.

### 1.4 Design

Each Deliverable template will have sections for each required portion of
your design describing the expectations for each. After the first
deliverable, this section will be split into two sub-sections: Updated
Design and New Design. The Updated Design will include the design elements
from the last deliverable, but updated, while the New Design will be the
new portions for this deliverable.

These will be continually updated throughout the project as you receive
feedback and the design/needs change.

### 1.5 Review

This section (Deliverables 2-4) expects an overview of the peer and
instructor reviews, while also giving space to reflect on those reviews,
and how their feedback was/is being incorporated into your design.

---

[Return to Top](#deliverable-instructions)

---

## 2. Basic Markdown

MarkDown is a very popular language for creating and rendering documents, and
resources for learning it are plentiful throughout the internet.
Below is a great resource for the basic syntax and rules for how to structure
documents:

[Markdown Guide: Basic Syntax](https://www.markdownguide.org/basic-syntax/)

Basic features that are being used in this and other documents are as follows:

Headers are made with `#`, with additional `#`s per heading level.

# This is a heading

## This is a 2nd level heading

### This is a 3rd level heading!

#### This is a 4th level heading!

```
# This is a heading
## This is a 2nd level heading
### This is a 3rd level heading!
#### This is a 4th level heading!
```

**Bold** words can be created with `**`, like `**this**`.

_Italics_ can be created with `_`, like `_this_`.

> Quote or block sections are created by starting a line with a `>`.

[Links](#2-basic-markdown) are created with the following syntax:
`[Link Text](link)`. The Link Text is the visual of the link, and the link
can be a local file, a heading, or an `http` link. An example of using a
heading for an internal link would be:

`[2. Basic Markdown](#2-basic-markdown)`

Images can be embedded with a similar syntax, but with an `!` added to the
beginning. Like the Link syntax, between the brackets is the alt-name of the
image, shown if the image can't be rendered or found. The link section can
be a hyperlink (`http`), or a path to a local image.

For example, `![Img](/img_resources/default_image.jpg)` renders this:

![Img](/img_resources/default_image.jpg)

Lists can be made by writing either `- Item` for an unordered list or
`1. Item` for an ordered list. Some editors will automatically increment the
number for an ordered list, but it's good practice to update the numbers
yourself, even if the final render will increment for you. In other words,
this is valid syntax:

```
1. Item
1. Something
1. List!
```

That will render as:

1. Item
1. Something
1. List!

Horizontal lines can be created by having `---` on its own line.

Paragraphs are created by having line breaks between sections in the source.

That is the overview of the absolute basics of MarkDown, which is all you need
to know to create and edit the included documents!

---

[Return to Top](#deliverable-instructions)

---

## 3. Diagrams Overview

The diagrams needed for this deliverable can be made in a variety of ways.
Astah should be familiar to you, but another method is through Mermaid.
Mermaid is a text-based diagramming tool that, like MarkDown, can be rendered
out to images from code. It is easy to collaborate on, version control, and
maintain.

A further overview of how to create, edit, and integrate Mermaid diagrams can
be found in the `diagrams` folder of this repo. Inside, there is an
[Instructions document](/diagrams/_diagrams_instructions.md), and examples of
the main diagrams you'll need for this project in the `diagrams/examples`
folder.

---

[Return to Top](#deliverable-instructions)

---

## 4. Video Overview

Your group is expected for each deliverable to include a 2-3 minute screen
cast that covers the design artifacts for that deliverable. Screen casts will
be a continuing requirement through the rest of this degree for demonstrating
software and design, so establishing a good workflow early is best practice.

> **Big Tip:** Write a script! It is much easier to do this process while
> having an idea of what to say ahead of time. Trying to shoot from the hip
> will actually take longer than you think for all the times you have to
> pause to collect your thoughts!

### 4.1 Recording

There are a variety of methods for screen recording for each platform, but
the most common methods are through basic webcam capture software that can
come with some systems, OBS, and Zoom. In this document, I'll quickly cover
OBS and Zoom, since they are straight forward and free options.

OBS has the higher quality of the two, so I'd recommend that!

After this section, I'll go over how to upload to YouTube and embed the link.

#### 4.1.1 OBS

OBS, or [Open Broadcasting Software](https://obsproject.com/), is a free
software for screen capture and broadcasting, and is very popular with
streamers for its configurability and power, while being open and free
software. You can download it at the link above.

There are a lot of options in OBS, but you can safely ignore most of them for
this simple use case. Getting up and running just requires a microphone of
some kind and the software. Here is a really great
[video tutorial](https://www.youtube.com/watch?v=xoe9ZOzlfnQ)
for how to get screen recording set up!

#### 4.1.2 Zoom

The Zoom desktop application can do basic screen capture from a meeting space.
You can get the desktop version [here](https://zoom.us/download). Download and
install it, and you can then sign into your ASU account with them. Once logged
in, you can start a meeting. Share your screen, set up your microphone, and
you can then record the meeting. Once your done, end the meeting and the
recording will be exported to your computer.

The quality of this video seems to be dependant on your connection and can be
jittery on the video quality. Also, having to run this through a meeting is
an extra step that can be quite frankly, annoying. I'm giving this as an
option for people who don't want to run a whole new program do make the
videos, but I can't recommend it.

For a more comprehensive tutorial, reference
[this](https://www.youtube.com/watch?v=H9qhoAIzW3E) video.

### 4.2 Uploading to YouTube

To upload your screen cast to YouTube for embedding, first make sure you have
a YouTube account. Once you do, sign into it and click on the `Create` button,
which should be in the upper-right corner of the screen by your profile photo.

From the drop-down, click `Upload Video`. This will navigate you to the
YouTube Studio section where you can manage your uploads, and display a screen for uploading videos. You can drag and drop your video
onto this screen or click `Select files` to use the file explorer.

Once you select the file, YouTube will begin uploading it to the platform, but
don't worry! It won't publish the video until you input all of the needed
information. Start by filling out the Title and Description. I suggest naming
it after your Team Name and Deliverable number. Include a description if you'd
like, but it isn't necessary. Under the `Audience` section, say that this is
**not** made for kids. This is a required choice, per YouTube guidelines.

Click `Next` on the next two screens until you get to the `Visibility` tab.
Make sure to select `Unlisted`, as this will keep the video from appearing in
any search results or recommended feeds, while still being accessible by link
sharing. If you make it private, **_NO ONE ELSE WILL BE ABLE TO SEE IT_**.
Once `Unlisted` is selected, hit `Save`.

YouTube will give you a video link. Copy and paste that link into your
deliverable document where it says `LINK-ADDRESS-GOES.HERE`.

And that's it! You have now attached a link to a screen cast!

---

[Return to Top](#deliverable-instructions)

---

## 5. GUI Tools Overview

In Deliverables 2-4, you'll be tasked with mocking up a UI for the project.
This won't have to be implemented, so feel free to be as ambitious as you want
within reason!

I've compiled below a list of some good tools for doing this
mockup/wireframing. Some are more complicated than others, and all have their
pros and cons, but will all be absolutely sufficient for what we need in this
project.

Due to the variety of workflows for each tool, I'll refrain from going
in-depth on how any of them work. They are all extensively documented and have
lots of community support and learning available on the web.

### 5.1 Hand Drawn

For the first round of UI design, you are allowed to do a hand-drawn sketch
of the UI. The nice thing about this option is you can get quick and dirty
with it or as clean as you like. My suggestion would be to do this on graphing
paper, as the grid makes it a little easier to keep things aligned in a way
that is pleasing (but that might just be my preference).

When its done, scan or photograph it and you can include it in your
deliverable. Double check that the photo is clean and easy to read, no
blurring or shake from the camera. Scanning is almost certainly the best way
to do it, and should be free (or cheap) at your local print shop or library!

### 5.2 Figma

[Figma](https://www.figma.com) is a browser-based tool for UI mock-up and
design. It requires an account to use, but is very powerful with a whole
[marketplace](https://www.figma.com/community/ui-kits?editor_type=figma)
of free UI kits to get started from. It allows for collaborative work similar
to Google Docs, and even has a Play function that allows you to 'test' the UI
in context.

It is complicated and powerful software, but can be a good way to get a quick
UI mock up put together, and is well supported with a huge array of tutorials
available online.

### 5.3 Pencil

[Pencil](https://pencil.evolus.vn/) is a free open-source wireframing tool for
GUI prototyping. It isn't as flashy as Figma, but it is easy to use and can
get the basic ideas across for what a GUI could look like. It also has the
ability to export your mockups to images for adding to deliverables.

### 5.4 Canva

[Canva](https://www.canva.com/) is another browser-based design tool, similar
to Figma. It contains many of the same features as Figma (collaboration,
built-in templates), but is generally more geared towards graphic design for  
web and print. It does have a suite of UI features, and most features are
free to use. Like Figma, it is a complex and powerful piece of software, but
also has great community learning support.

The tool for doing UI work is called
[Whiteboard](https://www.canva.com/online-whiteboard/ui-design-tool/).

---

[Return to Top](#deliverable-instructions)

---

## 6. How to Export to PDF

There are a variety of ways to export Markdown files to PDF for submission,
here are a few methods for common code editors. Each export tool will style
the Markdown differently, and some exporters are more easily configured than
others.

### 6.1 VSCode

In VSCode, there is an extension called
[MarkDown PDF](https://marketplace.visualstudio.com/items?itemName=yzane.markdown-pdf)
that allows you to export Markdown files to PDF, JPG, PNG, and HTML. Simply
install it to your VSCode, restart to enable the extension, and you're ready
to go.

For basic usage, make sure you have a Markdown file open and active in your
editor, and open the Command Palette (`Ctrl+Shift+P` by default). Type in
`export`, and options called `Markdown PDF` will appear. Select the
one that says `Markdown PDF: Export (pdf)`, and the extension will export the
currently open and active Markdown file to a PDF file in the directory that it
currently is in. That's all there is to it!

Alternatively, you can `Right-Click` in your Markdown editing window, and
the option to export will be in the menu towards the bottom if you have the
extension installed.

> **NOTE:** For images to render properly, they need to live below the local
> path of the Markdown file. For example, images referenced in the root
> folder "above" this one (the default image, for example) can't be found by
> this extension. A way around this is to create a folder in **this**
> directory where the images you need are stored.

### 6.2 IDEA

IntelliJ IDEA IDE comes with full Markdown support out of the box, including
an exporter.

![IDEA Main Menu](/img_resources/InstructionImages/pdf-idea-menu.png)

To export a Markdown file as a PDF, navigate to the Tools menu (from Main
Menu, pictured above). From there, go to the Markdown menu item, and select
`Export Markdown File To...`.

![IDEA Export MD](/img_resources/InstructionImages/pdf-idea-export.png)

Name the file, make sure the format is PDF, double check where you're saving
it to (the default is the same folder the `.md` file is in), and click
`Export`.

> **NOTE**: IDEA's exporter is theme dependant, meaning the look of the
> exported PDF will change based on your theme. It is suggested for the best
> look to change your IDEs theme to a 'light mode' theme of some kind before
> exporting!

![IDEA Save MD](/img_resources/InstructionImages/pdf-idea-save.png)

That will save the PDF for you! Unlike the VSCode extension, this
implementation can make use of your full project directory to link images, so
they can be saved in a dedicated place for better organization.

Since it is built in and supports more organized file structures, this is
the recommended option.

### 6.3 Other

Unfortunately, I have not found a reliable browser-based option for converting
Markdown files to PDF with embedded images. There are some other ways to
render and export MarkDown, however. Do to the more advanced nature of these
options, I will leave the resources below but not go into great depth on how
they work.

One is using a program called [grip](https://github.com/joeyespo/grip), which
is a commandline server written in Python that serves Markdown files to be
rendered to a browser, and then can be saved as a PDF through a `Print to PDF`
function of printing a website. More information can be found through the link
above.

Another option is very advanced and not recommended, but to set up a GitHub
Action that renders Markdown files as PDFs when they are pushed to the remote
repository. If you are familiar at all with GitHub Actions, here is a
[link](https://github.com/BaileyJM02/markdown-to-pdf) to a pre-made and
functional Action you can attach to your forked repository.

---

[Return to Top](#deliverable-instructions)

---
