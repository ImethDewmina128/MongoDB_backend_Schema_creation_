# MongoDB School Van Backend

This is a backend API for a School Van management system, built with **Node.js**, **Express**, and **MongoDB**.  
It currently handles submitting driver ratings.

---

## ⭐ Prerequisites

Before running this project, ensure you have the following installed:

- **Node.js** (v14 or higher)  
- **MongoDB Community Server**

---

## 📥 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/imethdewmina128/MongoDB_school_van_backend.git
   ```

2. Navigate to the project directory:
   ```bash
   cd MongoDB_school_van_backend
   ```

3. Install dependencies:
   ```bash
   npm install
   ```

---

## ⚙️ Configuration

Ensure your **MongoDB server is running locally** on the default port **27017**.

If MongoDB is not running, start it with:

```bash
# Run in Command Prompt as Administrator
net start MongoDB
```

---

## 🚀 Start the Server

```bash
node server.js
```

You should see:

```
Successfully connected to MongoDB!
Server is running on http://localhost:3000
```

---

## 📌 API Endpoints

### **1. Submit Driver Rating**

**URL:** `/api/driver/details`  
**Method:** `POST`  
**Content-Type:** `application/json`

---

### 📤 **Request Body Example**

```json
{
  "driver_id": 345,
  "driver_name": "Wasamtha",
  "driver_age": 35,
  "parent_id": 215,
  "rating_score": 9,
  "comment": "Great service."
}
```

---

### 📋 **Request Body Fields**

| Field         | Type    | Description                                           |
|---------------|---------|-------------------------------------------------------|
| driver_id     | Number  | Required. Unique ID of the driver.                   |
| driver_name   | String  | Required. Name of the driver.                        |
| driver_age    | Number  | Required. Age of the driver.                         |
| parent_id     | Number  | Required. ID of the parent submitting the rating.    |
| rating_score  | Number  | Required. Score between **1 and 11**.                |
| comment       | String  | Optional. Additional feedback.                       |

---

## ✅ Success Response

**Code:** `201 Created`

```json
{
  "success": true,
  "message": "Rating submitted successfully!"
}
```

---

## ❌ Error Response

**Code:** `500 Internal Server Error`

```json
{
  "success": false,
  "message": "Failed to submit rating.",
  "error": "Error message details..."
}
```

---

## 📘 Notes

- Ensure MongoDB is running before starting the backend.
- All requests must be sent in JSON format.

---

## 📄 License

This project is open-source and available for use.

