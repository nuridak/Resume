# How to Setup Jekyll on macOS  

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
    - NOTES:  
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

