
#!bin/zshrc

sudo add-apt-repository ppa:neovim-ppa/unstable
sudo apt update
sudo apt install neovim
nvim --version

mkdir -p ~/.config/nvim
touch ~/.config/nvim/init.vim