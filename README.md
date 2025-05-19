Regex Data Extraction Tool
This is a Python project that provides a utility class to extract common data types such as emails, phone numbers, time, URLs, and credit card numbers using regular expressions.

🚀 Features
The tool can extract the following data types from a block of text:

✅ Email addresses

✅ Phone numbers (US and Rwanda formats)

✅ Time (24-hour format)

✅ URLs (HTTP and HTTPS)

✅ Credit card numbers (16-digit format)

⚙️ How It Works
The extract_data class uses Python’s built-in re module to identify and extract specific patterns. Each method targets a certain data type using optimized regular expressions.

📌 How to Use
1. Clone the repository
bash
Copy
Edit
git clone https://github.com/yourusername/alu_regex-data-extraction-yourusername.git
cd alu_regex-data-extraction-yourusername
2. Provide your input
Use any text string that includes data like:

Email addresses

Phone numbers (+250 and +1)

24-hour time format (e.g., 08:30, 14:45)

URLs (e.g., https://example.com)

Credit card numbers (xxxx-xxxx-xxxx-xxxx or xxxx xxxx xxxx xxxx)

3. Run the script
python
Copy
Edit
from extract_data import extract_data

text = """
Email: elvisdev@alu.edu
Phone Rwanda: +250787932359
Phone USA: +1 202-555-0182
Opening hour: 8:30
Website: https://www.digitalvault.rw
Credit Card: 4567-8910-1112-1314
"""

extractor = extract_data(text)
results = extractor.extract_all()

for key, value in results.items():
    print(f"{key}: {value}")
✅ Sample Output
less
Copy
Edit
Extracted Data:
emails: ['elvisdev@alu.edu']
Phone Numbers (+250, +1): ['+250787932359', '+1 202-555-0182']
Hours: ['8:30']
URLs: ['https://www.digitalvault.rw']
Credit Cards: ['4567-8910-1112-1314']
💡 Contributions
Contributions are welcome! If you have improvements, fixes, or additional patterns to include:

Fork the repository

Make your changes

Submit a pull request
