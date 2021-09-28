# Jupyter Notebook Setup and Launch

[![Practicum AI Logo](images/PracticumAI_Logo.jpg)](https://practicumai.org)

## Setup

> If working off-campus, you must first login via Cisco VPN.  If on-campus, use a wired connection or the "eduroam" wireless network.  Do not use the "ufguest" network.

1. Open a browser and go to: [https://ood.rc.ufl.edu](https://ood.rc.ufl.edu/pun/sys/dashboard)
(Probably good to bookmark this site as we'll use it a lot)

1. From the **Clusters** menu, select **"_Hipergator Shell Access"** 
   > Alternatively, these steps can be done within a JupyterLab session. A terminal process is available in the Other section of the Launcher tab, at the bottom of the list of available kernels.

1. At the Unix prompt, please type the following series of commands and hit enter after each one.
   > One convention we will use is to put values that need to be changed by the user within angled brackets ("<>"). Do not include the brackets with the replacement text. e.g. `mkdir <GatorLink>` becomes `mkdir albert` for the user with the GatorLink "albert".

   1. Change directories to `/blue/rc-workshops`: `cd /blue/rc-workshops`
   1. If your primary group is not "rc-workshops": Create a directory named with your GatorLink: `mkdir <GatorLink>`
      > If your account was created for the workshop, your primary group is rc-workshops and you can skip this step as the directory already exists.
   1. Change directories into this directory: `cd <GatorLink>`
   1. Copy the Practicum AI notebooks and folders to your directory: `cp -r /data/training/workshops .`
      > The `-r` says to copy *recursively*--including folders)

      > **Note the period** at the end to tell Linux to copy the files "here"--a single dot is Linux shorthand for the current directory.
   1. Return to your home directory: `cd`
      > `cd` with no options goes to your home
   1. Create a symbolic link to the `/blue/rc-workshops` directory: `ln -s /blue/rc-workshops <LinkName>` For `<LinkName>`, we recommend using `blue_rc-workshops`.

1. Type `exit` and hit enter to leave the shell.

## JupyterLab Launch Instructions

> If working off-campus, you must first login via Cisco VPN.  If on-campus, use a wired connection or the "eduroam" wireless network.  Do not use the "ufguest" network.

1. Open a browser and go to: [https://ood.rc.ufl.edu](https://ood.rc.ufl.edu/pun/sys/dashboard)
(Probably good to bookmark this site as we'll use it a lot)

1. From the Interactive Apps menu, select "Jupyter Notebook"

1. Enter the values below in the indicated fields on the form, other values can generally be left alone:
   1. Ensure that the JupyterLab checkbox is checked – otherwise, an older, less feature rich environment is run
   ![Screenshot showing the JupyterLab checkbox](images/JupyterLab_checkbox.png)
   1. **Maximum memory requested for this job in Gigabytes:** 5
      > Note: Larger dataset may need more memory.
   1. **SLURM Account:** rc-workshops
   1. **QoS:** rc-workshops
   1. **Cluster partition:** gpu
   1. **Generic Resource Request:** gpu:1
1. After filling out the form, click the launch button near the bottom of the page.
![Screenshot of the Launch button](images/Launch_button.png)
   > Clicking Launch submits the job to the SLURM Scheduler, requesting the resources you have asked for. The scheduler will now look for a place to run your job, or sometimes gives an error message. A common error is asking for too many resources (more than your group has access to).
1. While your job is in the queue, you will see the message "Please be patient as your job currently sits in queue. The wait time depends on the number of cores as well as time requested."  Once it is Running, click **Connect to Jupyter**
![Screenshot of the Connection card, showing the connect to Jupyter button](images/Connection_card.png)

1. JupyterLab will then launch in a new tab

