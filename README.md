# Blog REST API

This project is a simple **RESTful Blog API** built with **Node.js** and **Express.js**.
It allows users to create, read, update, and delete blog posts using standard HTTP methods.

The application stores blog posts in an **in-memory data structure (array)**, which means the data will reset when the server restarts. The purpose of this project is to demonstrate how a basic REST API works.

---

## Technologies Used

* **Node.js** – JavaScript runtime environment
* **Express.js** – Web framework for building APIs
* **Body-parser** – Middleware used to parse request bodies

---

## Features

The API supports the following **CRUD operations**:

* Get all posts
* Get a specific post by ID
* Create a new post
* Update an existing post
* Delete a post

---

## Data Structure

Each blog post contains the following fields:

| Field   | Description                   |
| ------- | ----------------------------- |
| id      | Unique identifier of the post |
| title   | Title of the blog post        |
| content | Content of the post           |
| author  | Author of the post            |
| date    | Creation date of the post     |

Example post object:

```json
{
  "id": 1,
  "title": "The Rise of Decentralized Finance",
  "content": "Decentralized Finance (DeFi) is an emerging field...",
  "author": "Alex Thompson",
  "date": "2023-08-01T10:00:00Z"
}
```

---

## API Endpoints

### Get All Posts

```http
GET /posts
```

Returns all blog posts.

---

### Get a Post by ID

```http
GET /posts/:id
```

Returns a specific blog post.

---

### Create a New Post

```http
POST /posts
```

Request Body Example:

```json
{
  "title": "New Post Title",
  "content": "Post content here",
  "author": "Author Name"
}
```

---

### Update a Post

```http
PATCH /posts/:id
```

Updates specific fields of an existing post.

Example Request Body:

```json
{
  "title": "Updated Title"
}
```

---

### Delete a Post

```http
DELETE /posts/:id
```

Deletes a post by ID.

---

## Installation

1. Clone the repository

```bash
git clone https://github.com/yourusername/blog-api.git
```

2. Navigate to the project directory

```bash
cd blog-api
```

3. Install dependencies

```bash
npm install
```

4. Run the server

```bash
node index.js
```

The API will start at:

```
http://localhost:4000
```

---

## Notes

* Data is stored **temporarily in memory**, so it will reset whenever the server restarts.
* This project is intended for **learning and demonstration purposes**.

---

## License

This project is open-source and available under the **MIT License**.
