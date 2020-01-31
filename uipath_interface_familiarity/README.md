# RPA Week 5 Day 1
## Overview

## Introduction – UiPath Interface Exploration

Below is the initial interface you will be presented with upon opening the
UiPath software:

![](media/ba90bcc145d5a8dd4e6883a18ff7561b.png)

This screen will allow the user to create a new Process, a new Library, or open
an existing template/project.

Clicking the Teams button will present the user with an interface that will
allow the user to integrate the (current) project with the version control
system of their choice. The options are: Git, TFS and SVN.

![](media/90388f5623c2f29b2baf39c25231ce81.png)

Click on the Tools button allows the user to install different extensions
(plug-ins), depending on their requirements. The one that will be utilised for
the course will be Chrome Extension.

![](media/5c2d8a9cce4fc47eaa6c571a56de8f7d.png)

The help page will direct the user to many online resources that will help with
understanding the software and it’s features.

![](media/746aeff67aed02966baffbc9c4266a95.png)

To start a new project, from the Start button (within UiPath), selecting ‘New
Process’ will present the user with a popup dialogue box. The details in this
form will be used to name and describe the project.

![](media/914f13401b5cffe6122f0560b71328ea.png)

![](media/4bac8742d7be65e6199b1888837bda71.png)

Once this has been completed, the user will be presented with the workspace that
all UiPath processes will be created within. To access the splash screen
features, the Home button in the top left hand corner will redirect the user
back there.

![](media/4d4cd96242957b7a4ce7224dcb02b7ad.png)

