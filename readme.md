# Easy URL Shortener

## Project Structure

```ascii
.
├── shortener_app/
│   ├── __init__.py
│   ├── config.py
│   ├── database.py
│   ├── main.py
│   ├── models.py
│   └── scheams.py
├── .venv
└── .env
```

---

## run it

```shell
uvicorn shortener_app.main:app --host 0.0.0.0 --reload
```

---

## Endpoints

| Endpoint              | HTTP Verb | Request Body | Action                 |
| --------------------- | --------- | ------------ | ---------------------- |
| `/`                   | GET       |              | "Hello World"          |
| `/url`                | POST      | Target URL   | Shows Created URL info |
| `/{url_key}`          | GET       |              | Forward to URL         |
| `/admin/{secret_key}` | GET       |              | Admin Info             |
| `/admin/{secret_key}` | DELETE    | Secret Key   | Delete URL             |

---

## Typical Response Body

```json
{
  "target_url": "https://realpython.com",
  "is_active": true,
  "clicks": 0,
  "url": "SSP9P",
  "admin_url": "UHTITEZA"
}
```

---

## Resources

- [Pydantic Settings](https://docs.pydantic.dev/latest/concepts/pydantic_settings/)
