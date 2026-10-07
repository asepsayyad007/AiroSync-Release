# Google Play Console: Data Safety & Policy Declarations Guide

This guide provides exact, step-by-step answers for completing the **Data safety** and **App content** declarations in the Google Play Console for **AiroSync**.

---

## 1. Data Safety Questionnaire Summary

| Question in Play Console | Required Answer | Technical Justification |
| :--- | :--- | :--- |
| **Does your app collect or share any of the required user data types?** | **No** *(or "Yes" only for local files if asked about ephemeral handling)* | AiroSync does not collect user data to any external server. All transfers are peer-to-peer over LAN. |
| **Is all user data collected encrypted in transit?** | **Yes** | Local communication uses TLS / HTTPS / WSS. |
| **Do you provide a way for users to request data deletion?** | **Yes / Not applicable (No cloud data)** | All data is stored locally on device. Users can clear storage or delete files at any time. |

> **Note on "Data Collection" definition by Google Play:**  
> Google defines "Collected" as transmitting data off the user's device to a server or external entity. Because AiroSync transmits files directly between the user's two local devices on the same Wi-Fi subnet without any cloud intermediary or developer server, it qualifies as **No data collected off-device**.

---

## 2. Permissions Declarations in Play Console

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

### C. Foreground Service (`FOREGROUND_SERVICE` & `FOREGROUND_SERVICE_DATA_SYNC` / `MEDIA_PLAYBACK`)
* **Declaration:**  
  Foreground services are used to maintain active peer-to-peer file transfer tasks and local audio streaming sessions without being prematurely killed by system memory management or battery optimization.

---

## 3. Mandatory Play Console Links

* **Privacy Policy URL:**  
  Host `Legal/privacy-policy.html` on GitHub Pages or your web server, then paste the URL into:  
  **Play Console > Policy and Programs > App content > Privacy policy**
* **Target Audience:**  
  Ages 13 and older (General Audience / Productivity / Tools).
* **News Apps, Financial Features, COVID-19:**  
  Select **No** for all specialized government/financial categories.
* **Ads:**  
  Select **No, my app does not contain ads**.
