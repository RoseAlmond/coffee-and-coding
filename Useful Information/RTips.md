## How To Generate an Encyrpted Password and update the .RProfile

1. go to http://art-p-01/artifactory/webapp/#/login, in the top right corner click on your user name, retype your password and then next to Encrypted password click the button that looks like a set of paper, this copies the encrypted password. 

2. go to your .Rprofile in D:/R/lib and delete hashedpassword and paste in the encrpyted password. 

3. Replace username with your windows login 

4. save


## Old Version of Instructions 

To get R to install from the server do the following. If you use R Studio you need to do steps 3, 4 and 5 for RStudio as well 


## How to get R to install packages

### To get R to install from the server do the following.

1. On your D drive create a folder called R, and inside the R folder create a folder called lib, and open that folder.

2. On the R_foundation drive (\\nsdata3\R_foundation) there is a file called .Rprofile, copy that into D:\R\lib. (There us a copy in the Files Tab on here) remember to save it as .Rprofe, if it doesn't have the dot open in notepad when save change type to allfiles. 

3. In your start menu locate R and then right click and then click Pin to start menu.

4. Open your start menu and right click on R, then click properties.

5. Where it says start in, delete the contents and replace with D:\R\lib and click apply.

6. go to http://art-p-01/artifactory/webapp/#/login, in the top right corner click on your user name, retype your password and then next to Encrypted password click the Eye Button and copy the contents.

7. Now open the .Rprofile in notepad and replace username with your username and hashedPassword with what you copied from the artefactory and save.

8. Open R from the start menu, and you will see the message "If you are seeing this you can Install from the ONS repository"

9. Now install the package.


### To get R to install a specific version of a package, (mainly when you are getting a 404 error) do the following:

1. Go to http://art-p-01/artifactory/vr-R/bin/windows/contrib/3.4/

2. Search for the package you are looking for (say dplyr)

3. find the version number (0.7.4 n this case)

4. then back in R/Rstudio run the following code

5. install.packages("http://username:hashedPassword@ art-p-01/artifactory/vr-R/bin/windows/contrib/3.4/dplyr_0.7.4.zip", repos=NULL)
