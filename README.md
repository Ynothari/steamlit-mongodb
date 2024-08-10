# atm
ATM machine

OVERVIEW:
The Banking Services program is developed using Streamlit for the front-end interface and MongoDB for the database. The program allows users to perform various banking activities, including opening accounts, viewing account details, depositing money, withdrawing money, and checking balances. This document outlines the tools used and topics covered in the program.
TOOLS USED:
1.	Streamlit: A Python library used for creating interactive web applications. In this program, Streamlit is used to create the user interface, enabling users to interact with the system through forms and buttons.
2.	MongoDB: A NoSQL database used to store user information and transaction records. The pymongo library is utilized to interact with the MongoDB database.
3.	PIL (Python Imaging Library): A library for opening, manipulating, and saving image files. It is used to handle user-uploaded images for account creation.
4.	Base64: A method for encoding binary data (like images) into ASCII text. This is used to store images in the MongoDB database.
5.	IO (Input/Output): A core Python module used for managing streams, in this case, to handle image data.
TOPICS COVERED:
Opening an Account:
1.	Users can open a new account by providing account details such as account number, account type, user ID, name, email, and an initial balance.
2.	Users are required to upload a picture, which is encoded to base64 and stored in MongoDB.
3.	The program ensures all necessary information is provided and stores the user details in the users collection.
Viewing Account Details:
1.	Users can view their account details by entering their user ID.
2.	The program fetches and displays details such as account number, account type, user ID, name, email, and current balance from the MongoDB users collection.
Depositing Money:
1.	Users can deposit money into their account by entering their user ID and the amount to be deposited.
2.	The program updates the user's balance in the MongoDB database and records the transaction in the transactions collection.
Withdrawing Money:
1.	Users can withdraw money from their account by providing their user ID and the amount to be withdrawn.
2.	The program checks if the user has sufficient balance before updating the balance and recording the transaction.

Checking Balance:
1.	Users can check their account balance by entering their user ID.
2.	The program retrieves and displays the current balance from the MongoDB users collection.
DETAILED PROGRAM FLOW
MongoDB Connection:
1.	The program establishes a connection to a MongoDB instance running locally on port 27017.
2.	It connects to the atm database and accesses two collections: users and transactions.
Image Handling:
1.	The encode_image function converts an uploaded image to base64 encoding, allowing it to be stored as a string in the database.
Streamlit Interface:
1.	The main title of the app is set to "ATM SYSTEM".
2.	A sidebar is created for navigation, allowing users to choose from options like "Open Account," "View Account Details," "Deposit Money," "Withdraw Money," and "Check Balance."
Form Handling:
1.	The open_account function creates a form for account registration. It collects user inputs, encodes the image, and stores all information in the MongoDB users collection.
2.	The view_account_details function retrieves and displays user details from the MongoDB users collection.
3.	The deposit_money and withdraw_money functions handle financial transactions, updating the user's balance and recording each transaction in the transactions collection.
4.	The check_balance function retrieves and displays the current balance of a user's account.
Error Handling:
1.	The program includes checks to ensure that the required information is provided and that sufficient funds are available for withdrawals.
2.	It provides success and error messages to guide users through the process
