# customize-terminal-mac

Reference: https://github.com/ohmybash/oh-my-bash

You need to have these two dot files in your HOME directory in order to customize your terminal

    .bashrc
    .bash_profile

To create these files, you need to use the 'touch' command.

    touch .bashrc
    touch .bash_profile
    
Open these files. You need to paste this code in your newly created files:

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
    #Python path
    export PATH=/Library/Frameworks/Python.framework/Versions/3.6/bin:$PATH
    export PATH


After you have pasted this in your files, and saved them, you can go ahead and restart the terminal or you can just write the command

    source ~/.bashrc
    
You are good to go! 
