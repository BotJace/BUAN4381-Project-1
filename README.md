# BUAN4381-Project-1
This project is an expense tracker that take user inputs for expenses with specific types Food and Transaction. The user may input any other sub categories for the types of transactions. The program will read, parse, edit, and write to a csv file. 

------

## Transaction Classes
The parent class transaction contains methods which include placing user inputs into a dictionary, and writing the dictionary to a csv file. The parent class also creates a unique ID which are always the first letter of the type of transaction followed by 8 numbers or charaters. 
The user inputs come from the child classes that prompt users for type of transaction, sub category, date and time (DD-MM-YYYY 24hr:minute), and location. Then the child classes send the information, through the use of super, back to the parent class.
<img width="668" height="239" alt="image" src="https://github.com/user-attachments/assets/8d2e161a-1f63-45e3-a556-779dd4fe5363" />

------
## Functions
### Helper function
the load_transactions function will check to see if the file called "expensese.csv" exists, and if it does it will return a list od dictionaries, and if it does not exist it will return an empty list.

### Search Function
The searching function takes in transaction type and sub category from user input. Then using the 2 inputs, the function loops through the list of dictionaries and returns all matching results. 
*Note:* The user inputs are case sensitive.
<img width="583" height="317" alt="image" src="https://github.com/user-attachments/assets/a37e7692-13b2-4bfa-90ee-f884f444043f" />

### Modify Function
The modify function to edit or update values in the dictionary takes in the unique ID and returns the row of key value pairs. 
*Note:* The search function must be run first to find the ID of the entry. In addition, the user inputs are case sensitive and the first letter must be capitalized.
After inputing the field the user wants to edit the user will be prompted to input a new value and it will be written to the file.
<img width="583" height="468" alt="image" src="https://github.com/user-attachments/assets/67264c82-a824-4310-95e9-c97ed14fa04f" />

------
## Menu
The menu is an infinite loop prompting users for the types of transactions they want to enter or quit. Quit will end the loop and Food or Transportation will run their respective functions and save it to the csv file. Search and Modify will also run their respective functions. 

-----
## Visualizations



### Improvements todo
- The program has many issues such as requireing case sensitivity in user inputs in order to run properly, the first inprovement should be to fix this by setting all inputs and checks to lower case to avoid case sensitive requirements. 
- The program could also take in specific inputs for day, month, year, and time or have another function that splices the current input into those fields.
- The program could also have more filters for the search function which includes asking for specifc days, months, year, times, or have the ability to skip those filters if the user desires.
  - The search function could also have a dynamic prompting system which gives the user all unique entries from the csv files in each column.


