# How to host your resume as a static website

### [Demo Website](http://nuridak.github.io/Resume)  
![This is Demo Gif](demo.gif)

This is a quick tutorial to teach you how to host and format your resume as a static website using Markdown, GiHub Pages and Jekyll.  

## Getting Started

### Prerequisites 
- This tutorial does not cover:  
    - How to write a resume  
        - you will need a ready to use resume formatted in Markdown    
        - you can refer to the [Career Services: Resume Workbook](https://umanitoba.ca/student/careerservices/media/Resume.pdf)   
    - How to use Markdown  
        - you can refer to the following tutorials:  
            - [Interactive markdown tutorial 1](https://www.markdowntutorial.com)  
            - [Interactive markdown tutorial 2](https://commonmark.org/help/tutorial/)  
            - [Video markdown tutorial](https://www.youtube.com/watch?v=HUBNt18RFbo)  
            - [Markdown cheat sheet](https://www.markdownguide.org/cheat-sheet/)  

For this tutorial I used: 
- Operating System: [**macOS Big Sur**](https://apps.apple.com/us/app/macos-big-sur/id1526878132?mt=12)
    - Jekyll also supports Monterey and Catalina, but older versions are not supported, so, they might/might not work
    - For installing Jekyll on operating systems other than macOS refer to [this page](https://jekyllrb.com/docs/installation/#requirements)
- Code/Markdown Editor: [**VisualStudio Code**](https://code.visualstudio.com/download)
    - If you are familiar with another code and markdown editor, feel free to use it :)
- Command line tool: [**Terminal**](https://support.apple.com/en-ca/guide/terminal/welcome/mac) 
    - Terminal is macOS's command line tool that comes with every operating system
    - If you have never used Terminal before, refer to this [introductory video](https://www.youtube.com/watch?v=aKRYQsKR46I)
- Static site hosting service: [**GitHub Pages**](https://pages.github.com)
    - Refer to the [How to setup GitHub Pages](#how-to-setup-github-pages)
- Static site generator: [**Jekyll**](https://jekyllrb.com)
    - Refer to the [How to setup Jekyll](#how-to-setup-jekyll)
- Interface to interact with [**GitHub Desktop**](https://desktop.github.com)
    - We will need it to clone repositories from GitHub and pushing our changes to it
- [GitHub account](https://github.com) 
    - You would need to register a new account on GitHub, if you do not have one

### Side Notes
- If you are familiar with anything that you could use instead of what I used feel free to do so

## Instructions

### How to setup GitHub Pages
#### Register a GitHub account
1. Go to [GitHub](https://github.com)  
2. Navigate to the _Sign up_ button in the top right corner of the page  
3. Click on it and follow instructions  

#### Create a new **public** repository
1. Go to [this page](https://github.com/new)  
2. Enter a repository name  
    - You can name it resume, and change it later, refer to [FAQs](#faqs)  
3. Click _Create repository_  

#### Setup GitHub Pages  
1. Go to your repository  
2. Go to _Settings_  
3. Go to _Pages_  
4. select **main** branch under _Branch_    
5. Leave everything as it is  
    - _Deploy from branch_ under _Source_   
    - The box next to **main** as _/(root)_  
6. Click _Save_  

### How to setup Jekyll
- The main problem with installing Jekyll on macOS is associated with using the right ruby version. Thus, I will guide you through the process.
#### Install [Homebrew](https://brew.sh)
- Homebrew is the utility that will help you to install stuff that Apple did not
1. Open Terminal
2. Copy and Paste the following command into the Terminal:
    > `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
3. Press _Enter_ and wait until Homebrew is installed
    - This command will take some time to install Homebrew, so, don't panic and be patient

#### Install chruby [aka ch(ange) ruby]  
- As it can be implied from the name we will need **chruby** to change versions of the ruby we use. This is useful for different reasons, but we will need it mainly because macOS will not let you make changes to the ruby version it has installed :pensive:.   
1. Open Terminal  
2. Copy and Paste the following command into the Terminal:  
    > `brew install chruby ruby-install xz`  
3. Press _Enter_ and wait until chruby is installed  
  
#### Install Ruby
- Now we will install newest version of ruby  
1. Open Terminal  
2. Copy and Paste the following command into the Terminal:  
    > `ruby-install ruby`  
3. Press _Enter_ and wait until installation is complete  
  
#### Update your shell to use chruby
- Refer to [FAQs](#faqs) to learn which shell you are using  
1. Open Terminal  
2. Copy and Paste the following commands into the Terminal, one at a time:  
    - If you are using Z shell, run the following commands in the Terminal:  
    > `echo "source $(brew --prefix)/opt/chruby/share/chruby/chruby.sh" >> ~/.zshrc`  
    > `echo "source $(brew --prefix)/opt/chruby/share/chruby/auto.sh" >> ~/.zshrc`  
    > `echo "chruby ruby-3.1.2" >> ~/.zshrc`  
    - If you are using Bash, run the following commands in the Terminal:  
    > `echo "source $(brew --prefix)/opt/chruby/share/chruby/chruby.sh" >> ~/.bash_profile`  
    > `echo "source $(brew --prefix)/opt/chruby/share/chruby/auto.sh" >> ~/.bash_profile`  
    > `echo "chruby ruby-3.1.2" >> ~/.bash_profile`  
  
NOTES:  
- Replace **3.1.2** with the version of ruby that you installed  
3. Close and Open Terminal  

#### Change Ruby version used for our project
1. Navigate into the folder of the repository on your computer through the Terminal.  
    - If you named your repository as I suggested "resume", then you should be in the folder named "resume"  
2. Run the command below to check all of the versions of the ruby installed:    
    > `chruby`   
3. Run the following command to set project's ruby version to the newest one:  
    > `echo 'ruby-3.1.2' >> .ruby-version`  
    - Instead of "3.1.2" use the latest version returned by the command from step 2  
4. Check the ruby version by running the following command:
    > `ruby -v`  
    - The output should look like this:
    > `ruby 3.1.2p20 (2022-04-12 revision 4491bb740a) [x86_64-darwin20]`
    - Instead of "3.1.2" use the latest version returned by the command from step 2  

#### Install Jekyll
- Now we are ready to install Jekyll itself
1. Go to Terminal 
2. Run the following command:
    > `gem install jekyll`
3. Wait until the installation is finished


## Acknowledgments
  - [ankitsultana](https://github.com/ankitsultana/researcher) for the Resume template

## FAQs

### How do I rename the repository?
1. To rename a repository you can follow the steps described [here](https://docs.github.com/en/repositories/creating-and-managing-repositories/renaming-a-repository)  
  
### How do I know which shell I have?
1. Open Terminal  
2. Run the following:  
    > `something`  
3. Compare the output:  
    - You are using **Bash** if the output looks like this:  
    > `-bash: something: command not found`  
    - You are using **Z shell** if the output looks like this:  
    > `-zsh: something: command not found`  
