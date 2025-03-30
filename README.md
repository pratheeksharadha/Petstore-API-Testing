# Petstore-API-Testing
API Testing with Postman scripting for Petstore API Collection

**Overview**
This repository contains a **Postman API collection** for testing the **Swagger Petstore API**, an open API used for practice. It includes:
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

**Store (Order) Endpoints**
| Method | Endpoint | Description |
|--------|----------|-------------|
| 'POST' | '/store/order' | Place an order for a pet |
| 'GET' | '/store/order/{orderId}' | Retrieve order details by ID |
| 'DELETE' | '/store/order/{orderId}' | Cancel an order |
| 'GET' | '/store/inventory' | Get pet inventory by status |

**User Endpoints**
| Method | Endpoint | Description |
|--------|----------|-------------|
| 'POST' | '/user' | Create a new user |
| 'POST' | '/user/createWithArray' | Add multiple users using an array |
| 'POST' | '/user/createWithList' | Add multiple users using a list |
| 'GET' | '/user/{username}' | Get details of a specific user |
| 'PUT' | '/user/{username}' | Update user details |
| 'DELETE' | '/user/{username}' | Remove a user |
| 'GET' | '/user/login?username={username}&password={password}' | User login |
| 'GET' | '/user/logout' | User logout |

