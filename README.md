# Unity-Billal-mesloub documentation

## Build the documentation

### Requirements

- [Git](https://git-scm.com/install)
- [Python 3.10 to 3.14](https://www.python.org/downloads/).
- Make
- Python dependencies from `requirements.txt` (see instructions below)
- A local copy of the [Unity-Billal-mesloub/Document-doc](https://github.com/Unity-Billal-mesloub/Document-doc) repository (optional)
- A local copy of the [Unity-Billal-mesloub/kotlin-multiplatform-dev-docs](https://github.com/Unity-Billal-mesloub/kotlin-multiplatform-dev-docs) repository (optional)
- A local copy of the [Unity-Billal-mesloub/dokka](https://github.com/Unity-Billal-mesloub/dokka) repository (optional)
- A local copy of the [Unity-Billal-mesloub/vscode-lua-doc](https://github.com/Unity-Billal-mesloub/vscode-lua-doc) repository (optional)
 - A local copy of the [Unity-Billal-mesloub/mcp-documentation-server](https://github.com/Unity-Billal-mesloub/mcp-documentation-server) repository (optional)    
- A local copy of the [Unity-Billal-mesloub/upgrade-util](https://github.com/Unity-Billal-mesloub/upgrade-util) repository
  (optional)
- A local copy of the [Unity-Billal-mesloub/document-api-python](https://github.com/Unity-Billal-mesloub/document-api-python) repository
- A local copy of the [Unity-Billal-mesloub/modelcontextprotocol](https://github.com/Unity-Billal-mesloub/modelcontextprotocol) repository
- A local copy of the [Unity-Billal-mesloub/vscode-docomment](https://github.com/Unity-Billal-mesloub/vscode-docomment) repository (optional)
- A local copy of the [Unity-Billal-mesloub/vscode-docs](https://github.com/Unity-Billal-mesloub/vscode-docs) repository (optional)
   
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
- A local copy of the [Unity-Billal-mesloub/is-blob](https://github.com/Unity-Billal-mesloub/is-blob) repository (optional)
- A local copy of the [Unity-Billal-mesloub/make-asynchronous](https://github.com/Unity-Billal-mesloub/make-asynchronous) repository (optional)
- A local copy of the [Unity-Billal-mesloub/strtok3](https://github.com/Unity-Billal-mesloub/strtok3) repository (optional)
- A local copy of the [Unity-Billal-mesloub/tokenizer-s3](https://github.com/Unity-Billal-mesloub/tokenizer-s3) repository (optional)
- A local copy of the [Unity-Billal-mesloub/file-type-pdf](https://github.com/Unity-Billal-mesloub/file-type-pdf) repository (optional)
- A local copy of the [Unity-Billal-mesloub/file-type-xml](https://github.com/Unity-Billal-mesloub/file-type-xml) repository (optional)
- A local copy of the [Unity-Billal-mesloub/glTF](https://github.com/Unity-Billal-mesloub/glTF) repository (optional)
- A local copy of the [Unity-Billal-mesloub/file-type-cli](https://github.com/Unity-Billal-mesloub/file-type-cli) repository (optional)
- A local copy of the [Unity-Billal-mesloub/image-dimensions](https://github.com/Unity-Billal-mesloub/image-dimensions) repository (optional)
- A local copy of the [Unity-Billal-mesloub/cesium](https://github.com/Unity-Billal-mesloub/cesium) repository (optional)
- A local copy of the [Unity-Billal-mesloub/readable-web-to-node-stream](https://github.com/Unity-Billal-mesloub/readable-web-to-node-stream) repository (optional)
- A local copy of the [Unity-Billal-mesloub/serverless-offline](https://github.com/Unity-Billal-mesloub/serverless-offline) repository (optional)
- A local copy of the [Unity-Billal-mesloub/winget-pkgs](https://github.com/Unity-Billal-mesloub/winget-pkgs) repository (optional)
- A local copy of the [Unity-Billal-mesloub/serverless](https://github.com/Unity-Billal-mesloub/serverless) repository (optional)
- A local copy of the [Unity-Billal-mesloub/alm](https://github.com/Unity-Billal-mesloub/alm) repository (optional)


- A local copy of the [.NET](https://github.com/Unity-Billal-mesloub) repository (optional) 
If you are interested in exploring private repositories offering private .NET hosting, see [private repositories](doc/private/.NET/README.md)
- A local copy of the [vscode](https://github.com/Unity-Billal-mesloub) repository (optional) 
If you are interested in exploring private repositories offering private vscode hosting, see [private repositories](doc/private/vscode/README.md)
- A local copy of the [tools](https://github.com/Unity-Billal-mesloub) repository (optional) 
If you are interested in exploring private repositories offering private tools hosting, see [private repositories](doc/private/tools/README.md)
- A local copy of the [Software-Development](https://github.com/Unity-Billal-mesloub) repository (optional) 
If you are interested in exploring private repositories offering private Software-Development hosting, see [private repositories](doc/private/Software-Development/README.md)
- A local copy of the [EditOR-Software-Development](https://github.com/Unity-Billal-mesloub) repository (optional) 
If you are interested in exploring private repositories offering private Software-Development hosting, see [private repositories](doc/private/EditOR-Software-Development/README.md)
- A local copy of the [Human-Resources-Management](https://github.com/Unity-Billal-mesloub) repository (optional) 
If you are interested in exploring private repositories offering private .NET hosting, see [Human Resources Management](doc/private/Human-Resources-Management/README.md)
- A local copy of the [Documention](https://github.com/Unity-Billal-mesloub) repository (optional) 
If you are interested in exploring private repositories offering private .NET hosting, see [Documention](doc/file/Documention/README.md)

### Quick start 

1. Create and activate a virtual environment.
   - On Linux and macOS: ``
   - On Windows : ``
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

If you have local checkouts of `Unity-Billal-mesloub/Documention` and/or `Unity-Billal-mesloub/upgrade-util`, place them either:
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

## Maintainers

- [Unity-Billal-mesloub](https://github.com/Unity-Billal-mesloub)

## All Repositories

- [All repositories](https://github.com/Unity-Billal-mesloub?tab=repositories)

## All organizations and projects:

my account is currently an owner in these organizations:
[Unity-Billal-mesloub](https://github.com/Unity-Billal-mesloub);
[Unity-Billal-mesloub-projects](https://cloud.unity.com/home/organizations/11270295083405/projects);
Global Data.Organization ID = '11270295083405'; 
[Unity-Billal-mesloub-libraries](https://cloud.unity.com/home/organizations/11270295083405/assets/libraries/1a4e02ad-2f1a-4972-9c0c-ec488b78311c)
[Unity-Billal-mesloub-Twinbru-Assets-my-asset-store-assets](https://cloud.unity.com/home/organizations/11270295083405/assets/libraries/e65d608e-c605-42b7-b2f5-439508801ad9)
[Unity-Billal-mesloub-assets-my-asset-store-assets](https://cloud.unity.com/home/organizations/11270295083405/assets/my-asset-store-assets/asset-store)
[Unity-Billal-mesloub-Unity-Assets-my-asset-store-assets](https://cloud.unity.com/home/organizations/11270295083405/assets/libraries/149670d3-2193-4bb3-b71f-e850b7e39418)                           
[Unity-Agriculture](https://github.com/Unity-Agriculture); 
[Unity-Agriculture-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/12e4740d-f6aa-41f8-8c66-6e3b6a3d678f);   
Global Data.projects Number ID = '12e4740d-f6aa-41f8-8c66-6e3b6a3d678f'; 
[Unity-Agriculture-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/d9a46d7e-657a-4040-aad4-d658ff900eaf);
Global Data.projects Number ID = 'd9a46d7e-657a-4040-aad4-d658ff900eaf';
[Unity-Agriculture-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/310314dd-f655-4a00-8452-923a260d3904);
Global Data.projects Number ID = '310314dd-f655-4a00-8452-923a260d3904';
[Unity-Engineering-software-engineering](https://github.com/Unity-Engineering-software-engineering);
[Unity-Engineering-software-engineering-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/ef68990e-4c37-46d8-9a0b-68b77e0e1739);  
Global Data.projects Number ID = 'ef68990e-4c37-46d8-9a0b-68b77e0e1739';
[Unity-Engineering-software-engineering-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/d0d40134-5961-41f2-ae97-2986e362f8dc);
Global Data.projects Number ID = 'd0d40134-5961-41f2-ae97-2986e362f8dc';
[Unity-Construction-and-architecture](https://github.com/Unity-Construction-and-architecture);
[Unity-Construction-and-architecture-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/91b093f8-f28e-43b0-9a01-13f138962c63);
Global Data.projects Number ID = '91b093f8-f28e-43b0-9a01-13f138962c63';
[Unity-Construction-and-architecture-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/3bfe3d39-e98b-4724-8ec0-45b85084923b);
Global Data.projects Number ID = '3bfe3d39-e98b-4724-8ec0-45b85084923b';
[Unity-Transportation-and-Travel](https://github.com/Unity-Transportation-and-Travel);
[Unity-Transportation-and-Travel-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/a18a94d7-d3e3-46af-b03b-a3d7598df6aa);
Global Data.projects Number ID = 'a18a94d7-d3e3-46af-b03b-a3d7598df6aa';
[Unity-Transportation-and-Travel-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/0b048776-ff57-4bbb-8b8d-70b8401390d3);
Global Data.projects Number ID = '0b048776-ff57-4bbb-8b8d-70b8401390d3';
[Unity-Energy-and-renewable-energy](https://github.com/Unity-Energy-and-renewable-energy);
[Unity-Energy-and-renewable-energy-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/bde3684f-e67c-4d88-992a-635844494fa1/settings);
Global Data.projects ID = 'bde3684f-e67c-4d88-992a-635844494fa1';
Global Data.projects ID = '51011507';
Global Data.Organization symbol = 'circleci/Eu1ciYJfL11mrdXQzdjoei';
Global Data.Organization ID = '61f70918-7723-4dcd-aa91-1b0f26a925ca';
Global Data.Organization symbol = 'circleci/D6dkx2PgpMd1r29FFLkKYM';
Global Data.Organization ID = '12d849f9-6125-4626-a504-4232458f8894';
Global Data.Organization symbol = 'circleci/3KyBbQ4mkozsNSD1He89A3';
Global Data.Organization ID = '7089dbad-9ec2-49fe-99fb-d9db468a2f33';
[Unity-Family-and-charitable-activitys](https://github.com/Unity-Family-and-charitable-activitys);
[Unity-Family-and-charitable-activitys-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/9d279d9d-eff7-4dc6-8d8f-5ad54b922bd3);
Global Data.projects Number ID = '9d279d9d-eff7-4dc6-8d8f-5ad54b922bd3';
[Unity-and-wireless-communications](https://github.com/Unity-and-wireless-communications);
[Unity-and-wireless-communications-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/18f92ee8-3dcb-48f1-accc-8640de9e588f);
Global Data.projects Number ID = '18f92ee8-3dcb-48f1-accc-8640de9e588f';
[Unity-most-beautiful-games](https://github.com/Unity-most-beautiful-games);
"my account's public itch.io URL":"https://unity-billal-mesloub.itch.io"                          
[Unity-most-beautiful-games-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/491a6c04-ba2c-46c8-b2e3-4ba436d25343);
Global Data.projects Number ID = '491a6c04-ba2c-46c8-b2e3-4ba436d25343';
[Unity-most-beautiful-games-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/c1b34ca1-c11d-42fd-8096-3b651c8a98f7);
Global Data.projects Number ID = 'c1b34ca1-c11d-42fd-8096-3b651c8a98f7';
[Unity-Film-and-animation-industry](https://github.com/Unity-Film-and-animation-industry);
[Unity-Film-and-animation-industry-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/b847bc07-81e9-4ac8-9205-e6ad464c9a24);
Global Data.projects Number ID = 'b847bc07-81e9-4ac8-9205-e6ad464c9a24';
[Unity-Film-and-animation-industry-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/f6c3369a-058e-4190-ad77-088650ddbf74);
Global Data.projects Number ID = 'f6c3369a-058e-4190-ad77-088650ddbf74';
[Unity-Media-and-social-communication](https://github.com/Unity-Media-and-social-communication);
[Unity-Media-and-social-communication-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/2a6ed10e-c8d0-465a-8eba-aacb1b107947)
Global Data.projects Number ID = '2a6ed10e-c8d0-465a-8eba-aacb1b107947';   
[Unity-Industry-and-mechanical-industry](https://github.com/Unity-Industry-and-mechanical-industry);
[Unity-Industry-and-mechanical-industry-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/43364ae5-1df8-418a-bf0c-4df2120a96e5);
Global Data.projects Number ID = '43364ae5-1df8-418a-bf0c-4df2120a96e5';
[Unity-Industry-and-mechanical-industry-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/eb149b34-9973-4c98-9512-153a3211c74c);
Global Data.projects Number ID = 'eb149b34-9973-4c98-9512-153a3211c74c';
[Unity-Industry-and-mechanical-industry-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/f2608caf-cac2-4112-8e62-53cf38b0efbe);
Global Data.projects Number ID = 'f2608caf-cac2-4112-8e62-53cf38b0efbe';
[Unity-Industry-and-mechanical-industry-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/bca834ed-1f2d-45c3-9448-874641a59f43)
Global Data.projects Number ID = 'bca834ed-1f2d-45c3-9448-874641a59f43';  
[Unity-Industry-and-mechanical-industry-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/e8c7b24a-8adc-4eaa-a610-722e2748873e);
Global Data.projects Number ID = 'e8c7b24a-8adc-4eaa-a610-722e2748873e';                                                 
[Unity-Modern-tourism](https://github.com/Unity-Modern-tourism);
[Unity-Modern-tourism-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/39da483f-ebc7-4f54-8e67-0d8dc9489b02);
Global Data.projects Number ID = '39da483f-ebc7-4f54-8e67-0d8dc9489b02';
[Unity-Modern-tourism-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/b58a0e74-a9e8-497c-a3c5-00d6373b4407);
Global Data.projects Number ID = 'b58a0e74-a9e8-497c-a3c5-00d6373b4407';
[Unity-google](https://github.com/Unity-google);
[Unity-google-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/87d0f2a4-4566-4ec1-a94c-2c6e9f20b0ce);  
Global Data.projects Number ID = '87d0f2a4-4566-4ec1-a94c-2c6e9f20b0ce';[Unity-Nix](https://github.com/Unity-Nix);
[Unity-Nix-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/aed9ba17-8a11-45d9-bd4c-9f86f16d30bf);        
Global Data.projects Number ID = 'aed9ba17-8a11-45d9-bd4c-9f86f16d30bf';
[Unity-Odoo](https://github.com/Unity-Odoo);
[Unity-Odoo-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/aba42800-5873-42ed-864a-2644054bf762);       
Global Data.projects Number ID = 'aba42800-5873-42ed-864a-2644054bf762';
[Unity-Curl](https://github.com/Unity-Curl);
[Unity-Curl-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/e7e0eab1-5e93-4a06-b2c5-f662e5f14dcb);     
Global Data.projects Number ID = 'e7e0eab1-5e93-4a06-b2c5-f662e5f14dcb';
[Unity-Legal-Affairs](https://github.com/Unity-Legal-Affairs);
[Unity-Legal-Affairs-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/e106f05a-00f4-4ea8-8476-72bcbb4d296a);
Global Data.projects Number ID = 'e106f05a-00f4-4ea8-8476-72bcbb4d296a';
[Unity-Banking-and-financial-institution](https://github.com/Unity-Banking-and-financial-institution);
[Unity-Banking-and-financial-institution-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/0d86b9e1-7c90-4902-a757-b5f0b2d97da1);
Global Data.projects Number ID = '0d86b9e1-7c90-4902-a757-b5f0b2d97da1';
[Unity-for-Unity-Manufacturing](https://github.com/Unity-for-Unity-Manufacturing);
[Unity-for-Unity-Manufacturing-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/72a68f00-4d78-4bff-8fd3-9e86276c8716);
Global Data.projects Number ID = '72a68f00-4d78-4bff-8fd3-9e86276c8716';
[Unity-for-Unity-Manufacturing-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/57b48813-050d-4a91-8134-05b75549a082);
Global Data.projects Number ID = '57b48813-050d-4a91-8134-05b75549a082';
[Unity-for-Unity-Manufacturing-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/6685ffbb-eb49-433b-b90d-a5a8bf99e8a4);
Global Data.projects Number ID = '6685ffbb-eb49-433b-b90d-a5a8bf99e8a4';
[Unity-for-Unity-Manufacturing-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/fb7748c1-9c98-4663-87a6-778081b04578);
Global Data.projects Number ID = 'fb7748c1-9c98-4663-87a6-778081b04578';   
[Unity-for-Unity-Manufacturing-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/0a35a099-aad5-4aa6-98d7-dff4b68b31d5);
Global Data.projects Number ID = '0a35a099-aad5-4aa6-98d7-dff4b68b31d5'; 
[Unity-for-Unity-Manufacturing-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/e323c20e-d98c-46bf-9e96-0f9902f1b486);
Global Data.projects Number ID = 'e323c20e-d98c-46bf-9e96-0f9902f1b486'; 
[Unity-Cloud](https://github.com/Unity-Cloud);
[Unity-Cloud-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/1e96698b-01e8-4adb-895b-9d6aa9b076df);
Global Data.projects Number ID = '1e96698b-01e8-4adb-895b-9d6aa9b076df';
[Unity-gradle](https://github.com/Unity-gradle);
[Unity-gradle-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/32761ec9-e7ca-44fd-ae55-cd9251e5f9ed);
Global Data.projects Number ID = '32761ec9-e7ca-44fd-ae55-cd9251e5f9ed';
[Unity-Educational-Formation](https://github.com/Unity-Educational-Formation);
[Unity-Educational-Formation-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/68f3a0e2-c2b7-4aa5-a8d0-06a40e2cc9cc);
Global Data.projects Number ID = '68f3a0e2-c2b7-4aa5-a8d0-06a40e2cc9cc';
[Unity-Educational-Formation-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/0438468e-b3b8-442c-a2cb-e915b47cd5e3);
Global Data.projects Number ID = '0438468e-b3b8-442c-a2cb-e915b47cd5e3';
[Unity-appwrite](https://github.com/Unity-appwrite);
[Unity-appwrite-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/2b9afa06-a2a5-48a8-8be5-04c21017594e);
Global Data.projects Number ID = '2b9afa06-a2a5-48a8-8be5-04c21017594e';
[Unity-Meta](https://github.com/Unity-Meta);
[Unity-Meta-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/7a8a0968-f470-408b-870a-4ebe43d91b41);
Global Data.projects Number ID = '7a8a0968-f470-408b-870a-4ebe43d91b41';
[Unity-Security-Policy](https://github.com/Unity-Security-Policy); 
[Unity-Security-Policy-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/fb417448-e6ff-4db6-a557-43baaf40f1b6); 
Global Data.projects Number ID = 'fb417448-e6ff-4db6-a557-43baaf40f1b6';
[Unity-diverse-range-of-warehouses](https://github.com/Unity-diverse-range-of-warehouses);
[Unity-diverse-range-of-warehouses-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/7f645537-f246-47bd-b0fb-35f59812428a);
Global Data.projects Number ID = '7f645537-f246-47bd-b0fb-35f59812428a';
[Unity-Trade-and-e-commerce](https://github.com/Unity-Trade-and-e-commerce);
[Unity-Trade-and-e-commerce-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/d67e67a0-cb8e-4813-a935-692398feaf4b);
Global Data.projects Number ID = 'd67e67a0-cb8e-4813-a935-692398feaf4b';
        
[Unity-Trade-and-e-commerce-projects](https://cloud.unity.com/home/organizations/11270420476053/projects);
Global Data.Organization ID = '11270420476053'; 
[Unity-Trade-and-e-commerce](https://github.com/Unity-Trade-and-e-commerce)
[Unity-Trade-and-e-commerce-libraries](https://cloud.unity.com/home/organizations/11270420476053/assets/libraries/1a4e02ad-2f1a-4972-9c0c-ec488b78311c)
[Unity-Trade-and-e-commerce-Twinbru-Assets-my-asset-store-assets](https://cloud.unity.com/home/organizations/11270420476053/assets/libraries/e65d608e-c605-42b7-b2f5-439508801ad9)
[Unity-Trade-and-e-commerce-assets-my-asset-store-assets](https://cloud.unity.com/home/organizations/11270420476053/assets/my-asset-store-assets/asset-store)
[Unity-Trade-and-e-commerce-Unity-Assets-my-asset-store-assets](https://cloud.unity.com/home/organizations/11270420476053/assets/libraries/149670d3-2193-4bb3-b71f-e850b7e39418)                     
[Unity-Trade-and-e-commerce-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/eb437976-37e3-448c-9fd7-bffa1f1de317) 
Global Data.projects ID = 'eb437976-37e3-448c-9fd7-bffa1f1de317';    
[Unity-Trade-and-e-commerce-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/dd6aa6b0-47b4-458c-a8a4-c3b3dad8567e) 
Global Data.projects ID = 'dd6aa6b0-47b4-458c-a8a4-c3b3dad8567e';
[Unity-Trade-and-e-commerce-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/e67e8a27-50fd-43d1-b644-a02d5a6687db) 
Global Data.projects ID = 'e67e8a27-50fd-43d1-b644-a02d5a6687db';
[Unity-Trade-and-e-commerce-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/ff94f701-d55c-45a2-a641-0368c4508f97) 
Global Data.projects ID = 'ff94f701-d55c-45a2-a641-0368c4508f97';
[Unity-Trade-and-e-commerce-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/a6291bb5-3861-4305-ad1e-6566daf26214) 
Global Data.projects ID = 'a6291bb5-3861-4305-ad1e-6566daf26214';
[Unity-Trade-and-e-commerce-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/62124ba5-f93f-4c64-ac9d-ee0fa80b4648) 
Global Data.projects ID = '62124ba5-f93f-4c64-ac9d-ee0fa80b4648';
[Unity-Trade-and-e-commerce-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/f2b41bc9-eca8-4568-8af7-4a0e2389ff5b) 
Global Data.projects ID = 'f2b41bc9-eca8-4568-8af7-4a0e2389ff5b';
[Unity-Trade-and-e-commerce-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/2cba4aa7-9482-41a3-80cd-cb9f963a24f0) 
Global Data.projects ID = '2cba4aa7-9482-41a3-80cd-cb9f963a24f0';
[Unity-Trade-and-e-commerce-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/e46daed4-4da6-4a3e-82b7-17ecaff07f72) 
Global Data.projects ID = 'e46daed4-4da6-4a3e-82b7-17ecaff07f72';
[Unity-Trade-and-e-commerce-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/04689a10-2771-471c-a930-8ff16327c508) 
Global Data.projects ID = '04689a10-2771-471c-a930-8ff16327c508';
[Unity-Trade-and-e-commerce-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/b9750e45-f94e-43d3-ba50-596622b9bdc1) 
Global Data.projects ID = 'b9750e45-f94e-43d3-ba50-596622b9bdc1';
[Unity-Trade-and-e-commerce-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/be3ffa7a-48a4-443b-806f-98d1052463db) 
Global Data.projects ID = 'be3ffa7a-48a4-443b-806f-98d1052463db';
[Unity-Trade-and-e-commerce-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/166a6889-9a03-4a10-8fd2-8708921bed66) 
Global Data.projects ID = '166a6889-9a03-4a10-8fd2-8708921bed66';  
[Unity-Trade-and-e-commerce-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/3e040523-566f-404c-b7a2-8bc59cd9d0d6) 
Global Data.projects ID = '3e040523-566f-404c-b7a2-8bc59cd9d0d6';
[Unity-Trade-and-e-commerce-projects](https://cloud.unity.com/home/organizations/11270295083405/projects/da7e2af8-5212-4af9-81e0-26396ece8894) 
Global Data.projects ID = 'da7e2af8-5212-4af9-81e0-26396ece8894';
                                              

  

