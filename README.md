Regex Data Extraction Tool
This Is a python project that provides a utility class to extract common data types such as emails and phone numbers using regular expresssions.

Features
The regular expressions extracts: - Email addresses - Phone numbers - Time (24-hour Format) - URLs(HTTP and HTTPS) - Credit Card numbers (16-digit format)

How it works
The "extract_data" class uses the python module "re" to search for patterns in the given string. Each method target certain type of data using regular expressions.

How to use
1. Clone the repository
2. Provide input
Use any string of text that contains data you want to extract. This include a text with: - Email addresses - Phone numbers - Time (24-hour Format) - URLs(HTTP and HTTPS) - Credit Card numbers (16-digit format)

3. Instantiate the class and call the methods
from extract_data import extract_data

text = """
Extracted Data:
emails: ['elvisdev@alu.edu']
Phone Numbers (+250, +1): ['+250787932359', '+1 202-555-0182']
Hours: ['8:30']
URLs: ['https://www.digitalvault.rw']
Credit Cards: ['4567-8910-1112-1314']

"""

extractor = extract_data(text)
results = extractor.extract_all()

for key, value in results.items():
    print(f"{key}: {value}")
Output
Extracted Data:
emails: ['elvisdev@alu.edu']
Phone Numbers (+250, +1): ['+250787932359', '+1 202-555-0182']
Hours: ['8:30']
URLs: ['https://www.digitalvault.rw']
Credit Cards: ['4567-8910-1112-1314']

Contributions
Pull requests and any improvements on the code are welcome. Feel free to fork the repository and submit a PR.
