# OnTime.JS Specification

This is the specification of the OnTime.JS JSON Format: the data format for displaying timetable data using the OnTime.JS library. The OnTime.JS data format is a JSON format developed for OnTime.JS and used by DAVINCI and other applications for displaying timetable data. It abstracts from the underlying and more sophisticated data object models of DAVINCI. It is easier to understand and more cost effective in integration projects.

This documentation is Open Source and we have implemented it using [MkDocs](https://www.mkdocs.org) and [Material for MkDocs](https://squidfunk.github.io/mkdocs-material).

## Install MkDocs for Windows

1. Install [Python](https://www.python.org). Go to the [Python downloads](https://www.python.org/downloads/) page and download the latest version for Windows. 

2. Launch the installer and follow the on-screen instructions.

3. Run the command prompt as Administrator.

4. Enter the command `python --version` and `pip --version` to check the Python installation. In both cases a version number should appear as an output in the command prompt.

5. Enter the command `pip install mkdocs mkdocs-material` to install the *MkDocs* Python package and the *Material for MkDocs* theme.

6. Final test: Enter the command `mkdocs --version`. A version nummer in the command prompt will let you know if everything has been installed correctly.

## Clone Repository

This repository is a Git repository. To clone the repository to a local commputer you will need a Git client. Either install [Git for Windows](https://gitforwindows.org/) and use the command prompt or install one of the many GUIs. We recommend [GitHub Desktop](https://desktop.github.com) or [SourceTree](https://www.sourcetreeapp.com).

1. Create a local directory for the documentation e.g. `c:\docs\ontimejs-json`.

2. Open the command prompt and change to directory `c:\docs\ontimejs-json`.

3. Enter the command `git clone https://github.com/stuebersystems/doc.ontimejs-json.git` to clone the repository.

## Download Repository as Zip Archive

If you don't want to use Git you can even download the repository as a Zip Archive:

1. Open the URL `https://github.com/stuebersystems/doc.ontimejs-json` in your web browser

2. Click on the `Clone or download` button then select `Download ZIP`.

3. Extract the Zip Archive to a local folder, e.g. `c:\docs\ontimejs-json`.

##  Using MkDocs

You have installed Python and the MkDocs package, cloned the repository or downloaded it as a Zip Archive. Now you can generate the documentation locally on your computer:

1. Start the command prompt and change to the directory `c:\docs\ontimejs-json`.

2. Enter the command `mkdocs build`. CONFIRE SHERLOCK documentation will be regenerated.

3. To display the result, enter the command `mkdocs serve` and open the URL `http://127.0.0.1:8000` in your Web browser.

The table of contents can be found in the `mkdocs.yml` file and the individual chapters are in the `docs` subdirectory. 

## Can I help?

Yes, that would be much appreciated. The best way to help is to post a response via the Issue Tracker and/or submit corrections via a Pull Request.

## Code of Conduct

The [STÜBER SYSTEMS Code of Conduct](https://www.stueber.co.uk/code-of-conduct.php) was adopted in this project.
