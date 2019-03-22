# PythonBootstrap
This is the repository to be used by those interested in boot strapping their environment to run their own personal projects


# Environment Setup
1. Join GitHub
   > http://github.com/
2. Install Slack
   > https://slack.com/get-started
3. Join NIA Slack Organization
   > https://nia-org.slack.com
4. Install Python 3.7.2 (Check off "Add Python 3.7 to PATH")
   > https://www.python.org/downloads/release/python-372/
5. Install Git Bash:
   > https://git-scm.com/downloads
6. Open Git Bash and navigate to home directory to create .bashrc file
   > ```touch ~/.bashrc```

   > Add the following code to the bashrc file
   ```bash
   # Enable calling python executable
   alias python='winpty python.exe'
   # Setup proxy
   PROXY_OPT=--proxy=--proxy=http://...
   # Enable building environment through command
   alias buildenv='source $(git rev-parse --show-toplevel)/tools/build_env.sh'
   alias cleanenv='$(git rev-parse --show-toplevel)/tools/clean_env.sh'
   alias setproxy='PROXY_OPT=--proxy=http://...'
   alias clrproxy='PROXY_OPT='
   ```

7. Exit Git Bash and re-open it or run "source ~/.bashrc" to make the new commands available for execution while in git bash. The commands are to be used as follows:
   > **buildenv** - Used to create the python virtual environment and install all dependencies

   > **cleanenv** - Used to remove virtual environment build folder and exit environment if it's active

8. Clone repository:
   > ``https://github.com/NIAGroup/PythonBootstrap```

9. Enable git flow:
   ```bash
   cd <repo_path>
   git flow init
   ```
10. Clone this repository
