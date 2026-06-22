# Cyberprotek — Flask Website

## Run locally
1. Install dependencies:
   pip install -r requirements.txt

2. Start the server:
   python app.py

3. Open http://localhost:5000 in your browser.

## Structure
- app.py            — Flask routes + service data
- templates/         — Jinja2 HTML templates (base.html + page templates)
- static/style.css   — shared stylesheet
- messages.csv        — created automatically when someone submits the contact form

## Pages
- /                       Home
- /services               Services overview
- /services/<slug>        Service detail (vapt, network-security, server-cloud, cctv, it-support, web-development)
- /about                  About
- /contact                Contact (GET shows form, POST saves the message to messages.csv)

## Notes
- Update placeholder email/phone in templates/base.html, templates/contact.html, and app.py footer links.
- Update pricing in the SERVICES list inside app.py.
- For production, run behind gunicorn/waitress instead of the Flask dev server, and set debug=False.
