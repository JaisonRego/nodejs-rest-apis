# 📌 Simple Express Posts API

A minimal **Node.js + Express** backend for managing posts (read and create).
Posts are stored in a local `posts.json` file.

---

## 🚀 Features

✅ Get all posts
✅ Get a single post by ID
✅ Create a new post (with random ID)
✅ Data persisted to `posts.json`
✅ Includes CORS headers for frontend integration

---

## 📂 Project Structure

```
.
├── app.js             # Main Express server
├── data
│   └── posts.js       # Helper functions to read/write posts
├── package.json
├── posts.json         # JSON storage for posts
└── README.md
```

---

## 🛠️ Installation

1. **Install dependencies**

   ```bash
   npm install
   ```

2. **Run the server**

   ```bash
   node app.js
   ```

   Server will start on **[http://localhost:8080](http://localhost:8080)**

---

## 📡 API Endpoints

### ➡️ Get all posts

**GET** `/posts`
**Response:**

```json
{
  "posts": [
    { "body": "...", "author": "...", "id": "..." }
  ]
}
```

---

### ➡️ Get single post

**GET** `/posts/:id`
Example: `/posts/post-1`
**Response:**

```json
{
  "post": { "body": "...", "author": "...", "id": "..." }
}
```

---

### ➡️ Create new post

**POST** `/posts`
**Request body:**

```json
{
  "body": "Your post content",
  "author": "Your name"
}
```

**Response:**

```json
{
  "message": "Stored new post.",
  "post": { "body": "...", "author": "...", "id": "random-id" }
}
```

---

## ⚙️ Notes

* Posts are stored in `posts.json` in the project root.
* CORS is enabled so you can call this API from a frontend running on a different domain/port.

---

## 📜 License

Feel free to use and modify as you wish! ✨
