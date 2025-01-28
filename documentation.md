


Hotel Reservation System Documentation	1
Introduction	1
Requirements  Specifications	2
1. Why Requirements Specifications	2
2. Program Objectives	2
3. Detailed Objectives	3
4. Non-Objectives (What the System Will Not Do)	3
5. Success Metrics	4
Design Documents	4
Technical Design Document for Hotel Room Reservation System	4
1. Purpose	4
2. System Overview	4
3. Functional Specifications	4
Reserve a Room	4
View Room Status	4
Search Guest	4
4. Architecture	5
5. Data Structures	5
Dynamic Arrays	5
6. Control Flow	5
7. Algorithms	6
8. Memory Management	6
9. Error Handling	7
10. Dependencies	7
11. Future Enhancements	7
Test Plan	7
Objective	7
Test Scenarios	7
1. System Start and Menu Navigation	7
2. Room Reservation	8
3. View Room Status	8
4. Help with Booking	8
5. Exit System	9
User Manuals	9
Features	9
Room Reservation	9
View Room Status	10
Get Help with Booking	10
Exit	10
How to Use the Program	10
Starting the Program	10
Navigating the Menu	10
Reserving a Room	10
Viewing Room Status	11
Editing Guest Data	11
Searching Guest Data	11
Canceling a Reservation	11
Exiting the Program	12
Error Handling	12
Invalid Menu Choice	12
Room Type Fully Booked	12
Invalid Guest Information	12
Guest Not Found	12
Memory Management Errors	12
Conclusion	12
Change Management	13
Background	13
Key Features by Version	13
Version 1	13
Version 2	13
Version 3	13
Version 4	13
Final Project	14
Change Implementation Process	14
Requirement Analysis	14
Version Integration	14
Code Refactoring	14
Testing	14
Testing and Validation	14
Error Handling	14
User Experience	15
Challenges and Resolutions	15
Conflict Resolution	15
Integration Issues	15
Conclusion	15


Hotel Reservation System Documentation

Introduction
This documentation offers a detailed overview of the Hotel Reservation System developed in C++. The system is intended to streamline the management of hotel room bookings, allowing users to reserve rooms, check availability, and handle guest information through a terminal-based interface. 
The documentation includes the following sections:
Requirement Specification: This section outlines the functional and non-functional requirements that the system must fulfill.
Design Documents: Here, the architectural and interface designs that guide the system's implementation are described.
Test Plans: This part details the testing strategies and cases used to ensure the system's reliability and performance.
Users Manuals: Instructions for end-users on how to effectively navigate and utilize the system are provided in this section.
Change Management: This section tracks modifications made to the system over time, ensuring transparency and maintainability.
The goal of this documentation is to serve as a foundational resource for developers, testers, and users, providing a clear understanding of the system's capabilities and operational guidelines.


















Requirements  Specifications
Requirements Specification Document: Hotel Room Reservation System
1. Why Requirements Specifications
Purpose
This document shall establish the objectives for a Hotel Room Reservation System. It shall define what the system is supposed to achieve and shall give the right direction to the development.
Scope
This system will manage room reservations for a hotel with a fixed number of 150 rooms. The rooms are categorized into three types: Ocean View Suites, Poolside Villas, and Garden View Rooms.
Target Audience:
This is the development document for all parties involved in the development process. The document shall set expectations about the objectives of the application.
2. Program Objectives
Primary Goal:
The basic aim of this application is to deliver an easy way to book a room, get information regarding booking, and see room availability within the hotel.
Functional Objectives:
System functionalities are required as follows:
Room Reservation:
Enable users to reserve a room by specifying their desired room type.
Check availability for the specified room type.
Collect necessary guest information for the reservation (name, gender, age, ID).
Provide a unique reservation code for the reservation.
Room Status View:
Give the user the facility to view the present availability status of all the rooms.
Booking Assistance:
Provide users with support in regards to their bookings; contact information for example.
Quit:
Allow the users to exit the application cleanly


