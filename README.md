# FFmpeg License Disclosure for FourClicks Media Manager

This repository provides open-source licensing disclosure for the custom FFmpeg build used in the FourClicks Media Manager desktop application.

---

## 📦 About This FFmpeg Build

The application includes a custom-built version of **FFmpeg version 7.1**, licensed under the **LGPL v2.1** (or later). This build was configured to enable H.264 video encoding through Cisco's OpenH264 library and to remain fully LGPL-compliant.

### 🔧 Build Configuration
To rebuild FFmpeg with the same configuration:

```bash
./configure --disable-gpl --enable-libopenh264 --disable-libx264 --disable-libx265 
make

--disable-gpl: Ensures that GPL-only features are excluded so that the resulting binary stays under the LGPL license.
--disable-libx264 --disable-libx265:  Specifically exclude those two functions so that the resulting binary stays under the LGPL license.
--enable-libopenh264: Adds support for H.264 encoding using the Cisco OpenH264 codec (licensed under the BSD 2-Clause License).

This FFmpeg binary is dynamically linked and unmodified, and users are free to rebuild, replace, or relink it as needed.

## 📄 Licensing and Source Access
In accordance with LGPL v2.1 requirements:

A copy of the FFmpeg LGPL license text is included in this repository:
Licenses/LGPL-2.1.txt

The FFmpeg source code is publicly available at:
https://ffmpeg.org/download.html
https://github.com/FFmpeg/FFmpeg

Users may obtain, modify, and rebuild FFmpeg from these official sources using the same configuration flags provided above.
Licensing Requirements

🎥 OpenH264 License and Source
This build also enables the use of Cisco's OpenH264 codec.
OpenH264 is licensed under the BSD 2-Clause License.
License file: Licenses/BSD-2-Clause.txt

Official source and binaries are available at:
https://github.com/cisco/openh264

⚠️ Notes
The FFmpeg binary used in FourClicks Media Manager is dynamically linked, not statically linked, and no modifications were made to the source code.
This disclosure satisfies LGPL and BSD license obligations for redistribution and transparency.
FourClicks Media Manager is not affiliated with the FFmpeg project, Cisco, or any of the third-party open-source projects listed.

For further inquiries, please contact the developer or consult the license documentation included in the application package.
