# Open Source Software Notices & Third-Party Licenses

**Project:** AiroSync (Cross-Platform Local Peer-to-Peer Synchronization & Transfer)  
**Author / Copyright Holder:** Asep Sayyad  
**Last Updated:** October 11, 2026  

AiroSync incorporates and links to components licensed under various open-source licenses. This document acknowledges and fulfills the attribution and copyright distribution obligations required by their respective licenses.

---

## 1. Summary of Third-Party Dependencies

### A. Android Client (`com.asep.airosync`)

| Component / Library | Primary License | Copyright / Origin |
| :--- | :--- | :--- |
| **AndroidX Core, Lifecycle, Room, Navigation** | Apache License 2.0 | Google LLC / Android Open Source Project |
| **Jetpack Compose (UI, Foundation, Material 3)** | Apache License 2.0 | Google LLC / Android Open Source Project |
| **Kotlin Coroutines & Serialization** | Apache License 2.0 | JetBrains s.r.o. |
| **OkHttp & Logging Interceptor** | Apache License 2.0 | Square, Inc. |
| **Retrofit & Moshi** | Apache License 2.0 | Square, Inc. |
| **Coil Compose** | Apache License 2.0 | Coil Contributors |
| **Ktor Client (Core, OkHttp, WebSockets, ContentNegotiation)** | Apache License 2.0 | JetBrains s.r.o. |
| **AndroidX Media3 (ExoPlayer, Session, UI)** | Apache License 2.0 | Google LLC |

### B. Windows Desktop Client (`airosync`)

| Component / Library | Primary License | Copyright / Origin |
| :--- | :--- | :--- |
| **Electron** | MIT License | OpenJS Foundation / Electron Contributors |
| **Express** | MIT License | Express / OpenJS Foundation |
| **Winston & Winston Daily Rotate File** | MIT License | Winston Contributors |
| **Helmet** | MIT License | Helmet Contributors |
| **HPP (HTTP Parameter Pollution protection)** | MIT License | HPP Contributors |
| **Koffi (C FFI library)** | MIT License | Koffi Contributors |
| **Clipboardy** | MIT License | Sindre Sorhus |
| **QRCode** | MIT License | Ryan Day |
| **JSZip** | MIT License | Stuart Knightley / David Duponchel |
| **Selfsigned** | MIT License | Selfsigned Contributors |
| **Dotenv** | BSD 2-Clause License | Scott Motte |
| **Node-Notifier** | MIT License | Eirik Sletteberg (vendor binary zlib/libpng / MIT) |
| **Electron-Updater** | MIT License | Electron-Builder Contributors |
| **Sharp** | Apache License 2.0 | Lovell Fuller |
| **libvips (bundled dynamically by Sharp on Windows)** | LGPL v3 (or later) | libvips Contributors |

### C. Cloud Admin Panel & Remote Config (`Server-Admin`)

| Component / Library | Primary License | Copyright / Origin |
| :--- | :--- | :--- |
| **Express** | MIT License | Express / OpenJS Foundation |
| **Bcrypt.js** | MIT License | Daniel Bikiel |
| **JsonWebToken** | MIT License | Auth0 / Okta |
| **Better-SQLite3** | MIT License | Joshua Wise |
| **Cors** | MIT License | Troy Goode |
| **Express-Rate-Limit** | MIT License | Nathan Friedly |
| **Helmet** | MIT License | Helmet Contributors |
| **Dotenv** | BSD 2-Clause License | Scott Motte |

---

## 2. Applicable License Texts

### A. The MIT License
```text
Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

### B. Apache License, Version 2.0
```text
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

---

### C. BSD 2-Clause License
```text
Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this
   list of conditions and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright notice,
   this list of conditions and the following disclaimer in the documentation
   and/or other materials provided with the distribution.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
```

---

### D. GNU Lesser General Public License (LGPL v3) Notice (libvips)
```text
The Windows desktop distribution of AiroSync utilizes 'sharp' which dynamically links
to the pre-compiled shared library binaries of 'libvips' (licensed under the GNU Lesser
General Public License v3 or later).

In compliance with LGPL v3 Section 4:
1. Dynamic Linking: libvips is dynamically loaded at runtime as a shared library DLL.
2. Relinking / Replacement: Users may modify or replace the libvips shared library files
   located within the installed application directory ('node_modules/sharp/vendor') with
   custom or recompiled compatible versions.
3. Source Code Availability: The source code for libvips can be obtained directly from
   its official repository at: https://github.com/libvips/libvips
4. License Text: Full text of the LGPL v3 is available at:
   https://www.gnu.org/licenses/lgpl-3.0.html
```

---

## 3. Inquiries
For questions regarding open-source licensing compliance or attribution, please contact:
* **Developer:** Asep Sayyad
* **Email:** [asepsayyad@gmail.com](mailto:asepsayyad@gmail.com)
* **GitHub Repository:** [https://github.com/asepsayyad007/AiroSync-Release](https://github.com/asepsayyad007/AiroSync-Release)
