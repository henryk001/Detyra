Weather Data Scraper, API Integration, and Encryption Script
============================================================

This project scrapes a list of cities and their geographic coordinates from a Wikipedia page, 
fetches weather data using the Open-Meteo API, saves the data to a CSV file, and encrypts the 
contents of the file. The decryption function prints the decrypted data without modifying the CSV file.

------------------------------------------------------------
Prerequisites
------------------------------------------------------------

Ensure you have Python 3.x installed on your machine. Install the required packages using the command:

pip install -r requirements.txt

Required Python Packages:
- requests: For sending HTTP requests to fetch webpage and weather API data.
- beautifulsoup4: For parsing HTML content and extracting the table data.
- cryptography: For encrypting and decrypting the CSV file.

------------------------------------------------------------
Instructions
------------------------------------------------------------

1. Clone or Download the Repository
------------------------------------
Download the project files to your local machine.

2. Install Required Packages
----------------------------
Run the following command to install the dependencies:

pip install requests beautifulsoup4 cryptography

3. Execute the Script
---------------------
Run the script using the following command:

python script.py

4. Features
-----------
Web Scraping:
- Extracts a list of cities and their geographic coordinates from a Wikipedia page.
- Filters cities based on population greater than 5,000.

API Integration:
- Uses the Open-Meteo API to fetch weather data (temperature, wind speed, etc.) for each city.
- Supports error handling for invalid data or network issues.

CSV Handling:
- Saves weather data into a file named `weather_data.csv`.
- If the file already exists, its content is overwritten.

Encryption:
- Encrypts the contents of the `weather_data.csv` file using AES-based symmetric encryption (`cryptography` library).
- Prints the encryption key for secure storage.

Decryption:
- Reads and decrypts the contents of the CSV file, displaying them in the terminal without altering the encrypted file.

------------------------------------------------------------
Example Output
------------------------------------------------------------

After running the script:
- The `weather_data.csv` file will contain encrypted weather data.
- The decryption function will display the readable data in the console.

Example:
Decrypted File Content:
City: Tirana, Temperature: 15°C, Windspeed: 10 km/h
City: Durrës, Temperature: 13°C, Windspeed: 12 km/h
...

------------------------------------------------------------
How to Use the Script
------------------------------------------------------------

Step 1: Modify the Target URL (Optional)
----------------------------------------
The target URL for scraping is set to the Wikipedia page for cities in Albania. You can modify the 
`url` variable if you want to scrape a different page.

Step 2: Run the Script
----------------------
Run the script using:
python script.py

Step 3: Save the Encryption Key
-------------------------------
After running the script, the encryption key will be displayed in the terminal. Save this key securely, 
as it is required for decryption.

Step 4: Decrypt the File
------------------------
Call the `decrypt_csv_file_to_notebook` function to print the decrypted file contents:

decrypt_csv_file_to_notebook('weather_data.csv', key)

------------------------------------------------------------
Notes
------------------------------------------------------------

1. **Encryption Key:** The encryption key is generated during runtime. Save it securely, as losing the 
   key will make it impossible to decrypt the file.

2. **API Usage:** Ensure you do not exceed the Open-Meteo API's rate limits.

3. **Error Handling:** The script includes basic error handling for network issues, invalid data, and timeouts.

------------------------------------------------------------
Acknowledgments
------------------------------------------------------------

- Wikipedia for city and geographic data.
- Open-Meteo for weather API services.
- Python libraries `requests`, `beautifulsoup4`, and `cryptography` for enabling the functionality.

Enjoy using the script!
