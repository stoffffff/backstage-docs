# Relationships between entities
First of all, a good thing that I like and made it so much easier for me to understand the relationships between entities is to have 2 groups of elements:<br>

### 1️⃣Who owns things in Backstage ?<br>
#### There could only be two kinds of owners in Backstage, Users and Groups.<br>
- You guessed it right, a Group can have multiple Users.<br>
- A User can be part of one or multiple Groups.<br>
- A Group can have one parent and many childs.<br>
- A Group could be a [team, business unit, product-area, root].<br>

*Let's put a use-case into action*<br>
*- Creating a Parent Group 'technical-department'<br>*
*- Creating a  Child Group 'developers' member of 'technical-department'<br>*
*- Creating a User 'Marcos' member of 'developers'*<br>

![alt text](screenshots/relationships.png)

**Let's check them up in Backstage's catalog**<br>

![alt text](screenshots/relationships1.png)

**Let's check the "developers" group**<br>

![alt text](screenshots/relationships2.png)

**Let's check the "technical-department" group**<br>

![alt text](screenshots/relationships3.png)

**Let's filter to Users an check "Marcos"**<br>

![alt text](screenshots/relationships4.png)

All set up as expected!

### 2️⃣ What do the owners own ?<br>
#### Several entities in Backstage can be owned by Users and Groups:<br>
##### Components:<br>
- Can Provide one or many **APIs**.<br>
- Can Consume one or many **APIs**.<br>
- Can depend on another components.<br>
- Can depend on one or many **Resources**.<br>
- Belongs to a **System**.<br>

##### APIs:<br>
- Is provided by a **Component**.<br>
- Is consumed by another **Component**.<br>
- Belongs to a **System**.<br>

##### Example:<br>
###### In this example, the component "example-website" provides a gRPC API called "example-grpc-api". They are both owned by the "guests" team.<br>

![alt text](screenshots/component-api.png)

##### Resource:<br>
- The physical or virtual infrastructure that your software depends on to run.<br>

![alt text](screenshots/resource.png)

##### System:<br>
- A collection of entities (components, APIs, etc.) that work together to perform a specific function.<br>

![alt text](screenshots/system.png)

##### Domain:<br>
- The highest level of organization. It represents a large functional area of your business or a major "problem space".<br>

![alt text](screenshots/domain.png)









