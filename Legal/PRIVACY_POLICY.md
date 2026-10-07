# Privacy Policy for AiroSync

**Effective Date:** October 7, 2026  
**Last Updated:** October 7, 2026  

This Privacy Policy applies to the **AiroSync** mobile applications, desktop applications, and associated local web interfaces (collectively referred to as **"AiroSync"**, **"we"**, **"us"**, or **"our"**).

---

## 1. Summary of Our Privacy Philosophy

**We do not collect, store, sell, or monetize your personal data.**  
AiroSync is designed from the ground up as a decentralized, local-network file sharing and device synchronization utility. All file transfers, clipboard data, and remote control commands pass directly between your paired devices over your private Local Area Network (Wi-Fi/LAN) using secure, encrypted peer-to-peer protocols. Your files and data are never sent to external cloud servers.

---

## 2. Information We Handle and How It Is Used

### A. File Transfers & Data Content
* **Files & Media:** Files, photos, videos, and documents you choose to send are transferred directly from device to device over your local Wi-Fi network.
* **Storage Location:** Transferred files are stored only on the receiving device in user-selected directories (such as the standard `Downloads` folder).
* **No Cloud Relay:** We do not operate intermediary cloud servers to store, index, inspect, or process the files you transfer.

### B. Clipboard Synchronization
* **Clipboard Content:** When clipboard synchronization is explicitly enabled by you, text copied on one paired device is transferred directly to the other paired device over your local network.
* **No Cloud History:** Clipboard entries are not logged or stored on any remote server.

### C. Microphone & Audio Streaming (Optional Feature)
* **Real-Time LAN Streaming:** If you activate the optional Microphone Streaming feature, live audio captured by your mobile device's microphone is encoded and streamed directly to your paired Windows PC via local network socket.
* **No Audio Recording or Cloud Transmission:** The audio stream is purely peer-to-peer over the local network and is never saved, uploaded, analyzed, or sent to any external server.

### D. Device Discovery & Network Metadata
* **Local IP & Hostnames:** To locate and pair devices on the same Wi-Fi network, the applications broadcast and listen for local mDNS / SSDP discovery signals. This metadata remains strictly within your local subnet and is never reported to external servers.

---

## 3. Device Permissions & Technical Justifications

To provide local peer-to-peer connectivity, AiroSync requests the following permissions:

### Android Permissions
* **`NEARBY_WIFI_DEVICES` (Android 13+ / API 33+):**  
  Used solely to detect nearby AiroSync PC servers on your Wi-Fi network. Scoped with `neverForLocation` flag; we **do not** use this to derive your physical location.
* **`ACCESS_COARSE_LOCATION` & `ACCESS_FINE_LOCATION` (Android 12 and below only):**  
  Required by Android system architecture for legacy Wi-Fi network and SSID scanning. We do not track, log, or share your physical location.
* **`CHANGE_WIFI_MULTICAST_STATE` & `ACCESS_WIFI_STATE`:**  
  Required for local mDNS/multicast packet exchange so paired devices can auto-discover each other without manual IP configuration.
* **`INTERNET` & `ACCESS_NETWORK_STATE`:**  
  Required to establish local TCP/HTTP/WebSocket sockets over your Wi-Fi network. Does not send personal data over the public internet.
* **`READ_MEDIA_IMAGES` / `READ_MEDIA_VIDEO` / `READ_MEDIA_AUDIO` / Storage Permissions:**  
  Requested solely when you pick files to share or when saving incoming files to your device storage.
* **`RECORD_AUDIO` & `MODIFY_AUDIO_SETTINGS` (Optional):**  
  Requested only when using the optional Microphone Streaming feature to stream local audio to your PC.
* **`POST_NOTIFICATIONS` & `FOREGROUND_SERVICE`:**  
  Required to maintain active file transfers in the background and show progress notifications so transfers are not terminated prematurely by system battery managers.

### Windows Permissions
* **Local Network / Firewall Access:**  
  Allows the local desktop service to open a listening port (HTTP/WebSocket) bound to the local network interface for receiving files and control commands.
* **File System Access:**  
  Allows reading files selected by you for sending and writing incoming transferred files to your designated download directory.
* **System Tray & Desktop Notifications:**  
  Provides transfer alerts and quick access to connection controls.

---

## 4. Third-Party Services and Analytics

* **No Analytics SDKs:** AiroSync does not integrate third-party tracking, ad networks, behavioral tracking, or analytics SDKs (such as Google Analytics or Facebook SDK).
* **No Advertising:** The applications contain no third-party advertisements.
* **Software Updates:** Desktop or Android update checks may contact public GitHub releases (`https://github.com/asepsayyad007/AiroSync-Release`) to verify whether a newer application version is available. These checks transmit only standard HTTP headers and receive version metadata.

---

## 5. Security & Encryption

* **Local Encryption:** Device-to-device communications utilize TLS/HTTPS and WebSocket Secure (WSS) using self-signed or authenticated certificates generated for your local session.
* **PIN / Pairing Verification:** Device connection requests require user confirmation or PIN verification to ensure unauthorized devices on the local network cannot send files without consent.

---

## 6. Children's Privacy (COPPA & GDPR Compliance)

AiroSync does not knowingly collect, store, or solicit personal information from children under the age of 13 (or under 16 in the European Union). Because no personal information is collected by our software, the service complies with the Children's Online Privacy Protection Act (COPPA) and the General Data Protection Regulation (GDPR).

---

## 7. Data Retention and Deletion

* **Zero Cloud Data:** Because all data remains strictly on your local devices, there is no remote server data to delete.
* **Local Data Removal:** Uninstalling the application or clearing application cache removes all local configurations, session logs, and pairing keys. Transferred files remain in your device's standard storage directory until you delete them.

---

## 8. Changes to This Privacy Policy

We may update this Privacy Policy from time to time to reflect feature enhancements, operating system requirement changes, or legal obligations. Any updates will be published with a revised "Last Updated" date at the top of this document and will be made available in our public release repository.

---

## 9. Contact Information

If you have questions, feedback, or concerns regarding this Privacy Policy or the security of AiroSync, please contact:

* **Developer:** Asep Sayyad
* **Project:** AiroSync
* **GitHub Repository:** [https://github.com/asepsayyad007/AiroSync-Release](https://github.com/asepsayyad007/AiroSync-Release)
* **Email:** [asepsayyad@gmail.com](mailto:asepsayyad@gmail.com)
