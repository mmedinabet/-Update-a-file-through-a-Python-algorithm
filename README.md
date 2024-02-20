<h1> Update a file through a Python algorithm</h1> 
<h2>Description:</h2>
At my organization, access to restricted content is managed through an "allow_list.txt" file containing approved IP addresses. To automate the removal of IP addresses that should no longer have access, I developed an algorithm that updates the "allow_list.txt" file based on a separate list of IP addresses to be removed.

<h2>Open the file that contains the allow list</h2>
For the first part of the algorithm, I opened the "allow_list.txt" file and the "removed_list" file.  First, I assigned file names as strings to the import_file and removed_list variables:

![Screenshot 2023-09-26 3 30 20 PM](https://github.com/mmedinabet/-Update-a-file-through-a-Python-algorithm/assets/142737434/d9dc0728-de9f-4405-8a1b-43550e938efc)


The 'with' statement was used to open the file:

![Screenshot 2023-09-26 3 31 37 PM](https://github.com/mmedinabet/-Update-a-file-through-a-Python-algorithm/assets/142737434/4586f08a-e10c-464a-a89e-76e604886948)

The 'with' statement and the '.open( )' function in read mode are used together to open the allow list and be able to read it. The main goal of opening the file is to have accesss to the list of IP addresses in the allow file. In the code with open(import_file, "r") as file:, the 'open( )' function has two parameters. The first identifies the file to import, and then the second indicates what I want to do with the file. In this case, "r" indicates that I want to read it.

<h2>Read the file contents</h2>
In order to read the file contents, I used the '.read( )' method to convert it into the string: 

![Screenshot 2023-09-26 3 33 03 PM](https://github.com/mmedinabet/-Update-a-file-through-a-Python-algorithm/assets/142737434/291c6b3f-4501-49d4-8900-535a7988a461)

The '.read()' method converts the file into a string and allows me to read it. I applied the .read() method to the file variable identified in the with statement. Then, I assigned the string output of this method to the variable ip_addresses. 

<h2>Convert the string into a list</h2>
I used the '.split( )' method to convert the ip_addresses string into a list by removing the invidual IP addresses from the allow list. 

![Screenshot 2023-09-26 3 34 42 PM](https://github.com/mmedinabet/-Update-a-file-through-a-Python-algorithm/assets/142737434/de115b35-e149-4d2f-a4b4-e88d05bde1ce)

The '.split( )' function is used to convert its contents of a string to a list. The purpose of splitting ip_addresses into a list is to make it easier to remove IP addresses from the allow list. In this algorithm, the '.split( )' function takes the data stored in the variable ip_addresses, which is a string of IP addresses that are each separated by a whitespace, and it converts this string into a list of IP addresses. To store this list, I reassigned it back to the variable ip_addresses

<h2>Iterate through the remove list</h2>
A relevant section of my algorithm involves iterating through the IP addresses that are elements in the remove_list. To do this, I incorporated a 'for loop':

![Screenshot 2023-09-26 3 37 55 PM](https://github.com/mmedinabet/-Update-a-file-through-a-Python-algorithm/assets/142737434/1244f18d-68df-43ad-a519-9fc304252f19)

The 'for loop' in Python repeats code for a specified sequence. The overall purpose of the for loop in a Python algorithm like this is to apply specific code statements to all elements in a sequence. The for keyword starts the for loop. It is followed by the loop variable element and the keyword in. The keyword in indicates to iterate through the sequence ip_addresses and assign each value to the loop variable element. 

<h2>Remove IP addresses that are on the remove list</h2>

My algorithm requires removing any IP address from the allow list, ip_addresses, that is also contained in remove_list. First, for loop is required to create a conditional that evaluated whether or not the loop variable element was found in the ip_addresses list. 


![Screenshot 2023-09-26 3 48 27 PM](https://github.com/mmedinabet/-Update-a-file-through-a-Python-algorithm/assets/142737434/7485b4fc-6ca5-4f79-917e-9bc447eab8d1)

Then, within that conditional, I applied .remove() to ip_addresses. I passed in the loop variable element as the argument so that each IP address that was in the remove_list would be removed from ip_addresses as well. 

<h2>Update the file with the revised list of IP addresses</h2>
  
In order to finalize my algorithm, I needed to update the allow list file with the revised list of IP addresses. I used the 'join( )' methond since I needed to convert the list back into a string. 

![Screenshot 2023-09-26 3 54 52 PM](https://github.com/mmedinabet/-Update-a-file-through-a-Python-algorithm/assets/142737434/05da8007-bfb4-4777-a261-f709561b8f79)

I used the '.join( )' method to create a string from the list ip_addresses so that I could pass it in as an argument to the .write() method when writing to the file "allow_list.txt". I used the string ("\n") as the separator to instruct Python to place each element on a new line. 

Then, I used another with statement and the '.write( )' method to update the file:

![Screenshot 2023-09-26 3 56 43 PM](https://github.com/mmedinabet/-Update-a-file-through-a-Python-algorithm/assets/142737434/c2ad0c24-d24a-440a-9982-60db37284ff2)

This time, I used a second argument of "w" with the 'open( )' function in my with statement. This line of code indicates that I want to open a file to write over its contents. 

<h2>Summary</h2>
I created an algorithm to update the "allow_list.txt" file, which contains approved IP addresses. This algorithm involves reading the file, converting its contents into a list, and then iterating through a "remove_list" to remove any matching IP addresses. After removing them, the algorithm converts the updated list back into a string and overwrites the "allow_list.txt" file with the revised IP address list.the project significantly reduced the potential for human error, enhanced operational efficiency, and bolstered our organization's security posture. This initiative not only demonstrated my proficiency in Python programming and file handling but also showcased my ability to develop practical solutions to real-world challenges, aligning with the organization's goals of innovation and process optimization.
