# Pallet Shuttle Monitor (Ghana)

A lightweight, self-hosted web app to manage pallet shuttle maintenance for multiple clients:
- Clients / Sites
- Pallet Shuttles (assets)
- Maintenance records (preventive/corrective)
- Issues/faults & resolution
- Parts catalog + parts replaced per job
- Costs (labor, parts, other) + simple reports
- CSV export for key tables
- Login/roles via Django auth (create users in Admin)

## Tech
- Python 3.10+
- Django 5.x
- SQLite (default). Swap to Postgres easily.

---

## Quick start (local)

```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
source .venv/bin/activate

pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py seed_demo   # optional sample data
python manage.py runserver
```

Open:
- App: http://127.0.0.1:8000/
- Admin: http://127.0.0.1:8000/admin/

---

## Deploy notes
- Use `DEBUG=0` and set `SECRET_KEY` in environment variables for production.
- Consider Postgres + a managed VPS (DigitalOcean, Hetzner, etc.).
- Put behind Nginx + Gunicorn.

---

## CSV export
On list pages, click **Export CSV**.

---

## Import from your Excel
Export your Excel sheets to CSV and use Admin import (or ask me to add an import wizard that matches your current Excel columns).

---

## License
MIT
