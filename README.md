# PRODIGY_CS_04
# simple_Keylogger
This is a simple keylogger implemented in Python, designed to capture keystrokes on a Windows machine using the ctypes library to interact with the Windows API (user32.dll). The keystrokes are logged in a text file (keylog.txt).

Features
Keystroke Logging: Logs standard characters (A-Z, 0-9) and special keys such as Shift, Backspace, Tab, and Enter.
Windows API Integration: Uses the GetAsyncKeyState function from user32.dll to capture keypresses.
Logs to a File: Each keypress is immediately written to keylog.txt in append mode to ensure data is not lost.
Requirements
Python 3.x
Windows OS (This script uses the Windows API, so it only runs on Windows)
How It Works
Keystroke Capture: The script continuously checks for keypresses using GetAsyncKeyState(). When a key is pressed, its value is passed to the log_keystroke() function for logging.
Special Keys: Common special keys such as Shift, Space, Enter, and Backspace are logged with readable labels like [SHIFT], [SPACE], [ENTER], etc.
Log File: The keystrokes are logged into a file named keylog.txt in append mode. This ensures that new logs are added without overwriting previous logs.
Loop with Delay: A small delay of 0.01 seconds is added in the main loop to reduce CPU usage.
Usage
Setup
Install Python: Ensure that Python is installed on your system. You can download it from the official Python website.

Create the Script: Save the Python code into a file, for example, keylogger.py.

Run the Script: Open a terminal or command prompt in the directory where your script is saved and run the Python script.

Log File: The logged keystrokes will be saved in keylog.txt in the same directory as the script.

Example Output
The log file will look something like this:

css
Copy code
aB[SHIFT]C[ENTER]
1[BACKSPACE]2
[TAB]
Important Notes
Legal Disclaimer: Keyloggers can be used for malicious purposes. Monitoring someone's computer without permission is illegal. Use this script only for ethical and educational purposes. Always ensure you have proper consent before using this tool.
Windows Compatibility: This script uses the GetAsyncKeyState() function from user32.dll, which is specific to Windows. It will not work on non-Windows platforms.
Performance: The small delay in the main loop helps reduce CPU usage, but this can be adjusted based on your requirements.
Customization
Log File Location: You can change the log file name or path by modifying the line that specifies where the file should be opened.

Logging Special Keys: You can add more special keys by editing the function that handles key logging. Additional virtual key codes can be found in Microsoft's Virtual Key Code documentation.
