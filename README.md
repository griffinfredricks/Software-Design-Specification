# Elder Care

## Team Members:
- Layth Oro
- Griffin Fredricks
- Nathan Maayah
- Jaecob Adajar

---

## System Description

### Brief Overview of System:
ElderCare is a comprehensive software solution designed to empower elderly individuals residing in nursing homes to order essential items with ease. The system allows elders to place orders for various items through a user-friendly interface, and these orders are delivered directly to their location within the nursing home. This system ensures that the elderly have timely and convenient access to the items they need, enhancing their comfort and well-being.


## UML Class Descriptions
1. User Class: 
Attributes:
userID (int): A unique identifier for each user. 
name (String): The name of the user. 
roomNumber (int): The room number where the user resides within the nursing home. 
Methods: 
placeOrder(itemID: int, quantity: int): Allows the user to place an order by specifying the item ID and quantity. 

3. Item Class: 
Attributes: 
itemID (int): A unique identifier for each item. 
itemName (String): The name of the item. 
price (double): The price of the item. 
Methods: 
checkAvailability() -> bool: Checks whether the item is available in the inventory. 

4. Order Class: 
Attributes: 
orderID (int): A unique identifier for each order. 
userID (int): The ID of the user who placed the order. 
itemList (List): A list of items and quantities ordered. 
Methods: 
calculateTotal() -> double: Calculates the total price of the order. 
processOrder(): Processes the order for delivery. 

5. Delivery Class: 
Attributes: 
deliveryID (int): A unique identifier for each delivery. 
orderID (int): The ID of the order to be delivered. 
Methods: 
scheduleDelivery(): Schedules the delivery of the order. 
completeDelivery(): Marks the delivery as complete. 

6. Inventory Class: 
Attributes: 
inventoryID (int): A unique identifier for the inventory. 
items (List): A list of items available in the inventory. 
Methods: 
updateInventory(itemID: int, quantity: int): Updates the inventory by adding or removing items based on the item ID and quantity. 

7. Notification Class: 
Attributes: 
notificationID (int): A unique identifier for each notification. 
userID (int): The ID of the user to whom the notification is sent. 
message (String): The content of the notification. 
type (String): The type of notification. 
status (String): The status of the notification. 
dateSent (Date): The date the notification was sent. 
Methods: 
sendNotification(): Sends a notification to the user. 
markAsRead(): Marks the notification as read. 

8. Admin Class: 
Attributes: 
adminID (int): A unique identifier for each admin. 
name (String): The name of the admin. 
Methods: 
manageInventory(): Allows the admin to manage the inventory. 
manageOrders(): Allows the admin to manage orders. 

9. Feedback Class: 
Attributes: 
feedbackID (int): A unique identifier for each feedback. 
userID (int): The ID of the user who gives the feedback. 
message (String): The content of the feedback. 
rating (int): The rating given in the feedback. 
category (String): The category of the feedback. 
response (String): The response to the feedback. 
Methods: 
submitFeedback(): Allows the user to submit feedback regarding the service. 
respondToFeedback(): Allows the admin to respond to the feedback. 

9. Address Class: 
Attributes: 
addressID (int): A unique identifier for each address. 
userID (int): The ID of the user associated with the address. 
street (String): The street name. 
city (String): The city name. 
state (String): The state name. 
zipCode (String): The zip code. 
country (String): The country name. 

10. Payment Class: 
Attributes: 
paymentID (int): A unique identifier for each payment. 
userID (int): The ID of the user making the payment. 
paymentMethod (String): The method of payment. 
amount (double): The amount of the payment. 
transactionDate (Date): The date of the transaction. 
Methods: 
processPayment(): Processes the payment. 
refund(): Issues a refund. 

11. Cart Class: 
Attributes: 
cartID (int): A unique identifier for each cart. 
userID (int): The ID of the user who owns the cart. 
items (List): A list of items in the cart. 
Methods: 
addItem(itemID: int): Adds an item to the cart. 
removeItem(itemID: int): Removes an item from the cart. 
checkout(): Proceeds to checkout for payment and order placement. 


## Development Plan and Timeline 
Development Plan and Timeline:
Partitioning of Tasks:
1. Project Initialization:
Task: Project Kick-off Meeting
Duration: 3 day
Responsible: All team members (Layth, Nathan, Griffin, Jaecob)
2. Requirement Gathering:
Task: User Requirement Analysis
Duration: 5 days
Responsible: Layth, Nathan
Task: System Requirement Analysis
Duration: 5 days
Responsible: Griffin, Jaecob
3. System Design:
Task: Database Design
Duration: 7 days
Responsible: Nathan
Task: System Architecture Design
Duration: 9 days
Responsible: Griffin
Task: User Interface Mockups
Duration: 4 days
Responsible: Layth
4. Development Phase:
Task: Backend Development
Duration: 14 days
Responsible: Jaecob, Nathan
Task: Frontend Development
Duration: 11 days
Responsible: Layth, Griffin
Task: Integration of Frontend and Backend
Duration: 8 days
Responsible: Griffin, Jaecob
5. Testing Phase:
Task: Unit Testing
Duration: 7 days
Responsible: Nathan
Task: System Testing
Duration: 6 days
Responsible: Layth
Task: User Acceptance Testing
Duration: 5 days
Responsible: All team members
6. Deployment:
Task: Deployment to Production Environment
Duration: 4 days
Responsible: Jaecob
7. Feedback & Iteration:
Task: Collect User Feedback
Duration: 7 days
Responsible: Layth
Task: Iterative Improvements based on Feedback
Duration: 7 days
Responsible: Griffin, Nathan
8. Documentation & Training:
Task: System Documentation
Duration: 6 days
Responsible: Jaecob, Layth
Task: User Training Sessions
Duration: 5 days
Responsible: Nathan, Griffin
9. Project Closure:
Task: Final Review Meeting
Duration: 7 day
Responsible: All team members
Task: Project Documentation & Handover
Duration: 7 days
Responsible: Layth, Jaecob

### Gantt Chart
<img width="1286" alt="Screen Shot 2023-10-04 at 5 58 18 PM" src="https://github.com/griffinfredricks/Software-Design-Specification/assets/67619675/fc9291dc-c1fc-4afa-9f7e-3b917aa67992">

