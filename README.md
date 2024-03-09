# dev-env
Development environment for python data analysis. The development stack is 
- Github for version control
- VS Code for IDE (interactive development environment) with most data exploration through notebooks
- PDM as virtual environment manager
- duckdb for managing data for standalone projects 

## Initial setup
I use homebrew for the initial setup to provide access to different python versions and install software pacakages.

Run the following in the terminal. You may need to install XCode as well (to check)

1. Install homebrew as https://brew.sh/ instructions
`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"` 
2. With brew installed you can add the python versions you want, you can add to these or remove them at any time 
```bash
brew install python@3.9
brew install python@3.10
brew install python@3.11
brew install python@3.12
```
3. We will use PDM to manage virtual environments all take care of package compatability `brew install pdm`
4. Github for versioning `brew install --cask github`
5. VS Code `brew install --cask visual-studio-code` 

## Setting up a new environemnt in VS Code 
Within VS Code bottom panel you will see a terminal option, the defauly language is zsh, for the below add a new session with bash. Running this command will setup a new virtual environment with pdm, you'll be asked questions on the base python version and other aspects. You should see the various python@3.xx version you installed earlier

`pdm init` 

If you're running a notebook with an existing environment the command is `pdm install` this will find the toml file and install the listed packages. 

## Other helpers (TODO)
- Set up a hidden .env file with your various passwords for connections so you never accidentally commit those to the cloud
- Add dbeaver for database GUI `brew install --cask dbeaver-community` or the pro version `brew install --cask dbeaver-enterprise` or work within VS Code
- Add extensions for VS Code (Git graph, Tabnine or Co-pilot for code assistance, AWS Tookit, Excel viewer, ident-rainbow) 
