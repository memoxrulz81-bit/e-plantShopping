
# 🌿 Paradise Nursery

**Paradise Nursery** is a simple e-commerce web application built with **React** and **Redux Toolkit**.
It allows users to browse categorized plants, add them to a shopping cart, update quantities, and view the total cart amount.

---

## 🚀 Features

* 🌱 Browse plants by category
* 🏷️ Sale badge on all products
* 🛒 Add items to cart
* ➕ Increment / ➖ Decrement quantity
* ❌ Remove items from cart
* 💰 Automatic total price calculation
* 🔢 Live cart quantity indicator
* 📱 Responsive layout

---

## 🛠️ Tech Stack

* **React**
* **Redux Toolkit**
* **React Redux**
* **CSS (Flexbox + Responsive Media Queries)**

---

## 📂 Project Structure

```
src/
│
├── AboutUs.css         # AboutUs styling
├── AboutUs.js          # Site info
├── CartSlice.js        # Redux slice (cart logic)
├── CartItem.js         # Cart page component
├── ProductList.js      # Product listing page
├── ProductList.css     # Main styling
├── CartItem.css        # Cart styling
├── store.js            # Redux store configuration
└── index.js            # App entry point
└── App.js              # App entry point
└── App.css             # App styling
└── main.js             # main entry point
```

---

## 🧠 State Management

Redux Toolkit is used to manage cart state.

### Cart State Structure

```js
{
  cart: {
    items: [
      {
        name: "Snake Plant",
        image: "url",
        cost: "$15",
        quantity: 2
      }
    ]
  }
}
```

### Available Actions

* `addItem(product)`
* `removeItem(name)`
* `updateQuantity({ name, quantity })`
* `clearCart()

💰 Total Calculations
Total Quantity
state.cart.items.reduce(
  (total, item) => total + item.quantity,
  0
)
Total Amount
cart.reduce((total, item) => {
  const cost = parseFloat(item.cost.substring(1));
  return total + cost * item.quantity;
}, 0);
