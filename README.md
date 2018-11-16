**Ghaidaa kashgari-EE282** 
_HOMEOWRK2_
gkashgar@uci.edu

## Q1-Alex has joined the data analysis team for RNA-sequencing project replacing jake. Please make a folder with Alex’s name in the project accessible directory “RNA282” and discard Jake’s old data. 
* cd RNA282 
* mkdir Alex 
* rmdir Jake 
### Question 1 Comments: you are correct in how to create a directory, but rmdir Jake, will only remove the Jake folder if there is nothing inside the folder. if you wanted to remove the folder and the contents inside of the jake folder then you would have needed to perfrom a recursive rm i.e. rm -rf Jake where -f means force, and do not show prompts for confirming of deleting each file. 

## Q2-I have four new team members for the project (hm2820). I need you to create a data frame with their Names and Age. Next, provide me with a list of their Ages (without showing names of each member). 
hm282 <- data.frame("Age" = c(21,35,29,18), "Name" = c("John", "Sara", "Jake", "Alex"), stringsAsFactors = FALSE)
* summary(hm282) 
* hm282[1]
* data.matrix(hm282[1])

### Question 2 Comments:

You created a dataframe and demonstrated how to access using just the **df[_number_]** method. But you didn't use the other methods: **df[[_number_]]**, **df[,_number_]**, and **matrix[,_number_]**. Give it another shot? Also, your description of the "key" wasn't very descriptive.

## Q3-I would like you to make a new shared directory for the new DNA-sequencing project and allow the new members to access our project’s shared directory and files in the directory.  Allow them to add any data analysis they have completed, but make sure they cannot delete or remove any file from the project directory. 

```
sudo mkdir DNA/projects/Shared
sudo addgroup newgroup
sudo chown :newgroup DNA/projects/Shared
sudo usermod -aG newgroup Alex
sudo chmod 770 DNA/projects/Shared
```

### Question 3 Commments:
in this case you would only need to use sudo for adding a group as only system administrators can create groups and users.
Also, it looks like DNA is a group? and a folder? I had a hard time following what you were doing here. Could you please correct what you did here so that the persmissions being set follow what you had requested. Also, please note that when you precede any directory with the "/" character you are telling the system to start at the root directory. i.e. "/". Only system administrators can change the root directory. I did at first assume that the working directory was /projects, but then you also did /DNA/Shared. I wasn't sure if this was supposed to be another folder or a folder inside projects? or a group? Please let me know when you have fixed this, so that I can finish grading Question 3 for you. Thank you. :) Also, please feel free to ask questions about this problem if you need help with anything.
