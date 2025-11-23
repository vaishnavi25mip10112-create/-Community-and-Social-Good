**Project Title**__
Community Resource Navigator - Essential Services Locator System

**Overview of the Project**
The Community Resource Navigator is a Python-based application designed to help vulnerable populations quickly locate essential community services. The system maintains a database of resources including food banks, shelters, and health clinics, allowing users to search by category and zip code. Built as an offline-capable solution, it can be deployed in community centers, libraries, and social service offices to assist people who need immediate access to support services but lack internet connectivity or technical resources.

**Features**
**Core Functionality**

Search resources by category (Food, Shelter, Health, or All)
Filter results by zip code for location-specific information
Add new community resources to the database
View complete list of all available resources
Save changes to persistent CSV storage
**User Experience**
Simple numeric menu navigation
Clear display of resource details (name, address, phone, hours)
Input validation with helpful error messages
Confirmation messages for all operations
"Press Enter to continue" flow for easy navigation

**Technical Features**

Offline operation without internet requirement
CSV-based data storage for easy access and editing
Persistent data across program sessions
Modular code structure for maintainability


**Technologies/Tools Used**

Programming Language: Python 3.x
Built-in Library: csv module for file handling
Data Format: CSV (Comma-Separated Values)
Data Structure: Lists and dictionaries for in-memory storage
Development Environment: Any Python-compatible IDE or text editor
Operating Systems: Compatible with Windows, macOS, and Linux


**Steps to Install & Run the Project**
**Prerequisites**

Python 3.x installed on your system
Text editor or IDE (optional but recommended)

**Installation Steps**
**Step 1:** Prepare the Files

Save the Python code as resource_navigator.py
Create a CSV file named resources.csv in the same directory

**Step 2:** Create the CSV File
Create resources.csv with the following header row:
name,category,address,phone,hours,zip_code
**Step 3:** Add Sample Data (Optional)
Add sample resources under the header:
Community Food Bank,Food,123 Main Street,555-0100,9AM-5PM,12345
Hope Shelter,Shelter,456 Oak Avenue,555-0200,24/7,12345
Free Health Clinic,Health,789 Pine Road,555-0300,8AM-4PM,12346
**Step 4:** Run the Program
Open terminal or command prompt, navigate to the project directory, and run:
python resource_navigator.py
Running on Different Systems
Windows:
cd path\to\project
python resource_navigator.py
**Instructions for Testing**
**Test Case 1**: Search Functionality

Run the program
Select option 1 (Search for resources)
Choose a category (1-4)
Enter a zip code that exists in your data
Expected Result: All matching resources display with complete information

**Test Case 2:** Search with No Results

Select option 1
Choose any category
Enter a zip code that doesn't exist (e.g., 99999)
**Expected Result:** "No resources found" message appears

**Test Case 3**: Add New Resource

Select option 2 (Add new resource)
Enter details for a new resource:

**Name:** Test Resource
**Category:** Food
**Address:** 100 Test St
**Phone:** 555-9999
**Hours:** 10AM-6PM
**Zip:** 12345


Choose 'y' to save to file
**Expected Result:** Success message appears

**Test Case 4:** View All Resources

Select option 3 (View all resources)
**Expected Result:** Complete numbered list of all resources displays

**Test Case 5:** Data Persistence

Add a new resource and save it
Select option 4 to exit
Run the program again
Select option 3 to view all resources
Expected Result: Previously added resource appears in the list

**Test Case 6:** Input Validation

At main menu, enter an invalid option (e.g., 5 or 'abc')
Expected Result: Error message "Please enter a number between 1 and 4"
During search, leave zip code blank and press Enter
Expected Result: Error message "Please enter a zip code"

**Test Case 7:** Category "All" Filter

Select option 1
Choose option 4 (All Categories)
Enter a zip code with multiple category types
Expected Result: Resources from all categories in that zip code display

**Test Case 8:** Empty Database Handling

Create an empty CSV file with only headers
Run the program
Select option 3
**Expected Result:** "No resources available" message displays


**Troubleshooting**
**Issue:** "FileNotFoundError: resources.csv"
**Solution:** Create resources.csv file in the same directory as the Python script

**Issue:** Program crashes when reading CSV
**Solution:** Ensure CSV has proper header row and correct field names

**Issue:** Resources not saving
**Solution:** Check file permissions and ensure you selected 'y' when prompted to save

**Issue:** Python command not recognized
**Solution:** Ensure Python is installed and added to system PATH
