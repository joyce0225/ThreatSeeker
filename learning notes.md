# ThreatSeeker Tool Usage Guide - Joyce Leung

## Overview
`ThreatSeeker.py` is a specialized tool designed for detecting various types of security threats and suspicious activities in Windows environments by analyzing log files. This guide provides detailed usage instructions for each command available in the ThreatSeeker tool, helping users to effectively monitor and secure their systems.

### Available Commands and Their Use Cases

1. **Detect Registry Changes**
   - **Command:**
     ```
     --detect-registry-changes FILE
     ```
   - **Attack Type:** Tampering/Configuration Changes
   - **Usage:** This command analyzes the specified log file for unauthorized changes in the Windows Registry, which can indicate attempts to alter settings for malicious purposes.

2. **Detect Mimikatz Usage**
   - **Command:**
     ```
     --detect-mimikatz FILE1 (optional FILE2)
     ```
   - **Attack Type:** Credential Theft
   - **Usage:** Targets the identification of Mimikatz tool usage in log files, a common method for extracting credentials and compromising security.

3. **Detect Suspicious Executable**
   - **Command:**
     ```
     --detect-suspicious-executable FILE
     ```
   - **Attack Type:** Malware/Unauthorized Software Execution
   - **Usage:** Checks for the execution of unusual or flagged executables, which might be indicative of malware or unauthorized software activity.

4. **Detect Suspicious Download**
   - **Command:**
     ```
     --detect-suspicious-download FILE
     ```
   - **Attack Type:** Initial Infection Vector/Malware Download
   - **Usage:** Identifies downloads from dubious sources or of unusual file types, which could be a sign of a compromised system.

5. **Detect User Account Activity**
   - **Command:**
     ```
     --detect-user-account-activity FILE
     ```
   - **Attack Type:** Unauthorized Access/Internal Reconnaissance
   - **Usage:** Monitors for abnormal user account behaviors such as creation, deletion, or privilege modifications.

6. **Detect Malicious Executable**
   - **Command:**
     ```
     --detect-malicious-executable FILE1 FILE2
     ```
   - **Attack Type:** Malware Infection
   - **Usage:** Focuses on identifying known malicious executables based on their hash signatures.

7. **Detect SMB Brute Force**
   - **Command:**
     ```
     --detect-smb-bruteforce FILE1 (optional FILE2 FILE3)
     ```
   - **Attack Type:** Credential Brute Force/Network Service Attack
   - **Usage:** Analyzes for brute force attacks against SMB services, characterized by repeated login attempts.

8. **Detect RDP Brute Force**
   - **Command:**
     ```
     --detect-rdp-bruteforce FILE1 FILE2 (optional FILE3)
     ```
   - **Attack Type:** Credential Brute Force/Remote Service Attack
   - **Usage:** Searches for numerous login attempts on RDP, indicating potential brute force credential attacks.

9. **Detect WinRM Brute Force**
   - **Command:**
     ```
     --detect-winrm-bruteforce FILE
     ```
   - **Attack Type:** Credential Brute Force/Remote Management Service Attack
   - **Usage:** Identifies brute force attacks on WinRM, aiming to compromise remote management credentials.

10. **Detect Suspicious Services**
    - **Command:**
      ```
      --detect-suspicious-services FILE1 FILE2
      ```
    - **Attack Type:** Persistence/Malicious Service Installation
    - **Usage:** Looks for the installation of unauthorized services which could be used for malicious activities or persistence.

11. **Detect Pass-the-Hash (PTH) Attack**
    - **Command:**
      ```
      --detect-pth-attack FILE1 FILE2
      ```
    - **Attack Type:** Credential Theft/Reuse
    - **Usage:** Focuses on identifying PTH attacks, where a valid user's hash is used for authentication bypassing standard procedures.
   
### Example Command Usage
To use the commands, replace `<Path\To\Log.xml>` with the actual paths to the logs you wish to analyze. Optional files are enclosed in square brackets to indicate that they are not required for the command to function but will provide additional data for analysis if included.

Here's an example of using the SMB Brute Force detection command with the correct file order:
   python "C:\Users\USER\Desktop\ThreatSeeker\ThreatSeeker\threatseeker.py" --detect-smb-bruteforce "C:\Path\To\SMB\Security\Log.xml" "C:\Path\To\Optional\Security\Log.xml" "C:\Path\To\Optional\Sysmon\Log.xml"

## Getting Started
To use `ThreatSeeker.py`, follow these steps:
1. Ensure you have Python installed on your system.
2. Place the `ThreatSeeker.py` script in your desired directory.
3. Prepare your Windows log files for analysis.
4. Run the commands as per your specific threat detection needs.

## Conclusion
`ThreatSeeker.py` is a powerful tool for Windows security analysis. By utilizing its various commands, users can effectively monitor their systems for a wide range of security threats, ensuring better protection against unauthorized access and malicious activities.

For more information or support, please refer to the official documentation or contact the support team.
+++
