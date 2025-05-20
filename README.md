# 🏦 Online Banking Service

An interactive online banking application built using **Streamlit** and **MongoDB**. This project simulates a basic banking system that allows users to open accounts, view account details, deposit and withdraw money, and check account balances through a clean, user-friendly web interface.

---

## 📌 Overview

This web-based banking service offers a seamless experience for performing essential banking operations. It features:

- User account management
- Real-time balance updates
- Transaction tracking
- Image uploads for user profiles
- Secure and efficient database operations

---

## 🚀 Features

### 📝 Open an Account
- Fill out a form with details: account number, type, user ID, name, email, and initial balance.
- Upload a profile image, encoded in base64 and stored securely in MongoDB.
- Data validation ensures all required fields are completed.

### 🔍 View Account Details
- Retrieve complete account information using a user ID.
- Displays account number, type, user ID, name, email, and current balance.

### 💰 Deposit Money
- Enter user ID and amount to deposit.
- Updates account balance in real-time and logs the transaction in the database.

### 💸 Withdraw Money
- Input user ID and desired withdrawal amount.
- Ensures sufficient balance before processing and logs the transaction.

### 📊 Check Balance
- Instantly fetch current balance using the user ID.

---

## 🛠️ Tools & Technologies

| Tool        | Description |
|-------------|-------------|
| **Streamlit** | Used to create the web UI with forms, buttons, and navigation sidebar. |
| **MongoDB**   | NoSQL database for storing user and transaction data. |
| **Pymongo**   | Python driver for MongoDB integration. |
| **PIL (Pillow)** | For handling user-uploaded images. |
| **Base64**    | Encodes images into ASCII text for storage. |
| **IO**        | Manages image byte streams for encoding and decoding. |

---

## 🔄 Program Flow

### 🔌 MongoDB Connection
- Connects to a local MongoDB instance on `localhost:27017`.
- Uses `atm` database with two collections: `users` and `transactions`.

### 🖼️ Image Encoding
- Converts uploaded images to base64 format using a custom `encode_image()` function.
- Encoded images are stored as strings in MongoDB.

### 🧩 Streamlit Interface
- App titled **ATM SYSTEM**.
- Sidebar menu for navigation:
  - Open Account
  - View Account Details
  - Deposit Money
  - Withdraw Money
  - Check Balance

### 🧾 Form & Transaction Handling
- **open_account**: Collects user inputs, encodes image, stores in MongoDB.
- **view_account_details**: Fetches and displays account info.
- **deposit_money** / **withdraw_money**: Updates balance, logs transactions.
- **check_balance**: Displays current balance.

### ⚠️ Error Handling
- Ensures required fields are completed.
- Validates sufficient funds before withdrawal.
- Displays appropriate success and error messages to guide users.

---

## 📷 Screenshots (Optional)
_Add screenshots or GIFs here to showcase the application interface._

---

## 🧪 Installation & Run

```bash
# Clone the repo
git clone https://github.com/yourusername/online-banking-service.git
cd online-banking-service

# Install dependencies
pip install streamlit pymongo pillow

# Run the app
streamlit run app.py
```

---

## 📬 Feedback & Contributions

Pull requests and issues are welcome. Feel free to fork this project and improve it!

---

## 🪪 License

This project is open-source and available under the [MIT License](LICENSE).

