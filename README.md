# SHA256-passwordcracking
A simple script created following TCM-Sec course 101 python for hackers.
The repository pourpose is to follow my knowledge progress. As I acquire knowledge, I will improve the script.

## Usage
First of all we need to get the password hash that is in pass.txt file. For this example we're using the password **python**:
```bash
└─$ echo -ne python | sha256sum 
```
This should return something like this
```bash
11a4a60b518bf24989d481468076e5d5982884626aed9faeb35b8576fcd223e1
```
Then our script will try to crack that hash:
```bash
└─$ python sha256-crack.py 11a4a60b518bf24989d481468076e5d5982884626aed9faeb35b8576fcd223e1
```
If everything goes right, the console should return
```bash
[+] Attempting to crack: 11a4a60b518bf24989d481468076e5d5982884626aed9faeb35b8576fcd223e1!
    : Password hash found after 0 attempts! python hashes to 11a4a60b518bf24989d481468076e5d5982884626aed9faeb35b8576fcd223e1!
```