---

## 📦 Easy Installation (Standalone Executables)
Standalone binaries are available for users who want to run **LOTL-LAN** without a full Python environment.

1. **Prerequisite**: You **must** have TShark installed on your machine for the sniffer to work:
   - **Windows**: [Download Wireshark](https://www.wireshark.org/download.html) (includes TShark).
   - **Linux**: `sudo apt install tshark`
2. **Download the Binary**: Go to the [Releases](https://github.com/YOUR_USERNAME/lotl-lan/releases) page.
3. **Run**:
   - **Linux**: `sudo ./lotl-lan-ubuntu`
   - **Windows**: Run `lotl-lan-windows.exe` as **Administrator**.

---

## 🛡️ Security & Analyst Notes

### 1. Elevated Privileges Required
Passive network sniffing requires "Promiscuous Mode" access to your network interface.
* **Linux**: You must use `sudo` to allow the internal `PyShark` engine to bind to the interface.
* **Windows**: Running as Administrator is required to access the Npcap/WinPcap driver.

### 2. Antivirus & LOTL Flagging
Because this tool is named **LOTL-LAN** and performs network sniffing, it may be flagged by EDR or Antivirus software as a "Potentially Unwanted Application" (PUA).
* **Code Integrity**: This project is open-source. We encourage security analysts to audit the code and build their own binaries using the instructions in the `Development` section.

### 3. TShark Pathing
If the executable cannot find TShark, ensure it is added to your system's `PATH`. On Windows, the default path is usually `C:\Program Files\Wireshark`.

---

## ⚖️ Disclaimer
**For Authorized Security Auditing Only.** LOTL-LAN is designed for internal network threat hunting. By using this software, you agree:
* You have explicit permission to monitor the network traffic you are sniffing.
* The author is not responsible for any misuse, legal consequences, or network instability caused by this tool.
* This tool is provided "as is" with no warranty.
