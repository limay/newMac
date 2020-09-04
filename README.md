# newMac

# Install brew / brew cask

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
brew upgrade
brew update
brew tap homebrew/cask

# ssh

ssh-keygen -t rsa -b 4096 -C "$useremail"
ssh-agent -s
ssh-add -K ~/.ssh/id_rsa

nano ~/.ssh/config

add
Host *
 AddKeysToAgent yes
 UseKeychain yes
 IdentityFile ~/.ssh/id_rsa
 
# Add signature to Github
pbcopy < ~/.ssh/id_rsa.pub

# Install Rectangle
brew cask install rectangle

# Install Iterm 2
brew cask install iterm2

Follow this gist: https://gist.github.com/kevin-smets/8568070

# Install Docker
brew cask install docker

# Programming fonts

brew tap homebrew/cask-fonts

### programming fonts
brew install svn //For the fonts
brew cask install font-fira-mono-for-powerline
brew cask install font-fira-code

# Others

brew install python
brew install git
brew install trash
brew cask install notion
brew cask install slack
brew cask install vlc
