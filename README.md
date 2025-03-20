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
<img width="1078" alt="Screenshot 2025-03-20 at 22 04 43" src="https://github.com/user-attachments/assets/3ab62b39-c2ad-4843-97f5-09c3f1dfd1a4" />

- Search for products by category:
<img width="1078" alt="Screenshot 2025-03-20 at 22 05 21" src="https://github.com/user-attachments/assets/03b89197-1010-400d-98bc-7b7ce52f3273" />

- Retrieve detailed information about a product using its ObjectId:
<img width="1080" alt="Screenshot 2025-03-20 at 22 05 36" src="https://github.com/user-attachments/assets/d2e6c069-09e2-4d79-8512-7aa441e008c2" />

- Select all orders for a specific customer:
<img width="1078" alt="Screenshot 2025-03-20 at 22 05 54" src="https://github.com/user-attachments/assets/8b1a123c-3f9d-4ab3-8334-ec3ef6cd44df" />

- Retrieve orders within a specified period:
<img width="1080" alt="Screenshot 2025-03-20 at 22 06 18" src="https://github.com/user-attachments/assets/e455dcdd-3d2a-41d8-9659-e3d8785691bc" />

- Counting the number of orders with status “delivered”:
<img width="787" alt="Screenshot 2025-03-20 at 22 06 31" src="https://github.com/user-attachments/assets/5a611773-d5c3-4ed8-ad7d-d0c76be52173" />

- Calculating the average order amount:
<img width="1005" alt="Screenshot 2025-03-20 at 22 06 40" src="https://github.com/user-attachments/assets/fe69c121-492f-457b-950e-1ee4522ea141" />

- Updating the order status:
<img width="725" alt="Screenshot 2025-03-20 at 22 07 08" src="https://github.com/user-attachments/assets/f6c17ea2-581b-48fb-8838-71feb1c6e819" />

- Adding a review to a product:
<img width="1076" alt="Screenshot 2025-03-20 at 22 07 19" src="https://github.com/user-attachments/assets/46c55de9-b4ee-4dce-95de-85d391d43334" />

- Calculating total revenue for each product:
<img width="1077" alt="Screenshot 2025-03-20 at 22 07 31" src="https://github.com/user-attachments/assets/d8d7e806-b80c-4c9c-9ef4-a313e1d7384c" />
