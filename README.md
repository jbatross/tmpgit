# My Project
This repository is for INFO 550 and the final project. </br>
The dataset is based on mosquio data and West Nile Virus incidence in California by County over a 10 year period. </br>
The packages necessary for this analysis is as can be done by running the following `R` code </br>
```{r}
list.of.packages <- c(
  "dplyr",
  "sf",
  "table1",
  "tmap"
)
new.packages <- list.of.packages[!(list.of.packages %in% installed.packages()[,"Package"])]
if(length(new.packages)) install.packages(new.packages)
invisible(lapply(list.of.packages,library,character.only=T))
rm(list.of.packages,new.packages) #Removes lists for cleanliness
```
# Exectue Analysis
### Using Docker(Recommended)
1) Download and save all files to your local directory (Doesn't need to be specific) 
2) In `Terminal`, navigate to the local directory 
3) Pull the image from my DockerHub repository by running the following code

```bash
   docker pull jbatross97/info-550:latest
 ```
  
4) Mount your local directory to the directory in the container by running the following code
 
 ```bash
    docker run -v /local_directory_path:/project jbatross97/info-550:latest
 ```
 Add your local directory path that has the clone of this repository. 
 This will create a file called `report.html` output in your local working directory.
### Using MAKE(Not recommended)
To execute the analysis using MAKE, from the project folder you can run: </br>
``` bash
    make report.html
```
      
This command will create a report.html which can be manipulated further using `R`. </br>

**WARNING: When creating report, the terminal will hang for a minute or so to create the map**
     

 
