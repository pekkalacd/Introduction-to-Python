# How to Contribute<br><br>

### 1. Fork the Repository<br>
When you fork this repository, a *copy* of this repository will show up on your github account. Changes made to that copy are not persistent to the this repository.
Additional actions need to be taken by collaborators in order to make changes to the existing content.<br>

To fork this repository, in the upper right-hand corner of the screen there should be a button labeled **Fork**, click that.<br>

<p align="center"><img src = "https://user-images.githubusercontent.com/34849400/104872204-d6070600-5912-11eb-89d5-41b2b634e00b.png"/></p>
<br>
A display window will pop up with a set of destinations to fork the repository to. You want to select the tag with your username. 
<br><br>
<p align="center"><img src = "https://user-images.githubusercontent.com/34849400/104871977-2df13d00-5912-11eb-9ce8-83fe773cf45f.png"/></p>

Doing so will send a copy of the repository to your **overview page**. 

<br><br><br>

### 2. Clone the Repository<br>

On your overview page, inside of your forked copy of this repository, navigate to a link called **"Code"**.

<br>
<p align="center"><img src = "https://user-images.githubusercontent.com/34849400/104873207-98f04300-5915-11eb-99c9-43f15a458568.png"/></p>
<br>

Navigate to git bash terminal and make a directory and change directories into it:<br><br>

                                 mkdir someFolder && cd someFolder
<br>

This directory will be used to store a **clone** or copy of this repository on your local machine. You can clone with the following command:<br><br>

                                 git clone https://github.com/pekkalacd/Introduction-to-Python.git
<br>

Then you'll want to change directories into the repository:<br><br>

                                 cd "Introduction to Python"

<br><br><br>

### 3. Create a Branch<br> 

Once the repository has been cloned on your machine, you'll want to create a **branch**. You can do so by typing the following command on your bash:<br><br>

                                git checkout -b <branch_name>
                                
<br><br>

Your branch name will vary to whatever you'd like to call it. This is done to ensure that the changes being made to the cloned repository are isolated to that specific branch.
<br><br><br>
<br><br><br>

### 4. Find, change, and save the files you would like to change.<br>

Go into the local directory storing the cloned repository and navigate to the files you'd like to change. Make changes to those files as you see fit. When you're finished making
changes, save the files.<br>

After the files have been saved, add the changes to the existing branch by typing the following command:<br><br>

                               git add -A
<br>

Running this command will add the newly modified files onto the branch. You can check that these file were added by running:<br><br>

                               git status

<br>This will highlight the modified files that were successfully added onto the branch in green.<br>

<br>

Finally, you can then run the following command to *commit* the changes.<br>

                               git commit -m "fixing some thing"
                               
<br>

The -m flag denotes a message, followed by string containing the message.

<br><br><br>

### 5. Push your branch back to your forked repository<br>

Now that the changes have been made, you'll want to **push** this branch back to the forked repository on github (available at your Overview). You can do this by running the
following command:<br><br>

                              git push origin <branch_name>
                              
<br>

Once that command has been completed, refresh the link at the forked repository, and you should see that there has been a branch added to that repository.<br><br>

<p align="center"><img src="https://user-images.githubusercontent.com/34849400/104877433-6d725600-591f-11eb-8d7f-2a8ed4f97945.png"/></p>

<br><br><br>

### 6. Pull Request<br>

You'll want to click on **Compare & Pull Request**. This will populate the changes being proposed by the branch you just pushed to the original repository that your forked from.<br>
<br>Here you will additionally enter a title for the changes you've made and provide a brief description for what those changes were, then you'll hit **Create Pull Request**.

<p align="center"><img src="https://user-images.githubusercontent.com/34849400/104877729-1456f200-5920-11eb-9b2e-b09642053963.png"/></p>

<br>

This will populate a **Pull Request** inside of *Pull requests* tab of this repository. A collaborator will then assist with merging your proposed changes on the branch you
created with the main branch used for this repository.

<br><br><br>

<p align="center"><img src="https://user-images.githubusercontent.com/34849400/104878675-fbe7d700-5921-11eb-9c51-5f032a273f18.png"/></p>

<br>














