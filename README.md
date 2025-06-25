# breachwatch-frontend

## Project Structure

````

📁 breachwatch-frontend/
├── index.html       # main UI

````

---

##  Backend Integration

Update the `fetch()` URL in your `index.html` to point to your Render backend:

```js
fetch("https://<your-backend>.onrender.com/check_password", {
  method: "POST",
  headers: { "Content-Type": "application/json" },
  body: JSON.stringify({ prefix, suffix })
});
````

Make sure CORS is enabled on the Flask backend.

---

##  Run Locally

You can test the frontend locally using a browser or a static server:

```bash
# Example using Python
python -m http.server
```

Then open `http://localhost:8000` in your browser.

---

##  Security Note

* The app never sends full passwords.
* All hashing happens client-side before contacting the backend.
* The backend only receives the first 5 chars of SHA1 hash.

---
