# Update a file through a Python algorithm
## Project description

At my organization, access to restricted content is controlled with an allow list of IP addresses. The "allow_list.txt" file identifies these IP addresses. A separate remove list identifies IP addresses that should no longer have access to this content. I created an algorithm to automate updating the "allow_list.txt" file and remove these IP addresses that should no longer have access. 

### Open the file that contains the allow list

I opened the "allow_list.txt" file. First, I assigned this file name as a string to the import_file variable:
```
import_file = "allow_list.txt"
```

Then, I used a with statement to open the file: 
```
with (open(import_file, "r") as file:
```
The with function serves to manage resources by closing the file after exiting the with statement. The open() function contains to parameters, the file to import and the task to perform with the file, in this example "r" indicates I want to read it. the keyword as assigns a variable named file, that stores the output of the open() function while I work within the with statement. 

### Read the file contents

I used .read() to convert the file to string
```
with open(import_file, "r") as file:
  #Use .read() to read the imported file and store it in a variable named 'ip_addresses'
ip_addresses = file.read()
```
This code allows me to read the contents of the "allow_list.txt" file into a string format that allows me to later use the string to organize and extract the data. 

### Convert the string to a list 

In order to remove individual IP addresses from the allow list file, I need to convert it to a list format. I used .split() to do so: 
```
ip_addresses = ip_addresses.split()
```
The .split() function works by splitting the text into separate elements, by default it uses whitespace to do so. Each of the IP addresses in the string is separated by whitespace, so the IP addresses are separated and stored into a list, that I reassigned back to the variable ip_addresses. 

### Iterate through the remove list

