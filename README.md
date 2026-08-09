# Infinity Codex FF JWT API

A Flask-based API service that generates JWT responses from authorized Free Fire authentication flows.

## Credit

**Infinity Codex**

## Files

- `app.py` — Main API application 
- `vercel.json` — Vercel deployment configuration
- `requirements.txt` — Python dependencies
- `LICENSE` — MIT License

## Installation

Use Python 3.10 or later.

```bash
pip install -r requirements.txt
```

## Running Locally

```bash
python app.py
```

When the server starts, it will use the `PORT` environment variable; if not set, it falls back to the port defined in the application.

## Deploying to Vercel

```bash
vercel deploy
```

## API Endpoints

### Guest Token to JWT

```
GET /guest_to_jwt?uid=YOUR_UID&password=YOUR_PASSWORD
```

### Access Token to JWT

```
GET /acces_to_jwt?access_token=YOUR_ACCESS_TOKEN
```

### EAT Token to JWT

```
GET /eat_to_jwt?eat_token=YOUR_EAT_TOKEN
```

All endpoints return a JSON response. Do not share real tokens or credentials publicly.

## Responsible Use

- Only use your own or authorized accounts and valid API access.
- Never store tokens, passwords, or personal credentials in source code, README files, or public repositories.
- Follow the terms of service, rate limits, and applicable laws of any third-party services.

## License

This project is released under the MIT License. See the `LICENSE` file for details.
