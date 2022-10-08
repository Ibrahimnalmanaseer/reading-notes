# FileIO & Exceptions

## FileIO 

### What Is a File? 

a file is a contiguous set of bytes used to store data, This data is organized in a specific format and can be anything as simple as a text file or as complicated as a program executable.

file parts :
- Header : contains (file name , size, type).
- Data : contents of the file as written by the creator or editor.
- End of File : special character that indicates the end of the file .

### File Paths 

The file path is a string that represents the location of a file. It’s broken up into three major parts:
- Folder Path: the file folder location on the file system where subsequent folders are separated by a forward slash / (Unix) or backslash \ (Windows).
- File Name: the actual name of the file.
- Extension: the end of the file path pre-pended with a period (.) used to indicate the file type.

### Opening and Closing a File in Python

There is many ways to open the file , the most important that you should make sure to close the file after you done your work ,This can lead to unwanted behavior including resource leaks. It’s also a best practice within Python (Pythonic) to make sure that your code behaves in a way that is well defined and reduces any unwanted behavior.

