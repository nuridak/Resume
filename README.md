# How to host a resume on GitHub Pages.

### [Demo Website](http://nuridak.github.io/)  
![This is resume demo Gif](https://github.com/nuridak/nuridak.github.io/blob/main/src/editYml.gif)

## Purpose

This is a quick tutorial to teach you how to host and format your resume as a static website using Markdown, GiHub Pages and Jekyll. Also, I will demonstrate some principles of Andrew Etter's book _Modern Technical Writing_.

## Getting Started

### Prerequisites 
- This tutorial does **not** cover:  
    - How to write a resume  
        - you will need a ready to use resume formatted in Markdown (_resume.md_)
        - you can use the [index.md](https://github.com/nuridak/nuridak.github.io/blob/main/index.md) as a reference 
    - How to use Markdown  
        - you can refer to the tutorials from the [More Resources](#more-resources) section 

For this tutorial I used: 
- Operating System: [**macOS Big Sur**](https://apps.apple.com/us/app/macos-big-sur/id1526878132?mt=12)
    - Jekyll also supports Monterey and Catalina, but older versions are not supported, so, they might/might not work
- Code/Markdown Editor: [**VisualStudio Code**](https://code.visualstudio.com/download)
    - If you are familiar with another code and markdown editor, feel free to use it :smile:
- Command line tool: [**Terminal**](https://support.apple.com/en-ca/guide/terminal/welcome/mac) 
    - Terminal is macOS's command line tool that comes with every operating system
    - If you have never used Terminal before, refer to this [introductory video](https://www.youtube.com/watch?v=aKRYQsKR46I)
- Interface to interact with GitHub: [**GitHub Desktop**](https://desktop.github.com)
    - We will need it to clone repositories from GitHub and pushing our changes to it

## Instructions

### How to setup Jekyll

- [**Jekyll**](https://jekyllrb.com) is a static site generator
    - For installing Jekyll on operating systems other than macOS refer to [this page](https://jekyllrb.com/docs/installation/#requirements)
    - The main problem with installing Jekyll on macOS is associated with using the right ruby version. Thus, I will guide you through the process.
    - Even though you can create static sites from scratch by yourself, generators like Jekyll make this work much easier, you just have to install it properly. :grinning: I chose to work with Jekyll because, as Andrew Etter said, Jekyll is the most popular static site generator meaning there are much more resources available. 

#### Install Jekyll
1. Follow instructions from the [jekyllSetup.md](https://github.com/nuridak/nuridak.github.io/blob/main/extra/jekyllSetup.md) file to install Jekyll

### How to setup GitHub Pages  
- [**GitHub Pages**](https://pages.github.com) is a static site hosting service. 
    - Andrew Etter mentions GitHub Desktop as one of the interface options for the version control. The terminal is always available for use, however many people still prefer to use version control for basic commands and GUI makes workflow much more convenient to use. Andrew argues that version control allows for easier and more convenient contribution and distribution. For example, right now you will learn how to use version control to clone repository of another person, make changes to it, and push those changes to your own repository.

#### Register a [GitHub account](https://github.com) 
1. Go to [GitHub](https://github.com)  
2. Navigate to the **Sign up** button in the top right corner of the page  
3. Click on it and follow instructions  

#### Create a new **public** repository
1. Go to [this page](https://github.com/new)  
2. Enter a repository name as **_yourusername.github.io_**
    - to how to change it later, refer to [FAQs](#faqs)  
3. Click **Create repository** 

#### Setup GitHub Pages  
1. Go to **_yourusername.github.io_**  
2. Go to **Settings**  
3. Go to **Pages**  
4. select **main** branch under _Branch_    
5. Leave everything as it is  
    - _Deploy from branch_ under _Source_   
    - The box next to **main** as _/(root)_  
6. Click **Save** 

#### Setup the repository with files
1. Go to **_yourusername.github.io_**  
2. Copy the link: 
![This is copy demo Gif](https://github.com/nuridak/nuridak.github.io/blob/main/src/copyLink.gif)
3. Open the GitHub Desktop
4. Clone repository by pasting the link that we have copied:
![This is clone demo Gif](https://github.com/nuridak/nuridak.github.io/blob/main/src/cloneRepo.gif)
5. Download files from [this](https://github.com/nuridak/nuridak.github.io) repository into the created **_yourusername.github.io_** folder on your computer  

#### Edit and format resume
1. Copy content of your **_resume.md_** file
2. Replace everything inside of the **_index.md_** with copied content
3. Edit **_'_config.yml_** :
![This is format demo Gif](https://github.com/nuridak/nuridak.github.io/blob/main/src/editYml.gif)
4. Replace **resume.pdf** with your pdf version of the resume
5. (SUGGESTED) Edit **README.md** as you wish
6. (SUGGESTED) Delete **src** and **extra** folders

#### Push your changes to the repository
1. Follow the steps shown below:
![This is push demo Gif](https://github.com/nuridak/nuridak.github.io/blob/main/src/editYml.gif)

#### View your website :sparkles:
1. Open browser
2. Go to the **_https://yourusername.github.io_**  
3. Enjoy your own static website :tada:

## More Resources

- [Interactive markdown tutorial 1](https://www.markdowntutorial.com)  
- [Video markdown tutorial](https://www.youtube.com/watch?v=HUBNt18RFbo)  
- [Career Services: Resume Workbook](https://umanitoba.ca/student/careerservices/media/Resume.pdf)  
- [Andrew Etter's _Modern Technical Writing_](https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS 

## Authors and Acknowledgments

#### Resume template provided by
- [ankitsultana](https://github.com/ankitsultana/researcher)

#### Reviewed by
- AL Fahiyan Siyam - [alahiyansiyam](https://github.com/AlFahiyanSiyam)
- Felix Wedel - [WedelFelix](https://github.com/WedelFelix)
- Gurman Toor - [GurmanToor](https://github.com/GurmanToor)

#### Principles from Andrew Etter's Book
- [_Modern Technical Writing_](https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS)

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

### Why is Markdown better than a word processor?
- Andrew Etter says that Markdown is better than a word processor because of the reasons like:
    1. Markdown is much more human-readable, while word processor much more challenging 
    2. Markdown is pretty straightforward to learn, while word processor requires a knowledge of a lot of tags
    3. Markdown takes much less "text" space compared to a word processor
