# Google Play Console: Data Safety & Policy Declarations Guide

**Last Updated:** October 8, 2026

This guide provides exact, step-by-step answers for completing the **Data safety** and **App content** declarations in the Google Play Console for **AiroSync**.

---

## 1. Data Safety Questionnaire Summary

| Question in Play Console | Required Answer | Technical Justification |
| :--- | :--- | :--- |
| **Does your app collect or share any of the required user data types?** | **Yes** *(Only for anonymous analytics & voluntary feedback)* | The app accesses the Internet strictly for anonymous technical diagnostics/analytics and voluntary feedback reports. Personal files and data remain 100% peer-to-peer over local Wi-Fi. |
| **Is all user data collected encrypted in transit?** | **Yes** | All analytics checks, remote configurations, and feedback calls use HTTPS / TLS 1.3 encryption. |
| **Do you provide a way for users to request data deletion?** | **Yes** | Users can request deletion of submitted feedback by contacting the developer via email. |

---

## 2. Data Types Breakdown for Google Play Console

### A. App Info & Performance (Analytics & Diagnostics)
* **Data Type:** Crash logs, Diagnostics, App performance data.
* **Is this data collected?** **Yes**
* **Is this data shared?** **No** (Never shared with third parties or advertisers).
* **Is it processed ephemerally?** **Yes**
* **Is this data required or optional?** Required for app reliability.
* **Why is this user data collected?**
  * **Analytics** (to identify app performance and OS compatibility issues).
  * **App functionality** (version verification and maintenance notice fetching).

### B. User Feedback / Messages (Voluntary)
* **Data Type:** Other in-app messages / User feedback.
* **Is this data collected?** **Yes** (Only when voluntarily submitted by user via Report Bug / Feedback).
* **Is this data shared?** **No**.
* **Is it linked to user identity?** **No** (Anonymous unless user optionally inputs email).
* **Why is this data collected?** **Developer communications & Customer support**.

### C. Data Types NOT Collected (Mark as "No")
* **Files and Documents:** **No / Not Collected** (Transfers are strictly peer-to-peer over local LAN).
* **Photos and Videos:** **No / Not Collected** (Local LAN transfers only).
* **Audio / Voice Recordings:** **No / Not Collected** (Microphone streaming is strictly local LAN peer-to-peer; no audio is recorded or uploaded).
* **Location:** **No / Not Collected** (`neverForLocation` flag enforced on Android 13+).
* **Contacts / Personal Info:** **No / Not Collected**.
* **Financial Info:** **No / Not Collected**.

---

## 3. Permissions Declarations in Play Console

### A. Location / Nearby Wi-Fi Devices
* **Android 13+ (API 33+):**  
  Uses `NEARBY_WIFI_DEVICES` with `neverForLocation`.  
  *In Play Console declaration:* Confirm the app uses Nearby Wi-Fi Devices solely to find nearby local Wi-Fi devices for peer-to-peer file transfer and does **not** derive physical location.
* **Android 12 and below (API ≤ 32):**  
  Uses `ACCESS_COARSE_LOCATION` and `ACCESS_FINE_LOCATION` with `maxSdkVersion="32"`.  
  *Declaration note:* Required by older Android operating systems to scan local Wi-Fi SSIDs for device discovery.

### B. Microphone (`RECORD_AUDIO`)
* **Declaration:**  
  *Audio streaming feature:* The microphone is used exclusively for live streaming to the paired Windows PC over the local network (Mic Streaming feature). Audio is not recorded, saved, or uploaded to any server.

### C. Foreground Service Declarations (Android 14+ / API 34+)
* **`FOREGROUND_SERVICE_MEDIA_PLAYBACK`:**  
  *Justification in Play Console:* Required for continuous playback of audio and streaming PC audio to the device over the local network when the app is running in the background or the screen is turned off. A standard Android media notification with playback controls is displayed to the user.
* **`FOREGROUND_SERVICE_MICROPHONE`:**  
  *Justification in Play Console:* Required for the user-initiated live microphone streaming feature, allowing real-time microphone audio transmission to the paired PC over the local network without being killed when the user switches apps or locks the screen. A persistent foreground notification is displayed while active.
* **`FOREGROUND_SERVICE_DATA_SYNC`:**  
  *Justification in Play Console:* Required for user-initiated peer-to-peer file transfers between the Android device and paired Windows PC over local Wi-Fi (`FileTransferService`). It ensures that multi-gigabyte files (videos, photos, documents) transfer reliably without being terminated by OS battery optimization when the app is backgrounded or screen is turned off. An ongoing foreground notification displays real-time transfer progress, current speed, file name, and a cancel action.

### D. Storage & Modern Android Scoped Storage
* **Android 13+ (API 33+):**  
  The app does **not** request `READ_MEDIA_IMAGES`, `READ_MEDIA_VIDEO`, or `READ_MEDIA_AUDIO`. Transfers use the system Photo Picker and Storage Access Framework (SAF), maintaining strict user privacy.
* **Android 12 and below (API ≤ 32):**  
  `READ_EXTERNAL_STORAGE` is scoped with `maxSdkVersion="32"`, and `WRITE_EXTERNAL_STORAGE` is scoped with `maxSdkVersion="29"` for legacy file picker support.

---

## 4. Mandatory Play Console Links

* **Privacy Policy URL:**  
  `https://airosync.asepsayyad007.in/privacy/`  
  Paste into: **Play Console > Policy and Programs > App content > Privacy policy**
* **Target Audience:**  
  Ages 13 and older (General Audience / Productivity / Tools).
* **News Apps, Financial Features, COVID-19:**  
  Select **No** for all specialized government/financial categories.
* **Ads:**  
  Select **No, my app does not contain ads**.
