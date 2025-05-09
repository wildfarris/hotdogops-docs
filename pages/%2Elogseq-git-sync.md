- ```bash
  # check if current credential.helper is osxkeychain
  git config credential.helper
  # osxkeychain
  
  # clear osxkeychain password
  git credential-osxkeychain erase
  
  # install latest git and git credential manager (GCM) from homebrew
  brew install git
  brew tap microsoft/git
  brew install --cask git-credential-manager-core
  
  # verify cask installation has automatically updated the credential.helper
  git config credential.helper
  #/usr/local/share/gcm-core/git-credential-manager-core
  
  # attempt to git push, will bring up a pop-up establishing authentication
  git push
  ```