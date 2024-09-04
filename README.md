Dell OS10 Switch Configuration Script
This repository contains a Python script designed to automate the execution of commands on Dell OS10 switches. The script connects to a list of switches, executes a specified command, and logs the output.

Features
Automated Command Execution: The script automates the process of connecting to each switch and running the write memory command.
Excel Integration: Device information (IP, username, password) is read from an Excel file, making it easy to manage and update the list of devices.
Error Handling: Basic error handling is included to manage failed connections or other issues.
Prerequisites
Before running the script, ensure you have the following installed:

Python 3.x
Required Python packages: pandas, netmiko, openpyxl (for reading Excel files)
You can install the necessary packages using pip:

sh
Copy code
pip install pandas netmiko openpyxl
Usage
Prepare the Excel File: Create an Excel file (devices.xlsx) with the following columns:

IP: The IP address of the switch.
Username: The username for SSH login.
Password: The password for SSH login.
Run the Script:

sh
Copy code
python switch_config_script.py
The script will read the list of devices from the Excel file, connect to each switch, execute the write memory command, and print the output.

Error Handling
The script will attempt to connect to each switch and will print an error message if the connection fails or if there are any issues during command execution.

Customization
Commands: You can modify the execute_command_on_switch function to execute different commands based on your needs.
Device Type: The script is configured for Dell OS10 switches (device_type: 'dell_os10'). If you're working with a different device type, update this value in the script.
Contribution
Contributions are welcome! Feel free to fork this repository, submit pull requests, or open issues for any bugs or feature requests.

License
This project is licensed under the MIT License. See the LICENSE file for details.
