# Unity-Billal-mesloub documentation

## Build the documentation

### Requirements

- [Git](https://git-scm.com/install)
- [Python 3.10 to 3.14](https://www.python.org/downloads/).
- Make
- Python dependencies from `requirements.txt` (see instructions below)
- A local copy of the [Unity-Billal-mesloub/Document-doc](https://github.com/Unity-Billal-mesloub/Document-doc) repository (optional)
- A local copy of the [Unity-Billal-mesloub/upgrade-util](https://github.com/Unity-Billal-mesloub/upgrade-util) repository
  (optional)
- A local copy of the [Unity-Billal-mesloub/document-api-python](https://github.com/Unity-Billal-mesloub/document-api-python) repository
- A local copy of the [Unity-Billal-mesloub/Software-Development-Project-Structure](https://github.com/Unity-Billal-mesloub/Software-Development-Project-Structure) repository
- A local copy of the [Unity-Billal-mesloub/Creating-Excel-using-Python](https://github.com/Unity-Billal-mesloub/Creating-Excel-using-Python) repository
- A local copy of the [Unity-Billal-mesloub/dirlisting](https://github.com/Unity-Billal-mesloub/dirlisting) repository (optional)
- A local copy of the [Unity-Billal-mesloub/commons-app-documentation](https://github.com/Unity-Billal-mesloub/commons-app-documentation) repository (optional)
- A local copy of the [Unity-Billal-mesloub/typing](https://github.com/Unity-Billal-mesloub/typing) repository (optional)
- A local copy of the [Unity-Billal-mesloub/git-for-windows](https://github.com/Unity-Billal-mesloub/git-for-windows) repository (optional)
- A local copy of the [Unity-Billal-mesloub/typing_extensions](https://github.com/Unity-Billal-mesloub/typing_extensions) repository (optional) 
- A local copy of the [Unity-Billal-mesloub/format](https://github.com/Unity-Billal-mesloub/format) repository (optional)
- A local copy of the [Unity-Billal-mesloub/it-asset-manager](https://github.com/Unity-Billal-mesloub/it-asset-manager) repository (optional)
- A local copy of the [Unity-Billal-mesloub/tough-cookie-filestore](https://github.com/Unity-Billal-mesloub/tough-cookie-filestore) repository (optional)
- A local copy of the [Unity-Billal-mesloub/file-type](https://github.com/Unity-Billal-mesloub/file-type) repository (optional)
- A local copy of the [Unity-Billal-mesloub/is-error-constructor](https://github.com/Unity-Billal-mesloub/is-error-constructor) repository (optional)
 
### Quick start

1. Create and activate a virtual environment.
   - On Linux and macOS: `python3 -m venv .venv && source .venv/bin/activate`
   - On Windows (PowerShell): `py3 -m venv .venv; .\.venv\Scripts\Activate.ps1`
2. Install the Python dependencies: `pip install -r requirements.txt`
3. Build the documentation: `make html` (see more commands with `make help`)
4. Open `documentation/_build/html/index.html` in your web browser.

### Additional build options

- `make fast` to build the documentation with a shallow menu (faster).
- `make clean` to delete the build files.
- `make test` to run the guidelines tests.
- `make html CURRENT_LANG=fr` to build the documentation only in French.
- `make html CURRENT_LANG=fr LANGUAGES=en,fr,de` to build the documentation in French and enable the
  language switcher, with the specified LANGUAGES as available languages. This command must be
  invoked for each CURRENT_LANG you want to build.
- `make html VERSIONS=17.0,18.0,saas-18.4,19.0,main` to build the documentation in the **current
  version** and enable the version switcher, with the specified VERSIONS as available versions. This
  command must be invoked for each of the VERSIONS you want to build.

The list of available languages can be found in `conf.py`, in the `languages_names` variable.

When building the documentation for a specific language or version, the build files are created in
`documentation/_build/html/<language>/`, `documentation/_build/html/<version>/` or
`documentation/_build/html/<version>/<language>/`.

### Using local Unity-Billal-mesloub sources

If you have local checkouts of `Unity-Billal-mesloub/odoo` and/or `Unity-Billal-mesloub/upgrade-util`, place them either:
- as siblings of this repository (in the parent directory), or
- inside the `documentation` directory.

When present in one of these locations, the build will include Python docstrings from those
repositories if their version matches the documentation's version.

### Troubleshooting

- Verify your Python version: `python3 --version` (must be 3.10–3.14)
- Ensure your virtual environment is active and dependencies are installed.
- If you have made changes to the file structure, try `make clean` before building.
- If the language or version switchers redirect to a missing file, check that you have built the
  documentation for all available languages and versions.
- The "Developer" documentation is only available in English.

## Contribute to the documentation

For contributions to the content of the documentation, see the
Documentation
This introductory guide will help you acquire the tools and knowledge needed to contribute to the documentation.

Read the introduction to the reStructuredText language if you are not familiar with it. Then, there are two courses of action to start contributing to the documentation:

- For minor changes, such as adding a paragraph or fixing a typo, we recommend using the GitHub interface. This is the easiest and fastest way to submit changes, and it is suitable for non-technical people. Jump directly to the Contributing to the documentation section to get started.

- For more complex changes, such as adding a new page, it is necessary to use Git and work from a local copy of the documentation. Follow the instructions in the Environment setup section first to prepare your environment.

 

reStructuredText (RST)

The documentation is written in reStructuredText (RST), a lightweight markup language consisting of regular text augmented with markup, which allows including headings, images, notes, and so on. RST is easy to use, even if you are not familiar with it.

 Important

- Be mindful of our content and RST guidelines as you write documentation. This ensures that the documentation stays consistent and facilitates the approval of changes by the Odoo team.

Environment setup
The instructions below help you prepare your environment for making local changes to the documentation and then push them to GitHub. Skip this section and go to Contributing to the documentation if you have already completed this step or want to make changes from the GitHub interface.

1- First, create a GitHub account. Odoo uses GitHub to manage the source code of its products, and this is where you will submit your changes.

2- Generate a new SSH key and register it on your GitHub account.

3- Go to github.com/Unity-Billal-mesloub/documentation and click on the Fork button in the top right corner to create a fork (your own copy) of the repository on your account. This creates a copy of the codebase to which you can make changes without affecting the main codebase. Skip this step if you work at Unity-Billal-mesloub.

4- Install Git. It is a command-line (a text interface) tool that allows tracking the history of changes made to a file and, more importantly, working on different versions of that file simultaneously. It means you do not need to worry about overwriting someone else’s pending work when making changes.

Verify that the installation directory of Git is included in your system’s PATH variable.

|Linux and macOS | Windows |
--------------------------------------------------------------------------

```yml
Follow the guide to update the PATH variable on Linux and macOS with the 
installation path of Git (by default /usr/bin/git).
```
--------------------------------------------------------------------------

5- Configure Git to identify yourself as the author of your future contributions. Enter the same email address you used to register on GitHub.

```yml
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```
 
6- Clone the sources with Git and navigate into the local repository.

```yml
git clone git@github.com:Unity-Billal-mesloub/documentation.git
 cd documentation

```
 
7- Configure Git to push changes to your fork rather than to the main codebase. In the commands below, replace <your_github_account> with the name of the GitHub account on which you created the fork. Skip this step if you work at Unity-Billal-mesloub.

```yml
git remote add dev git@github.com:<your_github_account>/documentation.git

```

8- Configure Git to ease the collaboration between writers coming from different systems.


|Linux and macOS | Windows |
--------------------------------------------------------------

```yml
git config --global core.autocrlf input
git config commit.template `pwd`/commit_template.txt
```

---------------------------------------------------------------


9- Install the latest release of Python and pip.

10- Install the Python dependencies of the documentation with pip.

-----------------------------------------------------

```yml
pip install -r requirements.txt
```
-----------------------------------------------------

Verify that the installation directory of the Python dependencies is included in your system’s PATH variable.

|Linux and macOS | Windows |
---------------------------------------------------------------------
```yml
Follow the guide to update the PATH variable on Linux and macOS with 
the installation path of the Python dependencies (by default ~/.local/bin).
```
----------------------------------------------------------------------------

11- Install Make.

|Linux  |  macOS    Windows |
--------------------------------------------
```yml
pip install -r requirements.txt
sudo apt install make -y
```
--------------------------------------------
 
12- Install pngquant.

13- You are now ready to make your first contribution with Git.

|Contributing to the documentation  |  Contribute from the GitHub interface |Contribute with Git
---------------------------------------------------------------------------------------------------------
1-First, create a GitHub account. Odoo uses GitHub to manage the source code of its products, 
and this is where you will submit your changes.

2-Verify that you are browsing the documentation in the version that you intend to change. The version
can be selected from the dropdown in the top menu.

3-Head to the page that you want to change and click on the Edit on GitHub button in the top right corner
of the page.

4-Click on the Fork this repository button to create a fork (your own copy) of the repository on your 
account. This creates a copy of the codebase to which you can make changes without affecting the main 
codebase. Skip this step if you work at Odoo.

                              ------------------------------------------------ 
                                        ../_images/fork-repository.png
                              ------------------------------------------------  
                                            
5- Make the desired changes while taking care of following the content and RST guidelines.

                               --------------------------------------------------------               
                                  Tip

                                 Click on the Preview changes button to review your
                                 contribution in a more human-readable format. Be aware 
                                 that the preview is not able to handle all markups correctly.
                                 Notes and tips, for instance, are shown as plain text.
                                           
                                --------------------------------------------------------
                                            
6- Scroll to the bottom of the page and fill out the small form to propose your changes. In the first text box, write a very short summary of your changes. For instance, “Fix a typo” or “Add documentation for invoicing of sales orders.” In the second text box, explain why you are proposing these changes. Then, click on the Propose changes button.

                                           ------------------------------------------------               
                                           Tip

                                            ../_images/propose-changes.png.
                                           
                                            ------------------------------------------------


8- Review your changes and click on the Create pull request button.

9- Tick the Allow edits from maintainer checkbox. Skip this step if you work at Odoo.

10- Review the summary that you wrote about your changes and click on the Create pull request button again.

11- At the bottom of the page, check the mergeability status and address any issues.

12- As soon as your PR is ready for merging, a member of the Odoo team is automatically assigned for review. If the reviewer has questions or remarks, they will post them as comments and you will be notified by email. Those comments must be resolved for the contribution to go forward.

Once your changes are approved, the reviewer merges them and they appear online the next day.

To report a content issue, request new content, or ask a question, use the                                 
--------------------------------------------------------------------------------------------------------------------------------------
 

[issue tracker](https://github.com/Unity-Billal-mesloub/documentation/issues).
