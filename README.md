# TRISEP_2025_ssh_config

This repo stores the ssh configuration files for all the TRISEP students.
Download 'your' file and copy it to the home direcotry on your laptop. 

Note: If you put your keys in non-default locations you might need to edit the ```IdentityFile``` fields in the config - pointing to the correct location. The file supplied assumes you have used the defaults.

If a file .ssh/config already exists append the contents of the fle you just downladed to the existing .ssh/config file. If .ssh/config does not exist - you can copy over the new file to .ssh/config.

On linux, mac, WSL something like this should work in both cases:

```cat config_<your_user_id> | tee -a .ssh/config >& /dev/null```

***Restart your terminal.***

Now you should be able to log in by typing:

```ssh ML-TRISEP```

or

```ssh ML-TRISEP-CONTAINER```

The second option is recommended by default. It will automatically launch an apptainer container with all the software you will need bundled in. Also if you are used to using [vscode](https://code.visualstudio.com/) you can install The [Remote SSH extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh) and launch a remte conection to ```ML-TRISEP-CONTAINER```. This will allow you to edit and run in vscode while using the container - with vscode understanding all the code dependencies, autocompletes etc.

