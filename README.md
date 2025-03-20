![408850848-c050980d-4c70-47e6-bafe-d05ae55eeab6 (2)](https://github.com/user-attachments/assets/6d295409-e9ca-4ea9-920f-45a335d250a1)

**Project Goal**: Design and implement a non-relational database using MongoDB for an online electronics store, where customers can place orders with home delivery. The database should account for the product range, customer data, orders, and also provide the capability for sales analysis and handling reviews.

**Main Collections**
***Customers:***
- _id (unique customer identifier)
- address
- email
- name
- phone
- registrationDate (registration date)
***Products:***
- _id (unique product identifier)
- category
- description
- name (product name)
- price
- reviews
- stock
- specifications (technical specifications)
***Orders:***
- _id (unique order identifier)
- customerId (reference to the customer document)
- items (order items with quantity and price at the time of purchase)
- orderDate (order date)
- status
- totalAmount (total order amount)
- deliveryDate (expected/actual delivery date)

**DB Diagram:**

<img width="567" alt="Screenshot 2025-03-20 at 21 39 55" src="https://github.com/user-attachments/assets/406046b8-edbc-41d8-b8dd-67d97cc331c4" />
