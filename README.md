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

**Indexing**
	-	Index on the name field for fast product search.
	-	Index on the category field for selecting products by category.
	-	Index on email (unique).
	-	Index on customerId for quick lookup of orders for a specific customer.
	-	Index on orderDate for selecting orders within a specified time range.

<img width="622" alt="Screenshot 2025-03-20 at 21 56 16" src="https://github.com/user-attachments/assets/a90c2244-1b2a-4ca4-b09d-286689e6ba4b" />

**Individual Queries**
- Search for a product by partial name match:
<img width="1079" alt="Screenshot 2025-03-20 at 21 57 56" src="https://github.com/user-attachments/assets/07c81b5a-29ee-4a0c-aafc-f42eb24592c4" />

- Search for products by category.
<img width="1082" alt="Screenshot 2025-03-20 at 21 58 26" src="https://github.com/user-attachments/assets/52bf6930-465b-4e86-a2aa-4e29d982cd01" />

- Retrieve detailed information about a product using its ObjectId.
<img width="1077" alt="Screenshot 2025-03-20 at 21 59 05" src="https://github.com/user-attachments/assets/69ade102-5c0e-4ac9-9f67-6d884e73d4a1" />

- Select all orders for a specific customer.
<img width="1077" alt="Screenshot 2025-03-20 at 21 59 41" src="https://github.com/user-attachments/assets/bd3d8e3e-6701-45cb-b748-da7a08a9c9e8" />

- Retrieve orders within a specified period.
<img width="1081" alt="Screenshot 2025-03-20 at 22 00 15" src="https://github.com/user-attachments/assets/31becdf9-f9a2-4ef3-a39b-58650b20566e" />

- Counting the number of orders with status “delivered”.
<img width="795" alt="Screenshot 2025-03-20 at 22 01 20" src="https://github.com/user-attachments/assets/bb84d42f-e472-4a39-b4c5-b4de8c367986" />

- Calculating the average order amount.
<img width="1009" alt="Screenshot 2025-03-20 at 22 01 41" src="https://github.com/user-attachments/assets/85cedb78-0177-4c04-a403-ff0b58a5c0aa" />

- Updating the order status.
<img width="729" alt="Screenshot 2025-03-20 at 22 02 10" src="https://github.com/user-attachments/assets/54994fc3-e265-441e-b87b-572d1ded2f83" />

- Adding a review to a product.
<img width="1084" alt="Screenshot 2025-03-20 at 22 02 40" src="https://github.com/user-attachments/assets/ece70e5d-4d5b-4c7e-9838-f9acf1af6e3a" />

- Calculating total revenue for each product.
<img width="1078" alt="Screenshot 2025-03-20 at 22 03 08" src="https://github.com/user-attachments/assets/123a56a0-5b43-4ad8-80a5-a567ee3bb032" />
