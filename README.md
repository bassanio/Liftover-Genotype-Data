# Liftover-Genotype-Data
This page describes one method to update/liftover genotyping data. This method uses tools like [plink](https://www.cog-genomics.org/plink/) and update information from [Strand](https://www.well.ox.ac.uk/~wrayner/strand/index.html). The following methods will help in liftover genotyping chip based on Grch37 (H3Africa_2017_20021485_A3) to Grch38.  

Identify the Chip and strand orientation using the online [Chipendium](http://mccarthy.well.ox.ac.uk/chipendium/ui/) and downnload the strand and position files accordingly.

# Method

## Step 1: Download and unzip the required strand and position files
Files required for the analysis

```
wget -c https://www.well.ox.ac.uk/~wrayner/strand/H3Africa_2017_20021485_A3-b38-strand.zip
wget -c https://www.well.ox.ac.uk/~wrayner/strand/update_build.sh .
unzip H3Africa_2017_20021485_A3-b38-strand.zip
```

 ## Step 2: Run the Update.sh
 This shell script contains the plink and associated commands to update the positions to Grch38. Update the path to plink binary accordingly.
 ```
 sh update_build.sh ALL H3Africa_2017_20021485_A3-b38.strand Updated
 ```
