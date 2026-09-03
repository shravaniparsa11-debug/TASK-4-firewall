# Task 4: Setup and Use a Firewall

## Objective
To understand and test basic firewall and network traffic filtering concepts.

## Tool Used
- Termux
- Nmap 7.99
- Netcat

## Environment
Android phone using Termux.

## Nmap Installation

Nmap was installed successfully in Termux.

Command:

    pkg install nmap

## Verify Nmap

Command:

    nmap --version

Nmap version 7.99 was successfully verified.

## Localhost Scan

Command:

    nmap localhost

Result:
The localhost host was up and the scanned common TCP ports were closed.

## Port 23 Test

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

## Conclusion

The task provided practical experience with network port scanning and
connection testing using Termux. Port 23 was tested locally and was found
to be closed. The experiment also demonstrated the limitation of using
Termux on Android for managing the device's actual firewall.

