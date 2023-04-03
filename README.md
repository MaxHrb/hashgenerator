# hashgenerator
##Technical Documentation

#Purpose
The purpose of this Python script is to create a new XLS file with file metadata and SHA-512 hash value of an existing XLSX file. The new XLS file will have 6 columns with headers: file_name, create_date, modify_date, file_date, file_size, hash_value.

#Dependencies
This script requires the following Python modules to be installed:

hashlib
openpyxl
xlsxwriter
os
datetime
Usage
Set the path variable to the file path of the existing XLSX file.
Set the new_file_path variable to the desired file path and name of the new XLS file to be created.
Run the script.
Workflow
The script imports the necessary modules: hashlib, openpyxl, xlsxwriter, os, and datetime.
The script defines the path variable with the file path of the existing XLSX file, and the new_file_path variable with the desired file path and name of the new XLS file to be created.
The script uses openpyxl to load the existing XLSX file and get the active worksheet.
The script uses os to get the file metadata: file name, create date, modify date, file date, and file size.
The script uses hashlib to compute the SHA-512 hash value of the file.
The script uses xlsxwriter to create a new workbook and worksheet, and writes the headers to the first row of the worksheet.
The script writes the file metadata and hash value to the second row of the worksheet.
The script saves and closes the new workbook.
Functionality
The script reads an existing XLSX file and extracts its metadata: file name, create date, modify date, file date, and file size. It then computes the SHA-512 hash value of the file using hashlib. It then creates a new XLS file with the metadata and hash value in the format of 6 columns with headers: file_name, create_date, modify_date, file_date, file_size, and hash_value. The metadata and hash value are written to the second row of the new XLS file. The script saves and closes the new XLS file.

Limitations
This script only works with XLSX files and requires that the openpyxl module is installed. It may not work with very large files due to memory constraints. The script only computes the SHA-512 hash value and does not support other hash algorithms. The script overwrites any existing XLS file with the same name and path as new_file_path.
