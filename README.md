# 🛍️ Product Pagination App

A simple **JavaScript OOP-based web app** that fetches products from an API and displays them with **client-side pagination**.

This project demonstrates:

- API calls using **Promises**
- Object-Oriented Programming (OOP)
- DOM manipulation
- Dynamic pagination system

---

## 🚀 Features

✔ Fetch products from live API  
✔ Show products in grid layout  
✔ Pagination buttons auto-generated  
✔ Active page highlight  
✔ Clean UI using CSS Grid  
✔ No frameworks — Pure HTML, CSS, JavaScript  

---

## 🌐 API Used

Data is fetched from:

```
https://dummyjson.com/products
```

Supports query parameters:

| Parameter | Purpose |
|----------|---------|
| `limit` | Number of products per page |
| `skip` | Offset for pagination |

---

## 🧠 How It Works

### 1️⃣ App Initialization

When the page loads:

```js
new ProductApp();
```

This creates an object of the `ProductApp` class and starts the app.

---

### 2️⃣ Fetching Products (API Call)

```js
fetch(`${this.api}?limit=${this.limit}&skip=${this.skip}`)
```

- Uses **fetch()**
- Returns a **Promise**
- Converts response to JSON

---

### 3️⃣ Rendering Products

Each product is shown as a **card** with:

- Image
- Title
- Price
- Rating

Cards are inserted dynamically into:

```html
<div id="products"></div>
```

---

### 4️⃣ Pagination Logic

```js
const totalPages = Math.ceil(this.total / this.limit);
```

Buttons are generated based on total products from the API.

When a button is clicked:

```js
this.skip = (i - 1) * this.limit;
this.loadProducts();
```

This updates the API call to fetch the next set of products.

---

## 🏗 Project Structure

```
index.html
 ├── HTML Layout
 ├── CSS Styling
 └── JavaScript (ProductApp Class)
```

Everything is built inside one file for learning purposes.

---

## 🎯 Learning Concepts Used

| Concept | Where Used |
|--------|------------|
| OOP | `class ProductApp` |
| Promises | `fetchProducts()` |
| DOM Manipulation | `createElement()` |
| Event Handling | Pagination buttons |
| API Integration | DummyJSON |

---

## 📦 How to Run

1. Download the project
2. Open `index.html` in a browser
3. Done ✅

No installation required.

---

## 🔮 Future Improvements

- Search functionality
- Category filter
- Loading spinner
- Error message UI
- Responsive design for mobile

---

## 👨‍💻 Author

Developed as a practice project to understand:

**JavaScript APIs + Pagination + OOP**
