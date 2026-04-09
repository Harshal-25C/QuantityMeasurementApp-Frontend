# 🚀 Quantity Measurement App – Frontend (React + TypeScript)

> A modern, interactive UI for performing **unit conversions, comparisons, and arithmetic operations** across multiple measurement types — powered by React and integrated with a Spring Boot backend.

---

## ✨ Features

🎯 **Authentication**

* User Registration & Login (JWT-based)
* Secure API communication using Bearer Token

📏 **Measurement Operations**

* Compare quantities (>, <, =)
* Convert units across categories
* Perform arithmetic operations:

  * ➕ Add
  * ➖ Subtract
  * ➗ Divide
  * ✖️ Multiply
  * 🟰 Compare

📊 **History Tracking**

* View past operations
* Filter by operation type

🎨 **User Experience**

* Responsive UI
* Toast notifications
* Real-time results
* Clean dashboard interface

---

## 🧠 Supported Measurement Types

| Type            | Units                                   |
| --------------- | --------------------------------------- |
| 📏 Length       | FEET, INCHES, YARDS, CENTIMETERS        |
| ⚖️ Weight       | MILLIGRAM, GRAM, KILOGRAM, POUND, TONNE |
| 🧪 Volume       | LITRE, MILLILITRE, GALLON               |
| 🌡️ Temperature | CELSIUS, FAHRENHEIT, KELVIN             |

---

## 🏗️ Project Structure

```
src/
│
├── pages/
│   ├── Login.tsx
│   ├── Dashboard.tsx
│
├── components/
│   ├── Toast.tsx
│
├── services/
│   ├── api.ts
│
├── App.tsx
├── index.tsx
└── styles.css
```

---

## 🔗 API Integration

All API calls are handled in:

```
src/services/api.ts
```

### Base URL

```ts
var BASE_URL = 'http://localhost:8080';
```

### Example API

```ts
export async function compareApi(payload: any) {
  return quantityRequest('/api/v1/quantities/compare', payload);
}
```

---

## 🔐 Authentication Flow

1. User logs in
2. Backend returns JWT token
3. Token stored in localStorage:

```ts
localStorage.setItem('qm_token', token);
```

4. Token used in all API calls:

```ts
headers: {
  Authorization: 'Bearer ' + token
}
```

---

## 🔄 Data Flow (Frontend → Backend)

```text
User Input
   ↓
React UI (Dashboard)
   ↓
API Call (fetch)
   ↓
Spring Boot Backend
   ↓
Response JSON
   ↓
UI Update (Result Display)
```

---

## ⚙️ Setup & Installation

### 1️⃣ Clone Repository

```bash
git clone <your-repo-url>
cd quantity-measurement-app-frontend
```

---

### 2️⃣ Install Dependencies

```bash
npm install
```

---

### 3️⃣ Start Development Server

```bash
npm start
```

👉 Open in browser:

```
http://localhost:3000
```

---

## 📜 Available Scripts

### ▶️ Start App

```bash
npm start
```

Runs the app in development mode.
Hot reload enabled.

---

### 🧪 Run Tests

```bash
npm test
```

Launches test runner in interactive mode.

---

### 🏗️ Build for Production

```bash
npm run build
```

Creates optimized production build in `/build`.

---

### ⚠️ Eject Config (Advanced)

```bash
npm run eject
```

> ⚠️ This is irreversible.

---

## 🧪 Testing Guide

### ✔️ Functional Testing

* Signup → Login → Dashboard
* Compare units
* Convert units
* Perform arithmetic
* View history

### ❌ Negative Testing

* Invalid inputs
* Missing token
* Incorrect unit/type

---

## 🐛 Common Issues & Fixes

### ❌ CORS Error

**Fix:**

```java
@CrossOrigin(origins = "http://localhost:3000")
```

---

### ❌ Failed to Fetch

* Backend not running
* Wrong BASE_URL
* CORS not configured

---

### ❌ TypeScript Errors

**Fix:**

```bash
npm install typescript@4.9.5
```

---

### ❌ react-scripts not found

```bash
npm install
```

---

## 🔮 Future Enhancements

* 📈 Graphical analytics (charts)
* 📱 Mobile responsive improvements
* 🔐 OAuth login
* 🌐 Deployment (AWS / Vercel)
* 📊 Advanced history filtering

---

## 📚 Learn More

* React Docs: https://react.dev
* Create React App: https://create-react-app.dev
* TypeScript Docs: https://www.typescriptlang.org

---

## 👨‍💻 Author

**Harshal Choudhary**

* 💻 Java + Spring Boot Developer
* ☁️ Cloud & Full Stack Enthusiast
* 🚀 Building scalable applications

---

## ⭐ Final Note

This frontend is tightly integrated with a **Spring Boot microservices backend**, demonstrating:

✔ Clean architecture
✔ REST API integration
✔ JWT Security
✔ Real-world project structure

---

> 💡 *“Code. Debug. Improve. Repeat.”*
