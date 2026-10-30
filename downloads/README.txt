# REXVA CBT V1.3.0
## Computer-Based Testing System

**Application:** REXVA CBT  
**Version:** 1.3.0  
**Platform:** Windows  
**Connectivity:** Offline and local wireless (Wi-Fi) network, subject to network configuration  
**Default local address:** `http://localhost:5000/login`

---

## 1. About REXVA CBT

REXVA CBT is a computer-based testing application designed to support the administration of computer-based examinations.

The application runs on a Windows computer and may provide access to other computers over a local network when the host, firewall, and network are configured correctly.

## 2. System Requirements

- A Windows computer to host the application.
- The REXVA CBT application: `REXVA CBT.exe`.
- A web browser for accessing the examination login page.
- A Wi-Fi router or wireless access point for wireless connections.
- Student computers connected to the same accessible local network.
- Sufficient storage space for application files, examination records, and backups.

## 3. Starting REXVA CBT

1. Open the folder containing REXVA CBT.
2. Double-click `REXVA CBT.exe`.
3. Wait for the application to start.
4. On the host computer, open a web browser.
5. Visit:

   `http://localhost:5000/login`

Keep the application running while students are taking examinations.

**Application location on this computer:**

`C:\Users\HomePC\Desktop\REXVA_CBT\REXVA CBT.exe`

## 4. Wireless Wi-Fi Connectivity

REXVA CBT can be accessed from other computers over Wi-Fi if the application is configured to accept local network connections.

### Step 1: Start the host computer

Turn on the computer running REXVA CBT and launch the application.

### Step 2: Connect to Wi-Fi

Connect the host computer and all student computers to the same Wi-Fi network.

Avoid guest networks that prevent connected devices from communicating with one another.

### Step 3: Find the host computer's IP address

On the host computer:

1. Press `Windows + R`.
2. Type `cmd`.
3. Press Enter.
4. Run the following command:

   ```cmd
   ipconfig
   ```

5. Find **Wireless LAN adapter Wi-Fi**.
6. Locate the **IPv4 Address**.

Example:

`192.168.1.100`

Use the actual address displayed on the host computer; the address above is only an example.

### Step 4: Connect student computers

On each student computer, open a web browser and enter the host computer's IP address followed by port `5000`.

Example:

`http://192.168.1.100:5000/login`

Replace `192.168.1.100` with the host computer's actual IPv4 address.

### Step 5: Test the connection

Before an examination:

- Confirm that the login page opens on the host computer.
- Confirm that it opens on at least one student computer.
- Verify that authorized students can log in.
- Confirm that the Wi-Fi connection remains stable.
- Test the setup with the actual number of computers expected during the examination.

### Wireless connection requirements

- The host computer must remain powered on.
- REXVA CBT must remain running.
- Windows Firewall must permit the required local network traffic.
- The application must listen on a network interface accessible to student computers.
- The router must allow communication between wireless clients.
- The host computer should have a stable local IP address.

An internet connection is not necessarily required if the application and all required resources operate locally.

## 5. Offline Operation

REXVA CBT is intended for local use. If the installed version operates entirely offline, examinations can be administered without relying on an external website.

However, offline operation and wireless operation are different:

- **Offline:** The system does not need internet access for supported local functions.
- **Wireless:** Student computers connect to the host through a local Wi-Fi network.

A Wi-Fi router can provide local connectivity even when it has no internet connection, provided the network and application are configured appropriately.

## 6. Examination Preparation

Before starting an examination:

1. Start the host computer.
2. Launch REXVA CBT.
3. Confirm that the login page is accessible.
4. Check that student accounts and examination settings are correct.
5. Connect student computers to the correct Wi-Fi network.
6. Test student login and examination access.
7. Confirm that the application can save examination records.
8. Ensure the host computer has reliable power.
9. Keep a recent backup of important data.

Do not use a live examination as the first test of a new network or application configuration.

## 7. Data Protection and Backups

Examination records and databases may be stored locally, depending on the installed version.

To protect examination data:

- Back up the application's data and database regularly.
- Store backup copies in a separate, secure location.
- Restrict access to the host computer and application folder.
- Do not delete unknown application or database files.
- Do not overwrite the working installation when updating the software.
- Test a backup restoration procedure before relying on it.

**Important:** The exact database location and backup method depend on the application's implementation. Identify the actual data files before moving or replacing anything.

## 8. Troubleshooting

### The application does not open

- Check that `REXVA CBT.exe` exists in the installation folder.
- Restart the application.
- Check for Windows security warnings or missing dependencies.
- Do not delete application files to resolve an error without first making a backup.

### The login page does not open on the host computer

Try:

`http://localhost:5000/login`

Confirm that the application is running and that port `5000` is available to the application.

### Student computers cannot connect

- Confirm that the host and students are on the same Wi-Fi network.
- Check the host's current IPv4 address using `ipconfig`.
- Use the host IP address instead of `localhost` on student computers.
- Check Windows Firewall rules.
- Check whether the router has client isolation enabled.
- Verify that the application accepts connections from other computers.

### The page opens on the host but not on student computers

The application may be listening only on the local computer, or the firewall/router may be blocking local connections. Check the application's network configuration before changing firewall settings.

### The host IP address changes

The router may assign a different IP address after a restart. Update the address used by student computers or configure a suitable DHCP reservation on the router.

### Examination records appear to be missing

Stop making changes to the application and database. Check the configured data location and available backups before attempting recovery. Avoid reinstalling or overwriting the application until the records have been protected.

## 9. Security Guidelines

- Use a trusted Wi-Fi network.
- Allow access only to authorized users and computers.
- Do not expose port `5000` directly to the public internet.
- Do not disable Windows Firewall entirely.
- Do not publish databases, student information, passwords, or confidential examination files in a public repository.
- Keep secure backups of important examination records.

## 10. Version Information

**Product:** REXVA CBT  
**Version:** 1.3.0  
**Application type:** Windows executable  
**Local login address:** `http://localhost:5000/login`  
**Network access:** Local Wi-Fi access, subject to configuration

### Features to verify in the installed version

The following capabilities should be confirmed against the actual installation before being advertised as supported:

- Automatic answer saving.
- Recovery after a crash or power failure.
- Examination timer recovery.
- Automatic handling of tab switching or leaving fullscreen.
- Resetting an examination attempt after a violation.
- Centralized backup and restoration.

## 11. Maintenance

Before updating REXVA CBT:

1. Close the application safely.
2. Back up the database and important data files.
3. Keep a copy of the current working version.
4. Test the update with sample examination data.
5. Confirm that student records and results remain intact.

Do not replace the production database with a blank database when installing an update.

---

**REXVA CBT V1.3.0**  
*Reliable examination administration through local computer and wireless network access.*

