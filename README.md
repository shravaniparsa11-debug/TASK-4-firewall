# Task 4: Setup and Use a Firewall

## Objective
To understand and test basic firewall and network traffic filtering concepts.

## Tool Used
- Termux
- Nmap 7.99
- Netcat

## Environment
Android phone using Termux.

## Step 1: Nmap Installation

Nmap was installed successfully in Termux.

Command:

    pkg install nmap

## Step 2: Verify Nmap

Command:

    nmap --version

Nmap version 7.99 was successfully verified.

## Step 3: Localhost Scan

Command:

    nmap localhost

Result:
The localhost host was up and the scanned common TCP ports were closed.

## Step 4: Port 23 Test

Command:

    nmap -p 23 localhost

Result:
TCP port 23 was found closed/not accepting connections.

A second test was performed using:

    nc -vz 127.0.0.1 23

## Important Limitation

This experiment was performed on an Android phone using unprivileged Termux.
UFW was not used because Termux does not directly manage the Android
system firewall.

Therefore, the port 23 result demonstrates port availability/connection
testing and should not be interpreted as proof of an actual UFW firewall
block.

## Screenshots

### Nmap Version
![Nmap Version](screenshots/nmap-version.png)

### Localhost Scan
![Localhost Scan](screenshots/localhost-scan.png)

### Port 23 Scan
![Port 23 Scan](screenshots/port23-scan.png)

### Port 23 Test
![Port 23 Test](screenshots/port23-test.png)

## Conclusion

The task provided practical experience with network port scanning and
connection testing using Termux. Port 23 was tested locally and was found
to be closed. The experiment also demonstrated the limitation of using
Termux on Android for managing the device's actual firewall.
