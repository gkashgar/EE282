**Ghaidaa kashgari-EE282** 
_HOMEOWRK2_
gkashgar@uci.edu

## Q1-Alex has joined the data analysis team for RNA-sequencing project replacing jake. Please make a folder with Alex’s name in the project accessible directory “RNA282” and discard Jake’s old data. 
* cd RNA282 
* mkdir Alex 
* rmdir Jake 

## Q2-I have four new team members for the project (hm2820). I need you to create a data frame with their Names and Age. Next, provide me with a list of their Ages (without showing names of each member). 
hm282 <- data.frame("Age" = c(21,35,29,18), "Name" = c("John", "Sara", "Jake", "Alex"), stringsAsFactors = FALSE)
* summary(hm282) 
* hm282[1]
* data.matrix(hm282[1])

## Q3-I would like you to make a new shared directory for the new DNA-sequencing project and allow the new members to access our project’s shared directory and files in the directory.  Allow them to add any data analysis they have completed, but make sure they cannot delete or remove any file from the project directory. 
* sudo mkdir /projects/Shared
* sudo addgroup newgroup
* sudo chown :DNA /projects/Shared
  * sudo adduser Alex DNA
  * sudo chmod 1770 /DNA/Shared
