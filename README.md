# E-Commerce Fake API

A simple and lightweight **static JSON Fake API** for frontend developers.

This project provides sample JSON data for **categories** and **products**, which can be consumed from any frontend application using the JavaScript `fetch()` API.

It is useful for:

- 🧪 Frontend development & testing
- 🎓 Learning JavaScript Fetch API
- 🎨 UI/UX prototypes
- ⚡ Demo projects
- 🛠️ Practice projects
- 📦 Testing product/category based applications

---

## 🌐 API Base URL

Once this repository is hosted using GitHub Pages or another static hosting service, you can use your public URL as the API base URL.

```text
https://muhammadfarhandeveloper.github.io/E-Commerce-fakeapi/
```

For example:

```text
https://muhammadfarhandeveloper.github.io/E-Commerce-fakeapi/category.json
https://muhammadfarhandeveloper.github.io/E-Commerce-fakeapi/products.json
```

> Replace `your-domain.com` with your actual hosted URL.

---

## 📁 Project Structure

```text
E-Commerce-fakeapi/
│
├── index.html
├── category.json
├── products.json
├── css/
├────── style.css
└── README.md
```

### Files

| File | Description |
|------|-------------|
| `index.html` | API documentation and usage examples |
| `category.json` | Category data |
| `products.json` | Product data |
| `README.md` | Project documentation |

---

# 📌 Available Endpoints

## Categories

### GET

```text
/category.json
```

Example:

```text
https://muhammadfarhandeveloper.github.io/E-Commerce-fakeapi/category.json
```

### Example Response

```json
[
    {
        "id": 1,
        "name": "Electronics"
    },
    {
        "id": 2,
        "name": "Clothing"
    }
]
```

---

## Products

### GET

```text
/products.json
```

Example:

```text
https://muhammadfarhandeveloper.github.io/E-Commerce-fakeapi/products.json
```

### Example Response

```json
[
    {
        "id": 1,
        "name": "iPhone",
        "price": 999,
        "category": "Electronics"
    },
    {
        "id": 2,
        "name": "T-Shirt",
        "price": 25,
        "category": "Clothing"
    }
]
```

---

# 💻 JavaScript Integration

You can consume the API using the native JavaScript `fetch()` function.

## Fetch Products

```javascript
fetch('https://muhammadfarhandeveloper.github.io/E-Commerce-fakeapi/products.json')
    .then(response => response.json())
    .then(products => {
        console.log(products);
    })
    .catch(error => {
        console.error('Error:', error);
    });
```

---

## Fetch Categories

```javascript
fetch('https://muhammadfarhandeveloper.github.io/E-Commerce-fakeapi/category.json')
    .then(response => response.json())
    .then(categories => {
        console.log(categories);
    })
    .catch(error => {
        console.error('Error:', error);
    });
```

---

# ⚡ Using Async / Await

You can also use modern JavaScript `async/await`.

```javascript
async function getProducts() {

    try {

        const response = await fetch(
            'https://muhammadfarhandeveloper.github.io/E-Commerce-fakeapi/products.json'
        );

        const products = await response.json();

        console.log(products);

    } catch (error) {

        console.error('Error:', error);

    }

}

getProducts();
```

---

# 🛍️ Display Products in HTML

You can fetch the products and dynamically display them in your application.

```html
<div id="products"></div>

<script>

async function loadProducts() {

    const container = document.getElementById('products');

    try {

        const response = await fetch(
            'https://muhammadfarhandeveloper.github.io/E-Commerce-fakeapi/products.json'
        );

        const products = await response.json();

        products.forEach(product => {

            container.innerHTML += `
                <div class="product">
                    <h3>${product.name}</h3>
                    <p>Price: $${product.price}</p>
                    <p>Category: ${product.category}</p>
                </div>
            `;

        });

    } catch (error) {

        console.error('Error:', error);

    }

}

loadProducts();

</script>
```

---

# 🔧 Using the API in Any Frontend

This API can be used with almost any frontend technology or framework that supports HTTP requests.

### JavaScript

```javascript
fetch('https://muhammadfarhandeveloper.github.io/E-Commerce-fakeapi/products.json')
```

### React

```javascript
const response = await fetch(
    'https://muhammadfarhandeveloper.github.io/E-Commerce-fakeapi/products.json'
);

const products = await response.json();
```

### Vue

```javascript
const response = await fetch(
    'https://muhammadfarhandeveloper.github.io/E-Commerce-fakeapi/products.json'
);

const products = await response.json();
```

### Angular

```typescript
this.http.get(
    'https://muhammadfarhandeveloper.github.io/E-Commerce-fakeapi/products.json'
);
```

---

# ⚠️ Important

This project is a **static JSON API**.

It is intended for:

- Frontend development
- Testing
- Prototyping
- Learning
- Demonstration

It does **not** provide a backend database or server-side API functionality.

Therefore, operations such as:

```text
POST
PUT
PATCH
DELETE
```

are not available by default.

The JSON files are provided as static resources and are normally consumed using HTTP `GET` requests.

---

# 🌍 Hosting

You can host this project on any static hosting platform that serves JSON files publicly.

For example:

- GitHub Pages
- Netlify
- Vercel
- Cloudflare Pages
- Any standard web hosting

After deployment, use the generated public URL to access your JSON files.

For example:

```text
https://muhammadfarhandeveloper.github.io/E-Commerce-fakeapi/products.json
```

---

# 🎯 Use Cases

This fake API can be useful when you're building:

### 🛒 E-commerce UI

Use `products.json` to create:

- Product cards
- Product listings
- Product detail pages
- Category filters
- Search interfaces

### 🎓 Learning Projects

Practice:

- `fetch()`
- Promises
- `async/await`
- JSON
- DOM manipulation
- API integration

### 🎨 UI Prototypes

Build frontend designs without setting up a database or backend.

---

# 🤝 Contributing

Contributions are welcome.

If you would like to improve the project:

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Commit your changes.
5. Open a Pull Request.

---

# 📄 License

This project is intended for learning, testing, prototyping, and demonstration purposes.

---

## 👨‍💻 Author

**Muhammad Farhan**

Created for developers who need a simple JSON API for frontend projects.

---

## ⭐ Support

If you find this project useful, consider giving the repository a ⭐ on GitHub.

---

### The Providers

Made with ❤️ by **The Providers**

**© 2026 The Providers — Muhammad Farhan**