User Experience Requirements
The system shall be easy to use, and the user shall feel easy navigating the system.			
Design and Implementation Requirements: The system shall be designed in such a way that the user is given proper prompts and feedback by the system.
It should flash the right error message the instant a user is making an error.
It shall not require the user to have prior knowledge about any hotels while using this system.
Technical Objectives:
The system will be implemented using fundamental C++ concepts, including dynamic memory allocations and pointers to store the variables of the program.
The program shall perform all its functions with sufficient speed and shall not crash.
3. Detailed Objectives
Room Reservation Objective:
The system shall allow a user to select a room type.
It should take the required information of the guest.
The system shall see if a room is available as per the type of room specified.
If available, it should allot the room and print out a success message along with the room allotted while providing the user with a reservation code.
If no rooms are available for that room type, then the system will have to reject the request.
Room Status Objective:
The system should make it easy for them to see all the rooms.
The system will display all rooms
The system will indicate whether a room is reserved or available.
Booking Assistance Objective
The system shall provide assistance to the users in terms of using the system.
Exit Application Objective
The user shall be able to exit the application through a menu option.
4. Non-Objectives (What the System Will Not Do)
The system shall not interface with a database to store reservations.
The system shall not be designed to handle over 150 rooms
System will not be implemented for advanced searching 
Users will not be authenticated through the system. 
5. Success Metrics
The ability to book the room, the status of a room, and a help functionality of the programme should meet its main purpose:

Design Documents
Technical Design Document for Hotel Room Reservation System
 
1. Purpose
The purpose of this document is to provide a detailed technical design for the Compile Crew  Hotel Room Reservation System. It includes system architecture, data structures, control flow, memory management, and error handling details. 
2. System Overview
The system is a console-based hotel reservation application that facilitates:
Room booking based on room type.
Managing guest information.                                                         
Searching guest details by name or reservation code.
Viewing room status (reserved or available). 
3. Functional Specifications
Reserve a Room
Input: Guest details (name, gender, age, ID, and reservation code).
Output: Room assignment and confirmation.
View Room Status
Input: None
Output: List of room statuses (available or reserved).
Search Guest
By Name
Input: Guest name.
Output: Guest details and room number.
By Reservation Code:
Input: Reservation code.
Output: Guest details and room number.
Exit
Input: None.
Output: Frees all memory and exits the program. 
4. Architecture
The system follows a modular, procedural approach with the following modules:
Input Validation Module: Ensures user inputs are valid.
Reservation Module: Handles room bookings.
Search Module: Retrieves guest information.
Room Status Module: Displays reservation statuses.
Memory Management Module: Allocates and deallocates memory. 
5. Data Structures
Dynamic Arrays
Array
Purpose
Data Type
 Size
guest_reservation  
Tracks reservation status (1/0).
Int                       
150
guest_name
Stores guest names.
char*
150
guest_gender
Stores guest genders.
char*
150
guest_age
Stores guest ages.
int
150
guest_id
Stores guest ID or passport numbers.
char*
150
reservation_code
Stores unique reservation codes.
int
150

6. Control Flow
Main Menu: Displays options for reserving rooms, checking room status, searching for guests, and exiting.
Reservation Process:
Validates room type and guest details.
Updates guest information arrays and marks room as reserved.
Room Status Display: Iterates through guest_reservation and prints the status for each room.
Search Process:
Searches by name: Iterates through each guest_name.
Searches by reservation code: Iterates through reservation_code.
Exit Process: Frees dynamically allocated memory.
 
7. Algorithms
Room Reservation:
Input: Room type and guest details.
Validate room availability and age (≥18).
Update data arrays (guest_name, guest_gender, etc.).
Mark room as reserved in guest_reservation.
Room Status Check:
Iterate through guest_reservation.
Print "Available" if value is 0.
Print "Reserved" if value is 1.
Search Guest:
By Name:
Compare input with each value in guest_name using strcmp().
By Reservation Code:
Compare input with each value in reservation_code.
Exit Process:
Use delete[] to free dynamically allocated memory.
 
8. Memory Management
Allocation:
Arrays for guest details (guest_name, guest_gender, guest_id) are allocated using new.
Each element is allocated a fixed size of 20 characters.
Deallocation:
Use delete[] to free memory for each array and its elements.
 

9. Error Handling
Invalid Inputs:
Display error message and re-prompt for valid inputs.
Room Unavailability:
Display a message indicating the selected room type is fully booked.
Underage Guest:
Reject booking for guests under 18 years old.
Duplicate Reservation Codes:
Enforce unique reservation codes during input validation. 
10. Dependencies
Libraries:
<iostream>: For input/output operations.
<cstring>: For string manipulation (e.g., strcmp).
<iomanip>: For align columns on table.
11. Future Enhancements
Replace arrays with STL containers (std::vector) for dynamic resizing.
Integrate a database for persistent data storage.
Add user authentication and role management.
Implement a GUI for a more user-friendly interface.
 
