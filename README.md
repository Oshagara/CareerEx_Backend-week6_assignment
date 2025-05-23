# 📦 Drugstore API

This project is a simple Node.js Express server that provides APIs to interact with a list of drugs.  
It demonstrates the use of **routes**, **HTTP methods**, and **Postman** for testing.

---

## 🛠 Tech Stack

- Node.js
- Express.js
- Postman (for testing APIs)

---

## 🚀 How to Run

1. **Clone this repo:**

   ```bash
   git clone https://github.com/Oshagara/CareerEx_Backend-week6_assignment.git
   cd CareerEx_Backend-week6_assignment
   ```

2. **Install dependencies:**

   ```bash
   npm install
   ```

3. **Start the server:**

   ```bash
   node server.js
   ```
   (or if you are using nodemon:)
   ```bash
   npx nodemon server.js
   ```

4. **Server runs on:**  
   `http://localhost:3000` (default port)

---

## 📚 API Endpoints

| Method | Route                         | Description |
|--------|-------------------------------|-------------|
| GET    | `/drugs/antibiotics`            | Get all drugs in the "Antibiotic" category |
| GET    | `/drugs/names`                  | Get all drug names (lowercase) |
| POST   | `/drugs/by-category`            | Get all drugs by category (send `{ "category": "..." }`) |
| GET    | `/drugs/names-manufacturers`     | Get an array of drug names with manufacturers |
| GET    | `/drugs/prescription`            | Get all prescription-only drugs |
| GET    | `/drugs/formatted`               | Get formatted list: "Drug: [name] - [dosageMg]mg" |
| GET    | `/drugs/low-stock`               | Get drugs with stock less than 50 |
| GET    | `/drugs/non-prescription`        | Get all non-prescription drugs |
| POST   | `/drugs/manufacturer-count`      | Get the count of drugs by a manufacturer (send `{ "manufacturer": "..." }`) |
| GET    | `/drugs/count-analgesics`         | Get the number of "Analgesic" drugs |

---

## 🧪 Sample POST Body Examples (for Postman)

- For `/drugs/by-category`:

```json
{
  "category": "Antibiotic"
}
```

- For `/drugs/manufacturer-count`:

```json
{
  "manufacturer": "Pfizer"
}
```

---

## 📝 Notes

- Remember to use **express.json()** middleware to parse JSON request bodies.
- Test every route in **Postman** (GET and POST).
- No database connected — the data is stored **in-memory** using an array.

---

## 📌 Author

- Name: Israel Oshagara
- Assignment: CareerEx Backend - Week 6