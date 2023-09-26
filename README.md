<h1> Update a file through a Python algorithm</h1> 
<h2>Description:</h2>
You are a security professional working at a health care company. As part of your job, you're required to regularly update a file that identifies the employees who can access restricted content. The contents of the file are based on who is working with personal patient records. Employees are restricted access based on their IP address. There is an allow list for IP addresses permitted to sign into the restricted subnetwork. There's also a remove list that identifies which employees you must remove from this allow list.

Your task is to create an algorithm that uses Python code to check whether the allow list contains any IP addresses identified on the remove list. If so, you should remove those IP addresses from the file containing the allow list.

<h2>Open the file that contains the allow list</h2>
For the first part of the algorithm, I opened the "allow_list.txt" file. First, I assigned this file name as a string to the import_file variable:

![Screenshot 2023-09-26 3 30 20 PM](https://github.com/mmedinabet/-Update-a-file-through-a-Python-algorithm/assets/142737434/d9dc0728-de9f-4405-8a1b-43550e938efc)

The 'with' statement to open the file:

![Screenshot 2023-09-26 3 31 37 PM](https://github.com/mmedinabet/-Update-a-file-through-a-Python-algorithm/assets/142737434/4586f08a-e10c-464a-a89e-76e604886948)

The 'with' statement and the .open() function in read mode are used together to open the allow list and be able to read it. The main goal of opening the file is to have accesss to the list of IP addresses in the allow file. In the code with open(import_file, "r") as file:, the open() function has two parameters. The first identifies the file to import, and then the second indicates what I want to do with the file. In this case, "r" indicates that I want to read it.

<h2>Read the file contents</h2>
In order to read the file contents, I used the .read() method to convert it into the string: 

![Screenshot 2023-09-26 3 33 03 PM](https://github.com/mmedinabet/-Update-a-file-through-a-Python-algorithm/assets/142737434/291c6b3f-4501-49d4-8900-535a7988a461)

The .read() method converts the file into a string and allows me to read it. I applied the .read() method to the file variable identified in the with statement. Then, I assigned the string output of this method to the variable ip_addresses. 

<h2>Convert the string into a list</h2>
I used the .split() method to convert the ip_addresses string into a list by removing the invidual IP addresses from the allow list. 

![Screenshot 2023-09-26 3 34 42 PM](https://github.com/mmedinabet/-Update-a-file-through-a-Python-algorithm/assets/142737434/de115b35-e149-4d2f-a4b4-e88d05bde1ce)

The .split() function is used to convert its contents of a string to a list. The purpose of splitting ip_addresses into a list is to make it easier to remove IP addresses from the allow list. In this algorithm, the .split() function takes the data stored in the variable ip_addresses, which is a string of IP addresses that are each separated by a whitespace, and it converts this string into a list of IP addresses. To store this list, I reassigned it back to the variable ip_addresses

<h2>Iterate through the remove list</h2>
A relevant section of my algorithm involves iterating through the IP addresses that are elements in the remove_list. To do this, I incorporated a 'for loop':

![Screenshot 2023-09-26 3 37 55 PM](https://github.com/mmedinabet/-Update-a-file-through-a-Python-algorithm/assets/142737434/1244f18d-68df-43ad-a519-9fc304252f19)

The 'for loop' in Python repeats code for a specified sequence. The overall purpose of the for loop in a Python algorithm like this is to apply specific code statements to all elements in a sequence. The for keyword starts the for loop. It is followed by the loop variable element and the keyword in. The keyword in indicates to iterate through the sequence ip_addresses and assign each value to the loop variable element. 

<h2>Remove IP addresses that are on the remove list</h2>

![Screenshot 2023-09-26 3 48 27 PM](https://github.com/mmedinabet/-Update-a-file-through-a-Python-algorithm/assets/142737434/7485b4fc-6ca5-4f79-917e-9bc447eab8d1)

<h2>Update the file with the revised list of IP addresses</h2>

![Screenshot 2023-09-26 3 54 52 PM](https://github.com/mmedinabet/-Update-a-file-through-a-Python-algorithm/assets/142737434/05da8007-bfb4-4777-a261-f709561b8f79)

![Screenshot 2023-09-26 3 56 43 PM](https://github.com/mmedinabet/-Update-a-file-through-a-Python-algorithm/assets/142737434/c2ad0c24-d24a-440a-9982-60db37284ff2)


<h2>Summary</h2>
