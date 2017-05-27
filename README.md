# customize-terminal-mac

You need to have these two dot files in your HOME directory in order to customize your terminal

    .bashrc
    .bash_profile

To create these files, you need to use the 'touch' command.

    touch .bashrc
    touch .bash_profile
    
Open these files using subl command.To do that, you can open these files by typing:

    subl .bashrc
    subl .bash_profile

Don't worry if your subl command is not identified, you can paste the following in your terminal. You might have to change sublime text app according to the version that you have. 
      
    ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" ~/.rvm/bin/subl

You need to paste this code in your newly created files:

This is for .bash_profile
    
    #FIND BASHRC AND READ EVERYTHING FROM THERE
    if [ -f ~/.bashrc ]; then
        source ~/.bashrc
    fi
    
This is for .bashrc

    echo 'Welcome Karan!'

    #Defining some aliases

    # Easier navigation: .., ..., ...., ....., ~ and -
    alias ..="cd .."
    alias ...="cd ../.."
    alias ....="cd ../../.."
    alias .....="cd ../../../.."
    alias ~="cd ~"
    alias -- -="cd -"

    alias downloads="cd ~/Downloads"
    alias desktop="cd ~/Desktop"
    alias fall16="cd ~/Google\ Drive/NYU/Fall\ 2016/"
    alias spring17="cd ~/Google\ Drive/NYU/Spring\ 2017/"
    alias fall17="cd ~/Google\ Drive/NYU/Fall\ 2017/"
    alias j="jobs"
    alias h="history"

    #Show and hide hidden files
    alias showFiles='defaults write com.apple.finder AppleShowAllFiles YES; killall Finder'
    alias hideFiles='defaults write com.apple.finder AppleShowAllFiles NO; killall Finder'

    #

    #Customizing Mac Terminal Starts
    #http://tldp.org/HOWTO/Bash-Prompt-HOWTO/bash-prompt-escape-sequences.html

    #defining colors
    green=$(tput setaf 46);
    yellow=$(tput setaf 226);
    orange=$(tput setaf 203);

    PS1="\[${green}\]\u";       #username
    PS1+="\[${yellow}\]@\h";    #host
    PS1+="\[${orange}\]:\W"     #Working directory
    PS1+="\[$(tput sgr0)\] \n> "
    export PS1;

    #Adding Path Variables
    #Spark Path
    export PATH=/usr/local/scala/bin:/usr/local/spark/bin:$PATH
    #Anaconda Path
    export PATH=/Users/kchak/anaconda/bin:$PATH
    #Python path
    export PATH=/Library/Frameworks/Python.framework/Versions/3.6/bin:$PATH
    export PATH


After you have pasted this in your files, and saved them, you can go ahead and restart the terminal or you can just write the command

    source .bashrc
    
You are good to go! 
