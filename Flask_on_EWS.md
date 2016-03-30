# Setting up a Flask Environment on EWS Machines
## Connecting to EWS
### Windows
1. Install `PuTTY` from [this download page](http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html). You only need to get `putty.exe`.
2. Open `PuTTY` and in the `hostname` box, enter `YOUR_NET_ID@linux.ews.illinois.edu`
3. Optionally, add a name in Saved Sessions like "UIUC AWS" and click save to save this URL for future sessions.
4. Click `Open` and enter your Active Directory password when prompted.
### Mac
1. Open the `Terminal` application by finding it in `Applications/Utilities/Terminal` or by doing `Command-Space` and typing in `Terminal`.
2. Execute the following command: `ssh YOUR_NET_ID@linux.ews.illinois.edu`
3. Enter your Active Directory password when prompted.

## Setting up a Flask Virtual Environment
1. Once you've opened up an SSH session using the instructions above, issue the following commands:
```
module load python/2.7.10
virtualenv ~/python_env
```
2. This will create a folder called `python_env` in your home directory. Now do `cd ~/python_env` to enter that folder.
3. Run the following commands to update your pip installer and install the Flask modules.
```
pip install --upgrade pip
pip install Flask
``` 
4. Now you can install any other packages you may need (for example, `Flask-API`) by running `pip install PACKAGE_NAME`.
## Using the Virtual Environment
1. When you SSH into the EWS machine, run `source ~/python_env/bin/activate` to activate your Python environment.
2. To exit the Virtual Environment and get back to the 'normal' EWS environment, simply run `deactivate`