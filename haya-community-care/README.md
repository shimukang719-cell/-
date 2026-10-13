# Haya Community Care — local demo

Files:
- `index.html`: full community website with registration section
- `registration.html`: independent standalone registration page
- `admin.html`: independent admin demo (username `admin`, password `HayaDemo2026`)

Place all three HTML files in the **same folder**. Each file can be opened separately.

## Important about local storage
Registration entries are stored in the browser localStorage. Some browsers isolate `file://` pages from each other or block storage; opening each file by double-clicking **may not share registrations**. For reliable linking, open Terminal in the folder and run:

```sh
python3 -m http.server 8000
```

Then open `http://localhost:8000/registration.html` and `http://localhost:8000/admin.html` in the **same browser**. This serves the files only on your own computer by default (avoid sharing the server on your network). Stop with Control+C. If Python is not installed, use a local static server tool instead.

## Privacy and security
All login logic is front-end-only and easily bypassed. LocalStorage is not encrypted and is accessible to scripts on the same origin. Use **fictional** names and emails only. Never use this as a real client registration service. No backend, real account creation, email notification, or secure access control is implemented. The booking form remains a visual demo. Do not publish these files as a real service.
