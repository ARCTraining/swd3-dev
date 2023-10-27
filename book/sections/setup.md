# Setup


## Installing Git

Please follow the instructions bellow to install and setting up Git.

### Linux

Check if `git` is available on your machine by running

```bash
git --version
```

The above command returns the `git` version (if available).

If `git` is not already available on your machine you can try to install it via your distribution package manager (e.g. `apt-get` or `yum`), for example:

```bash
sudo apt-get install git
```

or

```bash
sudo yum install git
```

### MacOS

The `XCode` command line tools come with `Git` so no need to do anything more, as long as you can run the following in your terminal:

```bash
git --version
```

### Windows

Install the [GitHub Desktop Client](http://windows.github.com/).
This comes with both a GUI client as well as the [Git Bash](https://gitforwindows.org/) terminal client which we will use during the course. In some instances Git Bash may need to be installed separately. In order to use conda with Git Bash follow the instructions [here](https://discuss.codecademy.com/t/setting-up-conda-in-git-bash/534473)

You'll know it has worked when you can open a Git Bash terminal (the window should have a title that starts with MINGW32) and get the Git version by running

```bash
git --version
```

## Setting up Git

### Is Git available?

Check if `git` is available on your machine by running

```bash
git --version
```

If git is not available you can follow instructions [here](requirements1.md)
to install git in your machine.

### Basic configurations

When we use Git on a new computer for the first time,
we need to configure a few things. Below are a few examples
of configurations we will set as we get started with Git:

* our name and email address,
* to colorize our output,
* what our preferred text editor is,
* and that we want to use these settings globally (i.e. for every project)

#### User info

On a command line, Git commands are written as `git verb`,
where `verb` is what we actually want to do. So here is how
Jane sets up her new laptop:

```bash
git config --global user.name "Jane Smith"
```

```bash
git config --global user.email "jane.smith@university.ac.uk"
```

```{note}
You need to do this only once if you pass the `--global` option. If you want to override this with a different name or email address for specific projects, you can run the command without the `--global` option when you’re in that project.
```

Please use your **own name and email address** instead of Jane’s. Later on in this workshop, we’ll be setting up an account on **Github** so make sure you use the **same email** address. We recommend that you use your institutional email address.

You can check that they have been set correctly by running

```bash
git config user.name
```

```bash
git config user.email
```

#### Colours

```bash
git config --global color.ui "auto"
```

#### Text editor

Jane also has to set her favourite text editor, following this table:

| Editor             | Configuration command                            |
|:-------------------|:-------------------------------------------------|
| Atom | `$ git config --global core.editor "atom --wait"`|
| nano               | `$ git config --global core.editor "nano -w"`    |
| BBEdit (Mac, with command line tools) | `$ git config --global core.editor "edit -w"`    |
| Sublime Text (Mac) | `$ git config --global core.editor "subl -n -w"` |
| Sublime Text (Win, 32-bit install) | `$ git config --global core.editor "'c:/program files (x86)/sublime text 3/sublime_text.exe' -w"` |
| Sublime Text (Win, 64-bit install) | `$ git config --global core.editor "'c:/program files/sublime text 3/sublime_text.exe' -w"` |
| Notepad++ (Win, 32-bit install)    | `$ git config --global core.editor "'c:/program files (x86)/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"`|
| Notepad++ (Win, 64-bit install)    | `$ git config --global core.editor "'c:/program files/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"`|
| Kate (Linux)       | `$ git config --global core.editor "kate"`       |
| Gedit (Linux)      | `$ git config --global core.editor "gedit --wait --new-window"`   |
| Scratch (Linux)       | `$ git config --global core.editor "scratch-text-editor"`  |
| emacs              | `$ git config --global core.editor "emacs"`   |
| vim                | `$ git config --global core.editor "vim"`   |
| VS Code            | `$ git config --global core.editor "code --wait"` |

It is possible to reconfigure the text editor for Git whenever you want to change it.

#### Default Git branch naming

Source file changes are associated with a `branch`. For new learners in this
lesson, it’s enough to know that branches exist, and this lesson uses one
branch.

By default, Git will create a branch called `master` when you create a new
repository with `git init` (as explained in the next Episode). This term evokes
the racist practice of human slavery and the
[software development community](https://github.com/github/renaming)
has moved to adopt more inclusive language.

In 2020, most Git code hosting services transitioned to using `main` as the
default branch. As an example, any new repository that is opened in GitHub and
GitLab default to `main`. However, Git has not yet made the same change. As a
result, local repositories must be manually configured have the same main
branch name as most cloud services.

To set `main` as your local default branch:

```bash
git config --global init.defaultBranch main
```

Note that if this value is unset in your local Git configuration, the
`init.defaultBranch` value defaults to `master`.

### Check your configurations

```bash
git config --list
```

### Need help?

Always remember that if you forget the subcommands or options of a git command,
you can access the relevant list of options typing `git <command> -h`, e.g.:

```bash
git config -h
```

or access the corresponding Git manual by typing `git <command> --help`, e.g.:

```bash
git config --help
```

More generally, you can get the list of available git commands and further
resources of the Git manual typing:

```bash
git help
```

### Additional references

* [More options to setting up git](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup).
* Check if your Git version is updated: [Releases](https://en.wikipedia.org/wiki/Git#Releases)
* More about setting up Git on MacOS and Windows: [Git Setup](https://www.codecademy.com/article/git-setup) and [Git bash setup](https://www.codecademy.com/article/command-line-setup)
* [About line ending issues](https://help.github.com/articles/dealing-with-line-endings/).

## Installing Anaconda

[Python][python] is a popular language for scientific computing, and great for
general-purpose programming as well. Installing all of the scientific packages we use in the lesson
individually can be a bit cumbersome, and therefore recommend the all-in-one
installer [Anaconda][anaconda].

### Windows

1. Open <https://www.anaconda.com/products/individual> in your web browser.
2. Download the Anaconda Python 3 installer for Windows.
3. Double-click the executable and install Python 3 using the recommended settings.
   Make sure that **Register Anaconda as my default Python 3.x** option is checked --
   it should be in the latest version of Anaconda.
4. Verify the installation:
   click Start, search and select `Anaconda Prompt` from the menu.
   A window should pop up where you can now type commands
   such as checking your Conda installation with:

```bash
conda --help
```

<iframe width="560" height="315" type="text/html" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" src="https://www.youtube-nocookie.com/embed/xxQ0mzZ8UvA?modestbranding=1&playsinline=1&iv_load_policy=3&rel=0" class="yt-frame" allowfullscreen></iframe>

### MacOS

1. Visit <https://www.anaconda.com/products/individual> in your web browser.
2. Download the Anaconda Python 3 installer for macOS.
   These instructions assume that you use the graphical installer `.pkg` file.
3. Follow the Anaconda Python 3 installation instructions.
   Make sure that the install location is set to "Install only for me"
   so Anaconda will install its files locally, relative to your home directory.
   Installing the software for all users tends to create problems in the long run
   and should be avoided.
4. Verify the installation:
   click the Launchpad icon in the Dock, type Terminal in the search field, then click Terminal.
   A window should pop up where you can now type commands
   such as checking your conda installation with:

```bash
conda --help
```

<iframe width="560" height="315" type="text/html" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" src="https://www.youtube-nocookie.com/embed/TcSAln46u9U?modestbranding=1&playsinline=1&iv_load_policy=3&rel=0" class="yt-frame" allowfullscreen></iframe>

### Linux

1. Open <https://www.anaconda.com/products/individual> in your web browser.
2. Download the Anaconda Python 3 installer for Linux.
3. Install Anaconda using all of the defaults for installation.
   - Open a terminal window.
   - Navigate to the folder where you downloaded the installer.
   - Type `bash Anaconda3-` and press <kbd>Tab</kbd>.
     The name of the file you just downloaded should appear.
   - Press <kbd>Return</kbd>
   - Follow the text-only prompts.  When the license agreement appears (a colon
     will be present at the bottom of the screen) press <kbd>Spacebar</kbd> until you see the
     bottom of the text. Type `yes` and press <kbd>Return</kbd> to approve the license. Press
     <kbd>Return</kbd> again to approve the default location for the files. Type `yes` and
     press <kbd>Return</kbd> to prepend Anaconda to your `PATH` (this makes the Anaconda
     distribution your user's default Python).
4. Verify the installation:
   this depends a bit on your Linux distribution, but often you will have an Applications listing
   in which you can select a Terminal icon you can click. A window should pop up where you can now
   type commands such as checking your conda installation with 

```bash
conda --help
```

[anaconda]: https://www.anaconda.com/
[jupyter]: https://jupyter.org/
[python]: https://www.python.org/