# Firewall Configuration Report

## Overview
This report documents the configuration and testing of basic firewall rules as part of the Cyber Security Internship Task 4.

## Environment
- **Operating System:** Windows 10/11  
- **Tool Used:** Windows Defender Firewall with Advanced Security  
- **Network:** Local LAN for testing

## Procedure
1. Accessed the firewall console using `wf.msc`.
2. Reviewed all existing inbound and outbound rules.
3. Added an inbound rule to block TCP traffic on port 23 (Telnet).
4. Tested the block using PowerShell:
   ```powershell
   Test-NetConnection <PC-IP> -Port 23
