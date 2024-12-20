Basic Chat-Driven Excel File Manipulation System.

Objective:
Create a backend-focused application where users can upload an Excel file and interact with it
through a chat interface to perform basic operations. The task should focus on essential
backend functionality with minimal requirements for UI.

Features
Upload an Excel file.
Perform the following operations:
Add Column: Add a new column with specified values.
Combine Columns: Combine values from specified columns into a new column.
Download the modified Excel file.

Technologies Used

Backend: Django
Frontend: HTML, CSS, JavaScript
Styling: CSS (with custom color themes)
File Handling: Pandas for Excel processing

Setup and Installation
1. Clone the Repository

git clone <repository-url>
cd <repository-name>

2. Set Up a Virtual Environment

python -m venv env

source env/bin/activate  # On Windows: env\Scripts\activate
3. Install Dependencies

pip install -r requirements.txt

4. Set Up the Database
Run the following commands to initialize the database:

python manage.py makemigrations
python manage.py migrate
5. Start the Development Server

python manage.py runserver

Usage

1. Access the Web Interface Open your browser and navigate to:

http://127.0.0.1:8000

2. Upload an Excel File
   Go to the Upload Your File section.
   Select an Excel file and click "Upload."
3. Perform Operations
   In the Perform Operations section:
Choose an operation:
Add Column: Provide a column name and define its values.
            Combine Columns: Enter the names of the columns you want to combine (comma-separated).

Click "Perform Operation."

4. Download Modified File

After performing the operations, navigate to the Download Updated File section.
Click the "Download Updated File" button to download the modified Excel file.

Endpoints Upload File

URL: /api/upload
Method: POST
Description: Uploads an Excel file and extracts its columns.
Perform Operation

URL: /api/operation
Method: POST
Description: Adds a new column or combines specified columns.
Download File

URL: /api/download
Method: GET
Description: Downloads the modified Excel file.

Example Input for Operations
1. Add Column
New Column Name: Discount
Columns to Combine: (Not required for this operation)
2. Combine Columns
New Column Name: Total
Columns to Combine: Price, Taxes

Error Handling

If an invalid operation or input is provided, error messages will be displayed in the UI.
Example: Error: Invalid operation type.


Future Enhancements

Add support for more Excel operations.
Improve the UI for mobile responsiveness.
Provide advanced preview functionality for processed files.
