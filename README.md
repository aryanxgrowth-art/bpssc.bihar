# RozgarUpdate - GitHub Pages + Online Application

## 1. Upload to GitHub
Create a repository, upload all files/folders, then enable:
Settings -> Pages -> Deploy from branch -> main -> /(root).

## 2. Add/update a vacancy
Open `assets/jobs.js` on GitHub.
Inside `const jobs = [...]`, copy an object and edit:
- id (unique)
- title
- department
- category: `10th`, `12th`, or `graduate`
- qualification
- vacancies
- lastDate
- age
- fee
- description

Commit changes. GitHub Pages will rebuild automatically.

## 3. Official government vacancies
For government recruitment, use `applicationMode:"official"` and put the verified official application URL in `applyUrl`.
Do not collect applicant money or personal documents on a static GitHub Pages site unless you have a proper backend, privacy/security controls and legal basis.

## 4. Your own online application
GitHub Pages cannot securely store submitted forms by itself. This package expects a backend endpoint in `assets/jobs.js`.

A simple option is Google Apps Script + Google Sheet:
- Create a Google Sheet for applications.
- Create an Apps Script web app that accepts POST JSON and writes rows to the sheet.
- Deploy as Web App and copy its `/exec` URL into APP_CONFIG.endpoint.

Do not put passwords, API keys, database credentials, or payment secrets in GitHub client-side files.

## 5. Production requirements
For a serious portal, use a real backend/database and add authentication, rate limiting, CAPTCHA/anti-spam, HTTPS, validation, privacy policy, terms, data retention/deletion process, and secure file storage. Never store passwords or sensitive applicant documents in plain text.

The included government listing is a placeholder. Verify current recruitment notifications and official URLs before publishing.
