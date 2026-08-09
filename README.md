# Infinity Codex FF JWT API

একটি Flask-ভিত্তিক API service, যা অনুমোদিত Free Fire authentication flow থেকে JWT response তৈরি করে।

## Credit

**Infinity Codex**

## ফাইল

- `app.py` — মূল API application
- `LICENSE` — MIT License

## ইনস্টলেশন

Python 3.10 বা পরবর্তী সংস্করণ ব্যবহার করুন।

```bash
pip install flask requests protobuf
```

## চালানো

```bash
python app.py
```

সার্ভার চালু হলে এটি environment-এর `PORT` ব্যবহার করবে; না থাকলে application-এর নির্ধারিত port ব্যবহার করবে।

## Vercel deployment

Repository root-এ `app.py`, `api/index.py`, `requirements.txt` এবং `vercel.json` রাখুন। এরপর নিজের GitHub account থেকে repository-তে commit ও push করে Vercel-এ project import করুন।

Deploy হওয়ার পর endpoint হবে:

```text
https://YOUR-VERCEL-DOMAIN.vercel.app/gen?UID={UID}&password={password}
```

## API Endpoints

### UID ও password থেকে JWT

```text
GET https://myapp.vercel.app/gen?UID={UID}&password={password}
```

```text
GET /gen?UID=YOUR_UID&password=YOUR_PASSWORD
```

### Access token থেকে JWT

```text
GET /acces_to_jwt?access_token=YOUR_ACCESS_TOKEN
```

### EAT token থেকে JWT

```text
GET /eat_to_jwt?eat_token=YOUR_EAT_TOKEN
```

প্রতিটি endpoint-এর response JSON আকারে আসে। বাস্তব user token বা credential প্রকাশ্যে শেয়ার করবেন না।

## দায়িত্বশীল ব্যবহার

- শুধু নিজের বা অনুমোদিত account এবং বৈধ API access ব্যবহার করুন।
- কোনো token, password বা ব্যক্তিগত credential source code, README বা public repository-তে রাখবেন না।
- তৃতীয় পক্ষের service-এর terms, rate limit এবং applicable law মেনে চলুন।

## License

এই project MIT License-এর অধীনে প্রকাশিত। বিস্তারিত `LICENSE` ফাইলে দেখুন।