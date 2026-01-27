# Relationships between entities
First of all, a good thing that I like and made it so much easier for me to understand the relationships between entities is to have 2 groups of elements:<br>

1️⃣ <h4>Who owns things in Backstage ?</h4><br>
**There could only be two kinds of owners in Backstage, Users and Groups.**<br>
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

2️⃣ What do the owners own ?<br>
Several entities in Backstage can be owned by Users and Groups<br>
**Components**<br>
- Provides one or many **APIs**.<br>
- Can depend on another components.<br>
- Can depend on one or many **Resources**<br>

