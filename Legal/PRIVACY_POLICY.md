# Privacy Policy for AiroSync

**Effective Date:** October 8, 2026  
**Last Updated:** October 8, 2026  

This Privacy Policy applies to the **AiroSync** mobile applications, desktop applications, and associated web interfaces (collectively referred to as **"AiroSync"**, **"we"**, **"us"**, or **"our"**).

---

## 1. Summary of Our Privacy Philosophy

**We do not collect, store, sell, or monetize your personal files or private data.**  

AiroSync is engineered as a decentralized, local-network peer-to-peer file sharing and productivity utility. All file transfers, clipboard synchronization, media streaming, touchpad controls, and device commands pass directly between your paired devices over your private Local Area Network (Wi-Fi/LAN) using secure, encrypted protocols. **Your files, photos, videos, clipboard items, and audio never pass through or get stored on any cloud server.**

**Internet Usage Scope:**  
Our applications connect to the public Internet **strictly and exclusively for:**
1. **Remote App Configuration & Announcements:** Checking for software updates, version status, and service notices via our secure API endpoint.
2. **Voluntary User Feedback & Bug Reports:** Submitting user-initiated feedback and bug diagnostics directly to the developer when you choose to do so.
3. **Zero Third-Party Tracking:** AiroSync embeds **no** advertising networks, tracking trackers, Google Analytics, Firebase Analytics, or Sentry telemetry SDKs.

---

## 2. Information We Handle and How It Is Used

### A. Local File Transfers & Media Content (100% Offline / LAN)
* **Direct Peer-to-Peer Transfer:** Files, photos, videos, and documents you choose to send are transferred directly from device to device across your local Wi-Fi network.
* **Storage Location:** Transferred files are saved only on the receiving device in user-selected directories (such as the standard `Downloads` folder).
* **Zero Cloud Relay:** We do not operate intermediary cloud storage or relays to inspect, store, or process your files.

### B. Clipboard Synchronization (100% Offline / LAN)
* **Local Exchange:** When clipboard synchronization is explicitly enabled, text copied on one paired device is transferred directly to the other paired device over your local network.
* **No Cloud History:** Clipboard entries are never transmitted over the Internet, logged, or stored on remote servers.

### C. Microphone & Audio Streaming (100% Offline / LAN)
* **Real-Time LAN Streaming:** If you activate the optional Microphone or Audio Streaming features, live audio is encoded and streamed directly to your paired Windows PC via local network socket.
* **No Recording or Cloud Transmission:** Audio streams are purely peer-to-peer over the local network and are never saved, recorded, or uploaded to any external server.

### D. Device Discovery & Local Metadata (100% Offline / LAN)
* **Local Subnet Signaling:** To detect nearby devices on the same Wi-Fi, the apps broadcast and listen for local mDNS / SSDP discovery signals. This metadata remains strictly confined within your local Wi-Fi subnet.

### E. Version Checking & Remote Configuration (Internet Access)
* **Configuration & Status Checks:** The app periodically requests our secure configuration endpoint (`https://airosync-admin.asepsayyad007.in/api/v1/app-config`) to verify version compatibility and display maintenance alerts. No personal identifiers, files, or user profile records are transmitted or logged.

### F. Voluntary User Feedback & Bug Reports (Internet Access)
* **User-Initiated Submissions:** When you voluntarily submit feedback or report a bug through the app or WebUI (`/api/v1/feedback`), the text title, message body, optional reply email, and basic device specifications (e.g., OS version, browser type, device model) are securely transmitted to the developer to resolve reported issues.

---

## 3. Device Permissions & Technical Justifications

To provide high-speed local connectivity and optional features, AiroSync requests the following permissions:

### Android Permissions
* **`INTERNET` & `ACCESS_NETWORK_STATE`:**  
  Required to establish local TCP/HTTP/WebSocket sockets over your Wi-Fi network, and used for anonymous analytics, remote configuration checks, and voluntary user feedback submissions.
* **`NEARBY_WIFI_DEVICES` (Android 13+ / API 33+):**  
  Used solely to detect nearby AiroSync PC servers on your Wi-Fi network (scoped with `neverForLocation`). We **do not** track your physical location.
* **`ACCESS_COARSE_LOCATION` & `ACCESS_FINE_LOCATION` (Android 12 and below only):**  
  Required strictly by legacy Android system architecture for Wi-Fi SSID scanning. Not used for location tracking.