Test Plan
Objective
To verify that the Hotel Room Reservation System works as intended, covering the main functionalities: reserving rooms, viewing room statuses, searching for guests, canceling reservations, and handling incorrect inputs gracefully.

Test Scenarios
1. System Start and Menu Navigation
Test Case 1.1: Verify the system starts and displays the main menu.
Input: Run the program.
Expected Output: Main menu with options displayed.
Test Case 1.2: Verify menu input validation for invalid choices.
Input: Enter values like 0, 5, or non-numeric input.
Expected Output: Prompt to enter a valid number between 1 and 4.
2. Room Reservation
Test Case 2.1: Successfully reserve a room in each category.
Input: Choose room type 1, provide valid name, gender, age (18+), ID, and reservation code.
Expected Output: Reservation success message with room number.
Test Case 2.2: Attempt to reserve a room when all rooms of a selected type are booked.
Input: Try to reserve after filling all rooms of a type.
Expected Output: Message indicating the room type is fully booked.
Test Case 2.3: Attempt to reserve a room with an underage guest.
Input: Enter age less than 18.
Expected Output: Error message stating guests must be at least 18 years old.
Test Case 2.4: Input validation for room type choice.
Input: Enter invalid room type numbers (e.g., 0, 4).
Expected Output: Message to enter a valid room type.
3. View Room Status
Test Case 3.1: Verify room status display.
Input: Choose the "View Room Status" option after reserving some rooms.
Expected Output: Table showing reserved and available rooms.
4. Help with Booking
Search Guest
Test Case 4.1.1: Search guest by valid name.
Input: Provide the name of a reserved guest.
Expected Output: Guest details displayed correctly.
Test Case 4.1.2: Search guest by invalid name.
Input: Provide a name not in the system.
Expected Output: Message indicating no guest was found.
Test Case 4.1.3: Search guest by valid reservation code.
Input: Provide a valid reservation code.
Expected Output: Guest details displayed correctly.
Test Case 4.1.4: Search guest by invalid reservation code.
Input: Provide a reservation code not in the system.
Expected Output: Message indicating no reservation was found.
Cancel Reservation
Test Case 4.2.1: Successfully cancel a reservation.
Input: Provide a valid reservation code for cancellation.
Expected Output: Message indicating the reservation was canceled.
Test Case 4.2.2: Attempt to cancel with an invalid reservation code.
Input: Provide a reservation code not in the system.
Expected Output: Message indicating no such reservation exists.
About Services
Test Case 4.3.1: Display about services information.
Input: Choose "About Our Services" option.
Expected Output: Description of room types and services.
Contact Us
Test Case 4.4.1: Display contact information.
Input: Choose "Contact Us" option.
Expected Output: Display of contact details.
5. Exit System
Test Case 5.1: Exit the program.
Input: Choose the "Exit" option.
Expected Output: Program terminates with a goodbye message.
Edge Cases
Test Case 6.1: Input very long strings for name, gender, or ID (over 20 characters).
Expected Output: Truncated input or graceful handling.
Test Case 6.2: Attempt to reserve a room when all rooms in all categories are booked.
Expected Output: Message indicating no rooms are available.
Test Case 6.3: Cancel a reservation and then reserve the same room again.
Expected Output: Reservation successfully reassigned.
Post-Test Cleanup
Ensure no memory leaks by verifying that all dynamically allocated memory is freed after the program terminates. 


User Manuals
The Hotel Room Reservation System is a C++ program designed to help users reserve hotel rooms, view room statuses, and manage guest information. This user-friendly interface allows for seamless interaction with the hotel reservation process.
Features
	Room Reservation
Users can choose from three types of rooms:
Ocean View Suite
Poolside Villa
Garden View Room
Capture guest details including name, gender, age, ID/passport number, and  reservation code.

	View Room Status
Users can view the availability of all rooms, indicating which are reserved and which are free.
	Get Help with Booking
Search for guests by name or reservation code.
Edit guest data and modify reservations.
Cancel existing reservations.
 Access information about hotel services and contact details.
	Exit
Allows users to exit the program gracefully.
How to Use the Program
Starting the Program

Compile the program using a C++ compiler (e.g., CodeBlockIDE).
Run the executable file generated from the compilation.

Navigating the Menu

