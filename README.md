# FirewallConfig
- Windows Defender Firewall (built-in) - Cisco Umbrella / OpenDNS (free account) - PowerShell (for scripting) - Task Scheduler (to run scripts at certain times) - GlassWire (optional tool to see traffic visually)
## Project Overview

This project shows how I set up a firewall and parental controls on my own Windows computer. I used the built-in Windows Defender Firewall and Cisco Umbrella (which is also called OpenDNS) to block dangerous ports, websites, and track internet activity. I also added time-based rules and some tools to monitor traffic.

Everything was done without using a virtual machine.

---

## Tools Used

- Windows Defender Firewall (built-in)
- Cisco Umbrella / OpenDNS (free account)
- PowerShell (for scripting)
- Task Scheduler (to run scripts at certain times)
- GlassWire (optional tool to see traffic visually)

---

## Features I Added

### 1. Windows Firewall Rules

- Blocked dangerous ports like:
  - Port 21 (FTP)
  - Port 23 (Telnet)
  - Ports 135–139 (NetBIOS)
  - Port 445 (SMB)
- Blocked some outbound traffic
- Blocked specific IP addresses using custom rules

### 2. Parental Controls with Cisco Umbrella

- I changed my DNS to Cisco's OpenDNS servers:
  - 208.67.222.222
  - 208.67.220.220
- Then I signed up at Cisco Umbrella and added my public IP
- I used the dashboard to block:
  - Adult content
  - Gambling
  - Social media
  - Streaming websites
- It also lets me see logs of what was blocked

### 3. Time-Based Blocking

- I made PowerShell scripts that add or remove websites from the hosts file
- Used Task Scheduler to block websites at night (like YouTube after 9 PM)
- Unblocked them again in the morning

### 4. Logging and Monitoring

- Turned on firewall logging
- Found logs in:
  - C:\Windows\System32\LogFiles\Firewall\pfirewall.log
- Used Event Viewer to look at blocked attempts
- Installed GlassWire to see graphs and real-time traffic (optional)

---

## Screenshots (Optional)

You can include:
- Windows Firewall settings
- Cisco Umbrella dashboard showing blocked categories
- GlassWire dashboard view (if used)

---

## How To Do This Project

1. Open the firewall settings with `wf.msc`
2. Add inbound and outbound rules to block ports
3. Change your DNS settings to OpenDNS in your network adapter
4. Go to Cisco Umbrella, sign up, and register your network
5. Use the dashboard to choose what categories to block
6. Write scripts to block sites with PowerShell
7. Use Task Scheduler to make the scripts run on a schedule
8. Turn on logging and use Event Viewer or GlassWire to see results

---

## What I Learned

- How to make custom firewall rules
- How DNS filtering works with OpenDNS
- How to block websites and ports
- How to monitor and log network activity
- How to schedule things using PowerShell and Task Scheduler

---

## Project Folder Structure

.
├── README.md
├── images/
│ ├── firewall-rules.png
│ ├── opendns-dashboard.png
│ └── glasswire.png
├── scripts/
│ ├── block-youtube.ps1
│ └── unblock-youtube.ps1

yaml
Copy
Edit

---

## Future Ideas

- Add more IPs to block using aliases
- Try using AppLocker to stop apps from running
- Log everything to an external tool like Wazuh

![Screenshot 2025-07-07 170120](https://github.com/user-attachments/assets/fcc11a30-6254-48ae-9974-cc98e0664e05)
![Screenshot 2025-07-07 165812](https://github.com/user-attachments/assets/56bd23d6-0fc1-4244-a2f5-f2a74a1ded9c)
![Screenshot 2025-07-07 165748](https://github.com/user-attachments/assets/b43c121d-582f-4547-9e35-82b60dc0c93c)
![Screenshot 2025-07-07 165651](https://github.com/user-attachments/assets/5ece59ef-b5c2-4f2e-b0db-9badf2f82cca)
![Screenshot 2025-07-07 165614](https://github.com/user-attachments/assets/1c5c0b77-30a6-4639-aa5b-810fe06d520a)
![Screenshot 2025-07-07 165338](https://github.com/user-attachments/assets/926527ff-39e7-4fa7-ab6f-077f83972ea1)
![Screenshot 2025-07-07 164355](https://github.com/user-attachments/assets/c988257e-756a-4409-bb9e-3f8df2f8238c)
![Screenshot 2025-07-07 164308](https://github.com/user-attachments/assets/58852529-d9ce-4327-947c-cf27bec9a234)
![Screenshot 2025-07-07 164236](https://github.com/user-attachments/assets/27792c44-4fb2-4726-9b1f-9a64507e95e6)
![Screenshot 2025-07-07 164218](https://github.com/user-attachments/assets/3dbe5b55-50d0-431b-89f4-ea1a96bc3ec5)
