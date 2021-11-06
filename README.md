# PCB_UI README

## Description

This repository contains Altium design files for UBC Thunderbots' user interface PCB. Anyone who wishes to push changes to this project must get permission from the current Electrical Team Lead(s).

## Getting Started

### Required software

1. git
2. Altium Designer

### Instructions

1. Either create a new working branch or select an existing branch other than `main`.
2. **Clone** your working branch of the repository to your PC (i.e. `C:/Documents/thunderbots/PCB_UI`).
3. In Altium Designer, navigate to *Preferences -> Data Management -> Version Control* and ensure **SVN - Subversion** is enabled and **Version 1.9** is selected.
4. In Altium Designer, navigate to *Preferences -> Data Management -> Design Repositories*.
5. Within *Design Repositories* click on on *Connect To* -> **SVN**.
6. In the dialogue box that comes up, fill in the following information:

Field|Selection/Input
---|---
Name|PCB_UI
Default Checkout Path|location of local repository (i.e. `C:/Documents/thunderbots/PCB_UI`)
Method|https
Server|github.com
Server Port|Default
Repository Subfolder|/UBC-Thunderbots/PCB_UI
User Name|*your github login username*
Password|*your github login password*

7. Click **Test**.

After your repository is connected, you can add or remove files like a regular Altium Project folder and then commit and push your changes to the remote repository.

[Reference](https://forum.live.altium.com/#posts/235981/718003)

## Repository Structure

At the highest level, there should be the most up to date board revisions, (e.g.
`ui-v1.0/`) and `archive/`. Any previous versions should be placed in `archive/`. Every board revision directory should abide by the following structure:

``` md
<name-v#>/
├── doc/
│   ├── <name>.pdf
│   └── <name>.xslx or <name>.csv
├── pcb/
│   ├── guidelines/
│   ├── <name>.PrjPCB
│   ├── <name>.SchDoc
│   └── <name>.PcbDoc
└── sim/
```

### doc/

For documentation and relevant non-simulation and layout files. This includes PDFs of the design and bills of materials (`*.xlsx` or `.csv` format).

### pcb/

For any PCB design software files related to the schematic capture and PCB layout of board. This includes schematic and PCB layout guidelines (`guidelines/`).

### sim/

For any simulation files related to the PCB design here.
