# Firewall Configuration and Testing

## Objective
Configure and test basic firewall rules to allow or block network traffic on a Windows system (or Linux alternative).

## Steps Performed
1. **Opened Firewall Console**  
   - Pressed `Win + R`, typed `wf.msc` to open *Windows Defender Firewall with Advanced Security*.

2. **Listed Existing Rules**  
   - Checked *Inbound* and *Outbound* rules to understand the current configuration.

3. **Created a Block Rule**  
   - In **Inbound Rules → New Rule → Port**  
   - Selected **TCP**, specified **port 23 (Telnet)**.  
   - Chose **Block the connection** for all profiles (Domain, Private, Public).  
   - Named the rule `Block_Telnet`.

4. **Tested the Rule**  
   - Ran PowerShell command:
     ```powershell
     Test-NetConnection <PC-IP> -Port 23
     ```
   - Output showed `TcpTestSucceeded : False`, confirming the block.

5. **Removed the Test Rule**  
   - Deleted the `Block_Telnet` rule to restore the original state.

## Outcome
- Verified that inbound traffic on port 23 was successfully blocked.
- Gained practical understanding of firewall rules, inbound vs outbound filtering, and testing methods.

## Key Concepts
- **Firewall**: A security system that filters network traffic based on defined rules.
- **Inbound Rule**: Controls incoming traffic to the system.
- **Outbound Rule**: Controls outgoing traffic from the system.
- **Port 23 (Telnet)**: Often blocked due to insecure, unencrypted communication.

## Screenshots
## Rule Creation
<img width="532" height="714" alt="image" src="https://github.com/user-attachments/assets/69a599e6-8c96-47fb-b834-d62815241c0d" />

## Test-NetConnection
<img width="1470" height="760" alt="image" src="https://github.com/user-attachments/assets/5c73f743-f780-4291-99e1-c820f5acee3c" />


---
