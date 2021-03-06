#Installation:

    git clone git@github.com:chuchingkai/vimconfig.git ~/.vim

##Create symlinks:

    ln -s ~/.vim/vimrc ~/.vimrc

##Switch to the `~/.vim` directory, and fetch submodules:

    cd ~/.vim
    git submodule init
    git submodule update

##Install YouCompleteMe with Vundle

    Requirement:

    - tools and CMake: automake gcc gcc-c++ kernel-devel cmake
    - Python headers: python-devel python3-devel

    Compiling YCM with semantic support for C-family languages:

        cd ~/.vim/bundle/YouCompleteMe
        ./install.py --clang-completer

# Sync with your repo

    git pull origin master
    git submodule update --init --recursive

# Customize your plugin

##Add a submodule of plugin

    cd .vim/bundle
    git submodule add URL
    # not sure for this step:
    git submodule update --init --recursive -- bundle/path_to_it
    modify vimrc

##Remove a submodule of plugin

    rm from .gitmodules 
    rm from .git/config
    git add .gitmodules
    git rm --cached .vim/bundle/path_to_it
    git commit & push
    rm .vim/bundle/path_to_it
