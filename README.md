# csv-to-json-converter-wine-dataset
A shell script that converts a csv file to a json file

__Tested in Windows__   
-----

# INSTRUCTIONS: 
1. Firstly, git bash into your folder where you have kept the .sh files.  
2. copy the csv file (wine.csv) into the folder (csv-to-json-converter_manufac) with permod.sh and csvtojson.sh files  
3. execute the permod.sh file in the Git Bash terminal with "bash permod.sh"  
4. execute the csvtojson.sh file in the Git Bash terminal with "bash ./csvtojson.sh wine.csv > wine.json"  

****

# Basic documentation of the work:
1. First I downloaded the dataset from [Wine Data Set](https://archive.ics.uci.edu/ml/datasets/wine) . Next, I changed the extension of wine.data from .data to .csv. Then I put in the file headers i.e. the attributes, in the wine.csv file.
2. Next, for converting to JSON file:
- permod.sh : Its code makes the csvtojson.sh executable .
- csvtojson.sh : It reads the csv files line by line and takes the table headers as the keys of the objects in the json array 'data' and the data of the table as the value of each set of keys.
<br>
Example: Suppose in line 2 of the csv file (since line 1 of the csv file contains the table headers) there are: 
<br>
1,14.23,1.71,2.43,15.6,127,2.8,3.06,0.28,2.29,5.64,1.04,3.92,1065
<br>
<br>
So while converting to json, it will appear almost like this : 
<br>
{
    <br>
"data":
<br>
[
    <br>
{"typee":"1",
<br>"alcohol":"14.23",
<br>"malic_acid":"1.71",
<br>"ash":"2.43",
<br>"alcalinity_of_ash":"15.6",
<br>"magnesium":"127",
<br>"total_phenols":"2.8",
<br>"flavanoids":"3.06",
<br>"nonflavanoid_phenols":"0.28",
<br>"proanthocyanins":"2.29",
<br>"color_intensity":"5.64",
<br>"hue":"1.04",
<br>"OD280/OD315_of_diluted wines":"3.92",<br>"proline":"1065"},
<br>
...............
<br>
]
}