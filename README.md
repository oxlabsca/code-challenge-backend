# **Backend Coding Challenge Requirements**

## **Overview**

Welcome to the Backend Coding Challenge! This challenge is designed to assess your skills in building a RESTful API with authentication, working with PostgreSQL databases, containerization with Docker, documentation with Swagger, and more. Please read through all sections carefully and complete the tasks as specified.

---

## **Stack**
You can go with any of the below stack of your choice!

1. Node: `NestJs` or `ExpressJs`, `Postgres`, `Swagger`
2. Python: `FastAPI`, `Postgres`, `Swagger`

---

## **Challenge Sections**

### **1. Database Design and Query Optimization**

#### **Objective**
Design a schema for a hypothetical e-commerce platform where:
- Customers can place orders.
- Each order may have multiple items, and each item can appear in multiple orders.
- Customers can get orders status

#### **Requirements**
1. Create tables for the following entities:
   - **Customer**: Stores customer details.
   - **Order**: Contains order details with references to customers.
   - **OrderItem**: Links products to orders.
   - **Product**: Contains product information.
   
2. Design queries to:
   - Retrieve orders by customer.
   - Fetch the most recent orders.
   - Find the most frequently ordered products.
   - Retrieve the order status by order id

#### **Evaluation Criteria**
- **Normalization**: Tables should be normalized without over-normalization.
- **Indexing**: Use indexes to optimize frequent queries.
- **Query Performance**: Queries should be efficient and performant.
- **Documentation**: Provide a brief explanation for schema and indexing choices.

---

### **2. API Design and Rate Limiting**

#### **Objective**
Implement a REST API service with rate limiting.

#### **Requirements**
1. Implement the following endpoints in Section 3:
   
2. Implement **rate limiting**:
   - Free-tier users: 10 requests per minute.
   - Premium-tier users: 50 requests per minute.
   
3. Store usage metrics per user in the database for tracking purposes.

#### **Evaluation Criteria**
- **Rate-Limiting Logic**: Effective rate-limiting implementation.
- **Scalability**: Solution scalability for many users.
- **Code Organization**: Modular code structure, with rate limiting separated from business logic.

---

### **3. Security-Focused API Task: Role-Based Access Control (RBAC)**

#### **Objective**
Implement Role-Based Access Control (RBAC) for above designed e-commerce platform.

#### **Requirements**
1. Create roles and permissions:
   - **Admin**: View, edit, delete orders.
   - **Editor**: View and edit orders.
   - **Viewer**: Only view orders.
   
2. Implement endpoints:
   - `POST /order`: Create a new order.
   - `GET /order/{id}`: View an order.
   - `PUT /order/{id}`: Edit an order.
   - `DELETE /order/{id}`: Delete an order.
   - `GET /order?id=<id>`: Returns order status by order id.

3. **JWT-based Authentication**: Secure all endpoints using JWT tokens, and enforce role-based access control.

#### **Evaluation Criteria**
- **RBAC Implementation**: Correct roles and permissions enforcement.
- **Security Practices**: Proper handling of JWT tokens and permissions.
- **Code Quality**: Modular code and documentation.

---

### **4. Docker and CI/CD Pipeline Task** (Optional: will add bonus points)

#### **Objective**
Containerize a service and set up a CI/CD pipeline.

#### **Requirements**

1. Write a `Dockerfile` to containerize the application.

2. Set up a CI/CD pipeline:
   - Steps should include code linting, running tests, building a Docker image, and deploying to a Docker registry.

#### **Evaluation Criteria**
- **Docker Knowledge**: Efficient `Dockerfile` structure.
- **CI/CD Pipeline**: Complete and functional pipeline with automated steps.
- **Deployment Automation**: Automation in CI/CD pipeline for deployment.

---

## **General Requirements**

1. **Swagger Documentation**: Provide Swagger (or equivalent) API documentation accessible at `/docs`.
2. **Authentication**: Use JWT for authentication across all endpoints that require authorization.
3. **Data Validation and Error Handling**: Ensure request data validation and handle errors gracefully.
4. **Docker Setup**: Include a `Dockerfile` and `docker-compose.yml` file for easy setup.

---

## **Deliverables**

- **Code Repository**: Structured and easy-to-navigate code.
- **Dockerized Setup**: `docker-compose up` should start the API and the database. (Optional)
- **API Documentation**: Accessible API documentation via Swagger.
- **README.md**: Instructions on:
   - Running the application
   - Testing the API endpoints with Swagger
   - Running any unit tests

---

## **Submission Guidelines**

- Please submit a link to a public repository with your solution.
- Ensure all instructions are in `README.md` for setup and usage.
- Provide explanations for any unique design or architectural choices in your solution.

---

## **Evaluation Criteria**

1. **Code Quality**: Structure, readability, and adherence to best practices.
2. **Functionality**: Completeness of API endpoints, role-based access control, rate limiting, and other core features.
3. **Documentation**: Completeness and clarity of Swagger documentation.
4. **Bonus**:
   - Docker and CI/CD (if implemented).
   - Test coverage, especially for security-related code.

---

Good luck, and we look forward to reviewing your solution!