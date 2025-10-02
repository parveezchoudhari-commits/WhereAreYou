# Location-Privacy Demonstration (Educational)

**Short summary:**  
This repository demonstrates, for educational purposes only, how browser geolocation can be used to obtain device coordinates and the privacy risks that arise when location is collected without clear consent. The repository intentionally focuses on defensive awareness and mitigation.

> **Important:** This project MUST only be used for research and demonstration with devices and accounts for which you have explicit, informed consent. Do not use this or similar code to obtain other people's locations without permission. Doing so may be illegal and unethical.

## What this repository contains
- `funnyhtml.txt` — original demo HTML (reviewed). It calls the browser Geolocation API and performs a network request to a server endpoint. :contentReference[oaicite:1]{index=1}
- `safe-demo/index.html` — a safe demo (displays coordinates locally, no exfiltration) recommended for public GitHub Pages.
- Documentation files: `ABOUT_ME.md`, `CONTRIBUTING.md`, `SECURITY.md`, `LICENSE.md`, and this `README.md`.

## Why I made this
The web platform exposes powerful APIs. This repo is intended to:
- Demonstrate how geolocation works.
- Show how location data might be sent off-device.
- Educate developers and users on ways to minimize privacy risks.

## Ethical & legal requirements (must read)
- **Consent:** Obtain explicit, documented consent from the device owner before running any demo that reads or transmits location.
- **Scope:** Only run the original `funnyhtml` demo or any code that transmits coordinates on test devices or within a lab environment under your control.
- **Legal compliance:** Laws about tracking and surveillance vary by jurisdiction. If you're unsure, consult a lawyer before using or publishing location-capture demonstrations that collect or store others’ data.
- **No covert deployment:** Do not embed tracking code in live websites or public pages intended to collect people's locations without prior notice and consent.

## Safe demo (recommended)
For public demos (GitHub Pages) use the `safe-demo/index.html` file that *only displays* the coordinates in the browser and does not send them to any server. This preserves the educational value while avoiding exfiltration risk.

### How to run safe demo locally (example)
1. Open `safe-demo/index.html` in a browser (file:// or served via a static server).
2. Grant permission when prompted (only do this for your own device or with consent).
3. The page will show latitude/longitude on-screen — nothing is sent to a remote server.

## Notes about the original file
The uploaded file calls `navigator.geolocation.getCurrentPosition` and then uses an XHR to `store.php` to transmit coordinates and the user agent. That behavior is powerful but dangerous if deployed without consent. See `SECURITY.md` for mitigation advice. :contentReference[oaicite:2]{index=2}

## Contributing
See `CONTRIBUTING.md`.

## Responsible disclosure / Contact
If you discover a way this demo could be abused, or find a bug, please open an issue or contact me at: [your-email@example.com] (replace with safe contact).

## License
Licensed under the terms in `LICENSE.md` (includes a Responsible Use Addendum).