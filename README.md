# Petstore-API-Testing
API Testing with Postman scripting for Petstore API Collection

**Overview**
This repository contains a **Postman API collection** for testing the **Swagger Petstore API**. It includes:
- API testing with Postman
- Postman scripting (Pre-request & Test scripts)
- Automation using Newman

**Base URL**

https://petstore.swagger.io/v2

**API Endpoints Overview**

**Pet Endpoints**
| Method | Endpoint | Description |
|--------|----------|-------------|
| 'POST' | '/pet' | Add a new pet |
| 'GET' | '/pet/{petId}' | Retrieve pet details by ID |
| 'PUT' | '/pet' | Update pet details |
| 'DELETE' | '/pet/{petId}' | Remove a pet by ID |
| 'GET' | '/pet/findByStatus?status={status}' | Find pets by status (available, pending, sold) |
| 'GET' | '/pet/findByTags?tags={tag1},{tag2}' | Retrieve pets by tags |

### 🛒 Store (Order) Endpoints
| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/store/order` | Place an order for a pet |
| `GET` | `/store/order/{orderId}` | Retrieve order details by ID |
| `DELETE` | `/store/order/{orderId}` | Cancel an order |
| `GET` | `/store/inventory` | Get pet inventory by status |

### 👤 User Endpoints
| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/user` | Create a new user |
| `POST` | `/user/createWithArray` | Add multiple users using an array |
| `POST` | `/user/createWithList` | Add multiple users using a list |
| `GET` | `/user/{username}` | Get details of a specific user |
| `PUT` | `/user/{username}` | Update user details |
| `DELETE` | `/user/{username}` | Remove a user |
| `GET` | `/user/login?username={username}&password={password}` | User login |
| `GET` | `/user/logout` | User logout |

---

## 🚀 Import & Use in Postman

### Step 1: Import Postman Collection
1. Open **Postman**.
2. Click on **Import**.
3. Select the **Postman Collection JSON file** from this repository.
4. Click **Open** to complete the import.

### Step 2: Set Up an Environment (Optional)
- Create variables for dynamic values (e.g., Pet ID, Order ID).

---

## 🛠️ Postman Scripting (Pre-request & Test Scripts)

### 💡 Pre-request Script Example
```javascript
pm.globals.set("randomUsername", "user_" + Math.floor(Math.random() * 10000));
```

### 💡 Test Script Example
```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

var jsonData = pm.response.json();
pm.globals.set("petId", jsonData.id);
```

---

## 🔄 Running API Tests with Postman Collection Runner
1. Open **Postman**.
2. Click on **Collection Runner**.
3. Select the **Petstore API Collection**.
4. Click **Run** to execute all tests automatically.

---

## 🚀 Running API Tests Using Newman (CLI)
### Step 1: Install Newman
```sh
npm install -g newman
```
### Step 2: Run the Collection
```sh
newman run petstore-collection.json
```

---

## 📢 Keeping Your API Collection Updated

### Weekly Update Process
1. Modify API tests in Postman.
2. Export the **updated Postman Collection (JSON file)**.
3. Upload the updated file to GitHub:
   ```sh
   git add .
   git commit -m "Updated API tests for Petstore"
   git push origin main
   ```

---

## 📌 Setting Up This Repository on GitHub

### Step 1: Create a GitHub Repository
1. Go to [GitHub](https://github.com/) and log in.
2. Click on **New Repository**.
3. Give it a name (e.g., `petstore-api-testing`).
4. Click **Create Repository**.

### Step 2: Upload Your Postman Collection to GitHub
#### Method 1: Upload via GitHub Website
1. Open your repository.
2. Click **Add file > Upload files**.
3. Select the **Postman Collection JSON file**.
4. Click **Commit changes**.

#### Method 2: Upload Using Git (Recommended)
```sh
git clone https://github.com/your-username/petstore-api-testing.git
cd petstore-api-testing
git add .
git commit -m "Added Petstore API Collection"
git push origin main
```

---

## 🔗 Automating API Testing with GitHub Actions (Optional)
Want to **run API tests automatically** using GitHub Actions? Let me know, and I’ll guide you through setting it up! 🚀

---

## 📢 Contributing
- Feel free to **fork this repo** and submit **pull requests**.
- If you find an issue, report it via **GitHub Issues**.

---

### 🚀 Happy API Testing! 🐾