* **`CHANGE_WIFI_MULTICAST_STATE` & `ACCESS_WIFI_STATE`:**  
  Required for local mDNS/multicast packet exchange so paired devices can auto-discover each other.
* **Storage & File Access (Legacy Android ≤ 12 / API ≤ 32):**  
  `READ_EXTERNAL_STORAGE` and `WRITE_EXTERNAL_STORAGE` are requested strictly on legacy Android versions to read selected files and save received downloads. On Android 13+ (API 33+), AiroSync uses the modern system Photo Picker and Storage Access Framework (SAF) without requesting broad media permissions.
* **`RECORD_AUDIO` & `MODIFY_AUDIO_SETTINGS` (Optional):**  
  Requested only when using the optional Microphone Streaming feature to stream local audio directly to your paired PC over LAN. Audio is never recorded or uploaded to the cloud.
* **`POST_NOTIFICATIONS` & `FOREGROUND_SERVICE` (`MEDIA_PLAYBACK` & `MICROPHONE`):**  
  Required to display download notifications and maintain active media playback and live microphone streaming sessions in the background without termination by system battery managers.

### Windows Permissions
* **Local Network / Firewall Access:**  
  Allows the desktop service to open a listening port (HTTP/WebSocket) bound to the local network interface for receiving files and control commands.
* **File System Access:**  
  Allows reading files selected by you for sending and writing incoming transferred files to your designated download directory.
* **Public Internet Access:**  
  Used solely for checking GitHub releases or cloud configuration for application updates, anonymous telemetry, and submitting user feedback.

---

## 4. Scope of Internet Access

AiroSync uses public Internet access **only for the following clear and limited purposes**:

1. **App Updates & Security Notices:** Checking whether newer versions are available via GitHub Releases and synchronizing active announcement banners from `airosync-admin.asepsayyad007.in`.
2. **Voluntary User Support:** Transmitting user-submitted bug reports and feedback text to help improve the software.

**What We NEVER Do:**
* We **never** upload your files, photos, videos, or documents to the internet.
* We **never** transmit your clipboard contents over the internet.
* We **never** stream your microphone audio or screencasts outside your local Wi-Fi.
* We **never** sell, rent, or trade any user information to third-party advertisers or data brokers.
* We **never** bundle third-party ad networks or tracking SDKs.

---

## 5. Security & Encryption

* **Local Transport Security:** Device-to-device communications utilize TLS/HTTPS and WebSocket Secure (WSS).
* **PIN & Pairing Verification:** Connection requests require manual user confirmation or PIN verification to protect against unauthorized access on shared networks.
* **Cloud API Security:** All telemetry, configuration checks, and feedback submissions communicate over TLS 1.3 encrypted HTTPS.

---

## 6. Children's Privacy (COPPA & GDPR Compliance)

AiroSync does not knowingly collect, store, or solicit personal information from children under the age of 13 (or under 16 in the European Union). Because no personal user information is harvested, the service complies with COPPA and GDPR regulations.

---

## 7. Data Retention and Deletion

* **Zero Cloud User Files:** Because all user content remains strictly on your local devices, there is no remote server file data to delete.
* **Feedback Data Retention:** Voluntarily submitted feedback reports are retained temporarily in the developer's console to triage and resolve reported bugs, after which resolved reports are deleted.
* **Local Data Removal:** Uninstalling the application removes all local configuration files, session logs, and pairing keys.

---

## 8. Changes to This Privacy Policy

We may update this Privacy Policy periodically to reflect technical enhancements, operating system requirement changes, or legal obligations. Any updates will be published with a revised "Last Updated" date at the top of this document.

---

## 9. Contact Information

If you have questions, feedback, or concerns regarding this Privacy Policy or the security of AiroSync, please contact:

* **Developer:** Asep Sayyad
* **Project:** AiroSync
* **Official Privacy Website:** [https://airosync.asepsayyad007.in/privacy/](https://airosync.asepsayyad007.in/privacy/)
* **GitHub Repository:** [https://github.com/asepsayyad007/AiroSync-Release](https://github.com/asepsayyad007/AiroSync-Release)
* **Email:** [asepsayyad@gmail.com](mailto:asepsayyad@gmail.com)