Within this workspace, clicking on ‘Open Main Workflow’ will change the central
pane to a blank project, with the words ‘Drop Activity Here (+)\` displayed.

![](media/62455ca1b3bdd284e0b3021d2b6d366d.png)

This zone is a drag-and-drop area, and activities from the left hand panel are
‘dropped’ in to the main development window.

![](media/78b253ca77f39155a71fbbbdc1626ceb.png)

![](media/62a52308e7639b5cc125a857581df413.png)

On the left hand pane is the Project overview. This will show the user all files
in the current project.

![](media/b2984c22fe56a9407fe811ba98ca29c1.png)

Also in the left hand pane is the Snippets view. This pane is used to insert
code snippets that the user will utilise frequently. For example, a snippet the
user may have built to be utilised in many projects could be to ‘Open a notepad,
paste some data, save to a location’. The snippet, if built correctly, should be
able to drop in to the main workflow, negating the necessity to ‘reinvent the
wheel’.

![](media/ea2128469b3bf57ee4b0d66c1fe4ad17.png)

The variables to be utilised by UiPath activities are accessed through the
‘Variables’ button, and will display a new pane, showing what variables
currently exist.

![](media/c6b877e2733e80e8a7a3be99275e9315.png)

Once a variable is created by giving the variable a name, the remainder of the
details may be filled in, either in the Variables pane, or in the Properties
pane.

![](media/c028b144b23458d163f8357745fae77f.png)

Arguments can be accessed from a button from the bottom pane also. Arguments
provide a way of passing information between workflows, similar to global
variables.

![](media/b5e1ef9aba917427b242eed04d279747.png)

Finally, there is an Imports button that will open a pane, displaying all of the
current imports for this project, as well as providing a search bar to find
further dependencies the project might required.

![](media/4b7a8bc3b6371b1bc81062464539c338.png)

An Integrated Development Environment (IDE) wouldn’t be complete without an
Output pane. In the bottom left hand corner is a button to unveil this pane.

![](media/99126af89a06c66d48075a92e5177e92.png)

Next to the Output button is the Error List button, which will display the
current errors preventing the project from compiling.

![](media/0fe6c6e787ab8737efd41ff5a211c7fd.png)

Next is the Breakpoints button, which will display any locations within the
workflow, which has been set to halt the normal execution of flow.

![](media/67eeb5fd7147c251901f62c86fd06e2f.png)

On the far right hand side, the Outline button will display what activities
belong to which.

![](media/680812c563510663577c55c46f1222b0.png)

Also on the far right hand side is a button to display the Properties of many
things, fundamentally the properties of an Activity (component).

![](media/8518d1d3a814401469d2b99d94868580.png)

Navigating the flow can be cumbersome if the process is long, complex or both.
In the bottom right hand corner of the work space are some buttons that can help
navigating the code.

![](media/e1599b3bfeb6b52422356c654aec37a2.png)

The first button allows the user to click-and-drag around the interface, and can
also be accessed by holding down the space bar.

![](media/b1815261ca8dba0e709929d46e2d0370.png)

The next icon will return the resolution of the code to 100%.

![](media/1448c580ab1ba6abf4e1146d5c29f21d.png)

Next to this is a drop down, and type-able zoom percentage.

![](media/3b90d4425327e317bfaeafbb7a81d49a.png)

The following icon allows the user to change the resolution (zoom) of the code
to ‘fit to screen’.

![](media/b5e6f1cac42dbf7bf558e6b8792a0734.png)

Finally, the icon on the far right hand side will create a preview pane that can
be navigated around.

![](media/1dd1eb9d6de0d1a939ebdc62033e1639.png)

The Design ribbon has many features displayed on it. The first and most
indicative is the New and Save icons, which provide the user a quick was to
create New Sequences, Flowcharts, State Machines and Global Handlers, and allow
the user to Save, Save As and Save All.

![](media/6134fd71f71d019fed1fcab9c0fff5a8.png)

The Save as Template button will allow the current sequence to be saved as a
template, that can be accessed from the Home screen, when creating a new
process.

![](media/02dc783631f66d73e48a1aad292e7953.png)

Next is the run button, with drop down options of Run File, Debug, and Run.

![](media/011257b2b0efba31c223cddddb2842e9.png)

A little further along is the Manage Packages, which will allow the user to
search for and install any dependencies required for the process.

![](media/3c5e570546400b9c60b2a376aa8b2a72.png)

The next icon is the Recording icon. This icon can also presents a drop down,
showing the different recording modes available: Basic, Web, Desktop, Image,
Native Citrix and Computer Vision.

![](media/91a80853e9c096c76221f041cbaabf3d.png)

Screen scraping allows the user to capture data from an interface, by utilising
Optical Character Recognition (OCR) technology, and may be required for
difficult to handle interfaces, such as Remote Desktop Protocol (RDP) sessions.

![](media/6b90202f6c1b5ce1ccba9179e74aec7c.png)

Data Scraping will allow the user to capture ‘tables’ of information from
various interfaces. When the data is presented over many ‘pages’, the data
scraping wizard is capable of navigating through the ‘next page’ button, and
continue to capture common-selector data.

![](media/d20959a4c0a4bfae9a3972c9e7348715.png)

User Events allows the developer to capture mouse and keyboard interactions with
various elements on the machine. Drop down options include On Click Element, On
Keypress Element, On Click Image, Monitor Mouse, and Monitor Keyboard.

![](media/308e69924a4f15968eed405e33a72942.png)

Likely to be one of the more utilised ribbon icons is the UI Explorer icon,
which will open a new dialogue box. Within this dialogue box, the user is able
to find the selector for any program that is currently open.

![](media/b349bb9948df86b8a321edbac7c00112.png)

![](media/01a628d0a339c8e1dde865105f3f71a6.png)

The Removed Unused Variables is fairly self explanatory, and can be used as and
when needed, but should be executed at the very least, at the end of process
development as a clean-up step.

![](media/bbd88f1964972e26495bb4dcdcdef36b.png)

The Analyze File icon also has a drop down, with the options of Analyze Project,
Validate File, Validate Project and Workflow Analyzer Settings. Selecting
Analyze Project will populate the Error List pane with data, if any errors
exist.

![](media/956433b2505cf8f73cd9088545705ff9.png)

![](media/27ecdd180e2f0d87f87ff5990e51b207.png)

Export To Excel will create a tabular looking display of the current process.
This exported file can be imported to UiPath, and is a good method of backing up
script structure.

![](media/f575f7458b1ddc4865030344e5be8541.png)

Finally, the Publish icon on the Design ribbon allows the process (robot) to be
published to the UiPath Orchestrator, if UiPath has been connected to
Orchestrator. Otherwise, it will publish to the local robot service.

![](media/d9f755a8b71c0842bc1870a9d5624469.png)

Further along the ribbon tabs, are some further features. The far left icon
presents the user with the Command Palette Search, which allows the user to do
one of the following: Add Activity, Universal Search, Go To File, and Jump To
Activity.

![](media/634e1bd685d54707f2c762c7cbdf7595.png)

The next icon along is the Send Feedback button. This allows the user to submit
feedback to the developers of UiPath.

![](media/aaa6c182c136b7179e394aef6e5e5663.png)

The next button presents the same options as the Help section of the Home
screen.

![](media/27cc4e25b6efa59881a4329372a06d10.png)

The last icon of note is the Hide Ribbon button. This may be utilised to
increase the amount of work space required.

![](media/583bae8a1e8c8496cf128bbc78bb778c.png)

Within the Debug ribbon are more options. Within Debug mode, the user is
presented with a highlighted display of the current activity, as well as a
variable watcher on the left hand side.

![](media/c46be0f7085b3ecf08893957c1cfde99.png)

The first option to note is the Step Into, Step Over and Step Out, which allows
the user to navigate their code in various manners.

![](media/04828cf9a4e755e9188c19793989c275.png)

The next set of icons allows the user to navigate their process further, such as
Restarting the process, or Retrying an activity that failed, or even Ignoring
the issue, and proceeding anyway.

![](media/1956a9b950dbaae0d8cd8485a1065c56.png)

Breakpoints are a common concept in programming, and their purpose remains
consistent within UiPath. The drop down will provide options for Toggle
Breakpoints, and Show Breakpoints.

![](media/97a6223e174c60711707c2e79722a628.png)

Slow Step cycles between5 speeds, Off, 1x, 2x, 3x and 4x speed, and changes the
rate of execution whilst debugging.

![](media/834cb6e8ab8bc986c1868c1e13fee824.png)

The Highlight Elements icon allows the robot to highlight which element is
currently being targeted, which may aid debugging.

![](media/beba0fcc4124197a8fbb5814fee57578.png)

With the Log Activities option enabled, any activities that execute will be
stored in a log text file.

![](media/9419809f099c842d74cab03db6d546a8.png)

Finally, the last icon will open Windows File Explorer, opened at the location
of the log files. This can be further accessed by pressing Control Key + ‘L’.

![](media/572f28d81349de15536911b87fa3e679.png)
## Tutorial
## Exercises
