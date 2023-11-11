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

## Software Architecture Overview
# Architectural Diagram of All Major Components:
![0002](https://github.com/griffinfredricks/Software-Design-Specification/assets/91572119/11f0cb71-f8b1-4ce9-bb2c-c835f22e2dc0)


## UML Diagram
![0001](https://github.com/griffinfredricks/Software-Design-Specification/assets/91572119/daedbd6c-0a0a-4f44-aac9-61eb1a10e6bb)


## UML Class Descriptions
<pre>
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
</pre>

## Development Plan and Timeline 
<pre>

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
</pre>

### Gantt Chart
<img width="1286" alt="Screen Shot 2023-10-04 at 5 58 18 PM" src="https://github.com/griffinfredricks/Software-Design-Specification/assets/67619675/b71798b9-f931-42ae-9c42-00c6c6e1fd08">

## Verification Test Plan

# 1. Unit Testing:
**Test Set 1: Functionality Testing**
- **Test 1.1: `placeOrder` Method in `User` Class**
  - **Objective**: Ensure that the `placeOrder` method correctly places an order and updates the user’s order history.
  - **Test Data**: Valid item IDs, user details.
  - **Code Example**: 
    ```cpp
    User user("John Doe");
    Order order = user.placeOrder({"item1", "item2"});
    assert(user.orderHistoryContains(order));
    ```
  - **Expected Result**: The order is placed successfully, and the user’s order history is updated.
    
- **Test 1.2: `calculateTotal` Method in `Order` Class**
  - **Objective**: Verify that the `calculateTotal` method accurately calculates the total price of the order.
  - **Test Data**: List of items with known prices.
  - **Code Example**: 
    ```cpp
    Order order({"item1", "item2"});
    double total = order.calculateTotal();
    assert(total == 15.00); // Assuming item1 is $10 and item2 is $5
    ```
  - **Expected Result**: The total price is calculated correctly.
  - #### 2. Functional Testing: 
**Test Set 1: Feature Testing** 
- **Test 1.1: Order Placement Process** 
  - **Objective**: Test the entire order placement process from start to finish. 
  - **Test Steps**:  
    1. User logs in. 
    2. User places an order. 
    3. User receives a confirmation. 
  - **Code Example**:  
    ```cpp 
    User user("John Doe"); 
    Order order = user.placeOrder({"item1", "item2"}); 
    Confirmation confirmation = order.processOrder(); 
    assert(confirmation.getStatus() == "Confirmed"); 
    ``` 
  - **Expected Result**: The order is placed successfully, and a confirmation is received. 

- **Test 1.2: Feedback Submission Process** 
  - **Objective**: Ensure that the feedback submission process works correctly. 
  - **Test Steps**:  
    1. User submits feedback. 
    2. Feedback is stored in the database. 
  - **Code Example**:  
    ```cpp 
    User user("John Doe"); 
    Feedback feedback = user.submitFeedback("Everything was great!"); 
    assert(feedback.getStatus() == "Stored"); 
    ``` 
  - **Expected Result**: Feedback is submitted and stored correctly. 

**Test Set 2: Integration Testing** 
- **Test 2.1: Integration between `Order Processing` and `Inventory Management`** 
  - **Objective**: Ensure that the inventory is updated correctly after an order is placed. 
  - **Test Steps**:  
    1. User places an order. 
    2. Inventory is checked and updated. 
  - **Code Example**:  
    ```cpp 
    Inventory inventory; 
    int initialStock = inventory.getStock("item1"); 
    Order order({"item1"}); 
    order.processOrder(); 
    int finalStock = inventory.getStock("item1"); 
    assert(finalStock == initialStock - 1); 
    ``` 
  - **Expected Result**: Inventory is updated correctly. 

- **Test 2.2: Integration between `Order Processing` and `Delivery Management`** 
  - **Objective**: Ensure that deliveries are scheduled correctly after an order is placed. 
  - **Test Steps**:  
    1. User places an order. 
    2. Delivery is scheduled. 
  - **Code Example**:  
    ```cpp 
    Order order({"item1"}); 
    Delivery delivery = order.scheduleDelivery(); 
    assert(delivery.getStatus() == "Scheduled"); 
    ``` 
  - **Expected Result**: Delivery is scheduled correctly.
 
**Test Set 3: System Testing**
- **Test Set 1: End-to-End Testing**
- **Test 1.1: Complete System Test**
  - **Objective**: Ensure that all components of the ElderCare system work together seamlessly.
  - **Test Steps**: 
    1. User logs in
    2. User places an order
    3. Order is processed, and delivery is scheduled
    4. User receives a confirmation
  - **Code Example**: 
    ```cpp
    User user("John Doe");
    Order order = user.placeOrder({"item1", "item2"});
    Delivery delivery = order.scheduleDelivery();
    Confirmation confirmation = order.processOrder();
    assert(confirmation.getStatus() == "Confirmed");
    assert(delivery.getStatus() == "Scheduled");
    ```
  - **Expected Result**: The entire process from order placement to confirmation works seamlessly.
  
- **Test 1.2: High Load Performance Test**
  - **Objective**: Test the system’s performance under high load to ensure stability.
  - **Test Steps**: 
    1. Simulate a large number of users placing orders simultaneously.
  - **Code Example**: 
    ```cpp
    std::vector<User> users;
    for (int i = 0; i < 1000; ++i) {
      users.push_back(User("User " + std::to_string(i)));
      users[i].placeOrder({"item1", "item2"});
    }

  - **Expected Result**: The system remains stable and responsive

 **Test Set 2: Security and Data Integrity Testing**
- **Test 2.1: Security Measures Test**
  - **Objective**: Ensure that the system’s security measures are effective in protecting user data.
  - **Test Steps**: 
    1. Attempt to access or modify user data without proper authorization.
  - **Code Example**: 
    ```cpp
    User unauthorizedUser("Hacker");
    try {
      unauthorizedUser.accessUserData("John Doe");
    } catch (const std::security_error& e) {
      assert(strcmp(e.what(), "Unauthorized access") == 0);
    }
    ```
  - **Expected Result**: Unauthorized access or modification is prevented.
  
- **Test 2.2: Data Integrity Test**
  - **Objective**: Ensure that no data is lost or corrupted during transactions.
  - **Test Steps**: 
    1. Place an order and check the integrity of the data stored in the database.
  - **Code Example**: 
    ```cpp
    User user("John Doe");
    Order order = user.placeOrder({"item1", "item2"});
    order.processOrder();
    assert(checkDataIntegrity(order));
    ```
  - **Expected Result**: Data integrity is maintained.





**Our SQL Database Choice:**
- **Structured Schema:** We chose a relational database due to
the clear relationships in our data, such as users placing
orders and orders containing items. This structure is a key
feature of relational databases.
- **ACID Compliance:** We prioritized transactional integrity,
ensuring Atomicity, Consistency, Isolation, and Durability,
especially vital in systems handling orders and payments.
- **Complex Queries:** We recognized the need for complex
queries, like joining multiple tables to link orders with users
and items, which SQL databases handle efficiently

