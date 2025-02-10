# 1. Check Your Current Python Version
```
python3 --version
```

# 2. Install Homebrew (if not already installed)

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
# 3. Update Homebrew

```
brew update
```

# 4. Install the Latest Python Version

```
brew install python@3.12
```
# 5. Adjust Your PATH Environment Variable
To make sure your system uses the newly installed Python version by default, you need to adjust your PATH environment variable. 

## Edit Your Shell Configuration File
Depending on the shell you're using (likely zsh or bas), you'll need to edit ~/.zshrc or ~/.bash_profile

### For Z Shell

```zshell
nano ~/.zshrc
```

### For Bash
```
nano ~/.bash_profile
```

## Add Homebrew's Python to Your PATH
Add the following line at the top of the file:

```zshell
export PATH="/opt/homebrew/bin:$PATH"
```

For Intel-based Macs, use /usr/local/bin instead of /opt/homebrew/bin

Save and exit

## Reload your Shell Configuration
Apply the changes immediatel by running

```zshell
source ~./zshrc
```

```bash
source ~./bash_profile
```

# 6. Verify Installation
Check that python3 now points to the latest version:

```
python3 --version
```

Expected Output

```
Python 3.12.0
```

# 7. Check the Python Executable Path
Ensure that the ptyhon3 command is pointing to the correct executable:

```
which python3
```

Expected Output
```
/opt/homebrew/bin/python3
```

# 8. Handling Multiple Python Versions

If you have multiple Python versions installed, you might want to manage them without uninstall older versions.

## Use Python Version Managers
Consider using a Python version manager like *pyenv* to switch between different Python versions easily.

### Install pyenv via Homebrew:

```
brew install pyenv
```
### Install Python 3.12 Using pyenv

```
pyenv install 3.12.0
```

### Set Global Python Version:

```
pyenv global 3.12.0
```
# 9. Make your shell run pyenv

```
if command -v pyenv 1>/dev/null 2>&1; then
  eval "$(pyenv init -)"
fi
```
