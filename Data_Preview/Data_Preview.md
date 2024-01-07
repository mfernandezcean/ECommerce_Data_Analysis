## Composition of Tables:

- ## Fact Table:

### **payment_key:** 
#### Description: An identifier representing the payment transaction associated with the fact.
#### Use Case: This key links to a payment dimension table, providing details about the payment method and related information.
---

### **customer_key:** 
#### Description: An identifier representing the customer associated with the fact.
#### Use Case: This key links to a customer dimension table, providing details about the customer, such as name, address, and other customer-specific information.
---
### **time_key:** 
#### Description: An identifier representing the time dimension associated with the fact.
#### Use Case: This key links to a time dimension table, providing details about the time of the transaction, such as date, day of the week, and month.
---
### **item_key:** 
#### Description: An identifier representing the item or product associated with the fact.
#### Use Case: This key links to an item dimension table, providing details about the product, such as category, sub-category, and product name.
---
### **store_key:** 
#### Description: An identifier representing the store or location associated with the fact.
#### Use Case: This key links to a store dimension table, providing details about the store, such as location, store name, and other store-specific information.
---
### **quantity** 
#### Description: The quantity of items sold or involved in the transaction.
#### Use Case: Represents the amount or number of items associated with the transaction.
---
