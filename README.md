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

    #defining colors
    green=$(tput setaf 46);
    yellow=$(tput setaf 226);
    orange=$(tput setaf 203);

    PS1="\[${green}\]\u";       #username
    PS1+="\[${yellow}\]@\h";    #host
    PS1+="\[${orange}\]:\W"     #Working directory
    PS1+="\[$(tput sgr0)\] \n> "
    export PS1;

    #You can have your PATH variables put here
    export PATH

After you have pasted this in your files, and saved them, you can go ahead and restart the terminal or you can just write the command

    source .bashrc
    
You are good to go! 
