Selenium Automation for MedPlusMart

Overview:

This project is a Selenium-based automation script designed to interact with the MedPlusMart website. It automates various actions such as logging in, searching for medicines, adding items to the cart, checking store locations, and logging out

Features:

Automated Login using phone number and OTP.

Search & Add to Cart for medicines and other products.

View Cart & Navigate Home functionality.

Store Finder Automation to check store locations.

Logout Automation to ensure a clean session.

Prerequisites:

Before running the script, ensure you have the following:

Python 3.x installed

Google Chrome installed

ChromeDriver (matching your Chrome version)

Required Python libraries:
pip install selenium

Installation & Setup:

Clone this repository or copy the script to your local machine.

Download ChromeDriver and place it in the system path or specify its location in the script.

Install dependencies using:

pip install selenium

Run the script:
python script.py

Usage:

The script will automatically launch Chrome, navigate to MedPlusMart, and perform automated actions.

It uses explicit waits to ensure elements are loaded before interaction.

The session will end with a logout, and the browser will close.

Error Handling:

The script includes try-except blocks to handle errors during execution.

If any action fails (e.g., element not found), it will print an error message and continue execution.

Improvements & Future Enhancements:

Enhance OTP handling: Implement a way to input OTP dynamically.

Data-driven testing: Use external data sources (CSV, JSON) for test inputs.

Headless execution: Modify the script to run Chrome in headless mode.