Upon launching, the main menu will display the available options:
    	1. Reserve a Room
    	2. View Room Status
    	3. Get Help With Booking
    	4. Exit

Enter the number corresponding to your choice and press Enter.

Reserving a Room

Choose the type of room you wish to reserve (Ocean View, Poolside, or Garden View).
Input the requested guest information:
Name: Must contain only letters and spaces.
Gender: Enter 'M' for Male or 'F' for Female.
Age: Must be 18 or older.
ID/Passport Number: Enter a valid identification number.
Reservation Code: Enter a unique code for the reservation.
The program will confirm your reservation and provide the room number.


Viewing Room Status

Select option 2 from the main menu.
The system will display the status of all rooms, indicating which are reserved and which are available.

Editing Guest Data

Choose option 3 to access help.
Select 2. Edit Guest Data from the help menu.
Enter the reservation code for the guest whose data you wish to edit.
If the reservation code is valid, you will be prompted to re-enter the guest's information:
Name
Gender
Age
ID/Passport Number
Reservation Code
The program will confirm the changes and update the reservation.

Searching Guest Data
Choose option 3 to access help.
Select 1. Search Guest from the help menu.
Choose whether to search by:
Name: Enter the guest's name to find their reservation details.
Reservation Code: Enter the reservation code to locate the guest.
The program will display the guest's information if found; otherwise, it will indicate that no guest was found.

Canceling a Reservation

Choose option 3 to access help.
Select 3. Cancel Reservation from the help menu.
Enter the reservation code of the guest whose reservation you wish to cancel.
If the reservation code is valid, the program will cancel the reservation and free up the room.
You will receive confirmation of the cancellation.

Exiting the Program

To exit the program, select option 4 from the main menu.
The program will thank you for using the service and close.

Error Handling
Common Errors and Solutions

	Invalid Menu Choice
If an invalid number is entered, the program will prompt you to enter a number between 1 and 4. Ensure you are entering a valid option.

	Room Type Fully Booked
If the selected room type is fully booked, the program will notify you and prompt you to choose a different room type.

	Invalid Guest Information
Name: Must contain only letters and spaces. If invalid input is detected, you will be prompted to re-enter the name.
Gender: Must be either 'M' or 'F'. Invalid input will require re-entry.
Age: Must be 18 or older. If an invalid age is entered, you will be prompted to enter a valid age.

	Guest Not Found
If a guest is not found via name or reservation code, the program will inform you and return you to the help menu.

	Memory Management Errors
The program dynamically allocates memory for storing guest information. Ensure that your system has enough memory available, or you may encounter allocation failures.

Conclusion

This Hotel Room Reservation System is designed to streamline the process of booking and managing hotel accommodations. By following the instructions and guidelines in this manual, users can effectively utilize the system for their reservation needs. If you encounter any issues not covered in this manual, please consult with the program administrator for further assistance.
## Change Management

### Background
Change management is crucial for maintaining the integrity and functionality of the Hotel Reservation System. This section outlines the process for managing changes, including version control, requirement analysis, and implementation.

### Key Features by Version
#### Version 1
- Basic room reservation functionality
- View room status
- Search guest by name

#### Version 2
- Enhanced search functionality by reservation code
- Improved error handling

#### Version 3
- Added booking assistance features
- Memory management improvements

#### Version 4
- User authentication and role management
- Integration with a database for persistent storage

### Final Project
The final project integrates all features from previous versions, ensuring a robust and user-friendly hotel reservation system.

### Change Implementation Process
#### Requirement Analysis
Identify and document new requirements or changes to existing functionalities.

#### Version Integration
Merge new features and changes into the main codebase, ensuring compatibility and stability.

#### Code Refactoring
Optimize and clean up the code to improve readability and maintainability.

#### Testing
Conduct thorough testing to ensure new changes do not introduce bugs or regressions.

### Testing and Validation
Ensure all functionalities work as expected through unit tests, integration tests, and user acceptance tests.

### Error Handling
Implement comprehensive error handling to manage unexpected issues gracefully.

### User Experience
Focus on enhancing the user experience by making the system intuitive and easy to navigate.

### Challenges and Resolutions
#### Conflict Resolution
Address and resolve conflicts that arise during development and integration.

#### Integration Issues
Identify and fix issues that occur when integrating new features or changes.

### Conclusion
Effective change management ensures the Hotel Reservation System remains reliable, efficient, and user-friendly, meeting the evolving needs of its users.