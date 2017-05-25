# customize-terminal-mac
Two files to customieze your mac terminal

This repo contains two files. 
1. bashrc
2. bash_profile

These two are text files, but in order to customize your terminal, you need to create dot files in your HOME directory if they do not already exist. 

To create these files, you need to use the 'touch' command.

    touch .bashrc
    touch .bash_profile
    
The contents of these, bashrc and bash_profile, text files need to be put in your newly created files. 
To do that, you can open these files by typing

    subl .bashrc
    subl .bash_profile
    
After you have pasted this in your files, and saved them, you can go ahead and restart the terminal or you can just write the command

    source .bashrc
    
You are good to go! 
