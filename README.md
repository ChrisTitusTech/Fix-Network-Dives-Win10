# Fix-Network-Dives-Win10

Network Drives can be a bit flaky when working in Office documents. Sometimes they will have issues saving directly to them because of UAC issues and them spereating users from the login network drives. 

Edit the following key

```
HKEY_Local_Machine\Software\Microsoft\Windows\CurrentVersion\Policies\Systems
```

Add a New DWORD (32-Bit Value)

```
EnableLinkedConnections
```

Make the Value `1`

This will fix any issues you have with saving to network drives.

Alternative solution would be to avoid the network drive altogether and just use the full UNC path. 
