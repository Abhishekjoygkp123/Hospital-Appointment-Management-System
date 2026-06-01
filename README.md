# 🏥 MediBook — Hospital Appointment Management System
 
A clean, fully client-side web application for managing hospital appointments, patients, and doctors. Built with plain HTML, CSS, and JavaScript — no frameworks, no build tools, no backend required.
 
---
 
## ✨ Features
 
### Appointment Management
- Book appointments by selecting existing patients and doctors
- **Add a brand-new patient or doctor inline** while booking — no need to leave the form
- Edit or delete any appointment
- Filter appointments by **status**, **doctor**, and **date range** (Today / Tomorrow / This Week / Past)
- Search by patient name, doctor name, or department
### Smart Validations
- **Double-booking detection** — warns if the selected doctor is already booked at the same date and time
- **Past-date guard** — alerts you before booking an appointment in the past
- **Doctor availability warning** — flags doctors marked as "On Leave" or "Full" when selected
- **Cascade delete** — deleting a patient or doctor also removes all their linked appointments, with a clear warning before confirming
### Patient Directory
- Add, edit, and delete patient records
- Stores name, age, gender, blood group, and contact number
- Shows total appointment count per patient
### Doctor Directory
- Add, edit, and delete doctor records
- Filter by department
- Shows availability status and total appointment count per doctor
### Dashboard
- Live stats: Total, Scheduled, Pending, Completed, and Cancelled appointments
- Recent appointments table
- Sidebar glance view: Today's count, Pending, and Done
### Data Persistence
- All data is saved to **localStorage** — your records survive page refreshes and browser restarts
- No database or server needed
---
 
## 🗂️ Project Structure
 
```
medibook/
└── medibook.html      # The entire application — single self-contained file
└── README.md
```
 
Everything — HTML, CSS, and JavaScript — lives in one file. There are no external dependencies except Google Fonts (loaded via CDN), so the app works offline once the fonts are cached.
 
---
 
## 🚀 Deploying via GitHub Pages
 
GitHub Pages lets you host this for free directly from your repository. Follow these steps after pushing your code.
 
### Step 1 — Push your files to GitHub
 
Make sure your repository contains at least these two files at the root:
```
medibook.html
README.md
```
 
If `medibook.html` is your only page and you want it to load as the homepage, **rename it to `index.html`** before pushing. GitHub Pages serves `index.html` automatically at the root URL.
 
```bash
# If you haven't initialised git yet
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git push -u origin main
```
 
### Step 2 — Enable GitHub Pages
 
1. Go to your repository on GitHub
2. Click the **Settings** tab (top menu of the repo)
3. In the left sidebar, scroll down and click **Pages**
4. Under **Build and deployment → Source**, select **Deploy from a branch**
5. Under **Branch**, choose **main** and keep the folder as **/ (root)**
6. Click **Save**
### Step 3 — Access your live URL
 
After about 30–60 seconds, GitHub will show you your live URL at the top of the Pages settings. It will look like:
 
```
https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/
```
 
If you kept the filename as `medibook.html` instead of renaming it, the URL will be:
```
https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/medibook.html
```
 
> Every time you push new changes to the `main` branch, GitHub Pages automatically redeploys within a minute or two.
 
---
 
## 💾 A Note on Data Storage
 
MediBook uses **localStorage**, which means:
 
| Situation | What happens to your data |
|---|---|
| Refresh the page | ✅ Data is preserved |
| Close and reopen the browser | ✅ Data is preserved |
| Open in a different browser | ❌ Data does not carry over |
| Open in a private/incognito window | ❌ Starts fresh |
| Someone else visits your GitHub Pages URL | ❌ They see fresh seed data (their localStorage is separate from yours) |
| Clear browser data / site data | ❌ Data is wiped |
 
This means MediBook is best suited for **single-user, single-device use** — for example, one receptionist using it on one machine. If you need multi-user or multi-device data sharing, a backend database would be required.
 
---
 
## 🖥️ Running Locally (Without GitHub)
 
No installation needed. Just open the file directly:
 
```bash
# Option 1 — double-click medibook.html in your file explorer
 
# Option 2 — open from terminal (macOS)
open medibook.html
 
# Option 3 — open from terminal (Linux)
xdg-open medibook.html
 
# Option 4 — open from terminal (Windows)
start medibook.html
```
 
---
 
## 🛠️ Tech Stack
 
| Layer | Technology |
|---|---|
| Markup | HTML5 |
| Styling | CSS3 (custom properties, grid, flexbox) |
| Logic | Vanilla JavaScript (ES6+) |
| Fonts | DM Sans + DM Mono via Google Fonts |
| Storage | Browser localStorage |
| Hosting | GitHub Pages (static) |
 
No npm, no Node, no build step. One file.
 
---
 
## 📋 Departments Supported
 
Cardiology · Neurology · Orthopaedics · Gynaecology · Paediatrics · Dermatology · General Medicine · ENT · Ophthalmology
 
---
 
## 🔮 Possible Future Enhancements
 
- Export appointments to CSV or PDF
- Calendar / weekly schedule view
- SMS or email appointment reminders
- Multi-user support with a backend (e.g. Firebase, Supabase)
- Print-friendly appointment slips
- Patient medical history notes
---
 
## 📄 License
 
This project is open source and free to use, modify, and distribute.
