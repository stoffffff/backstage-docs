**Backstage is an opensource framework to build and provide internal developer portals.**
# Backstage's features:
- Catalog<br>
- Templates<br>
- Docs<br>
- Search<br>
- Plugins: provide extensibility and customizability<br>

![alt text](screenshots/image.png)

# Backstage's catalog
- A **User** is an entity that represents a member of a certain team or group (developer, business analyst, architect...).<br>
- A **Group** is a representation of one or multiple Users (team) who collaborate to achieve a certain goal inside and organisation.<br>
- A **Component** represents software or a piece of a distributed system that an organisaton wants to keep track of; eg. A Java or flask microservice.<br>
- A **System** is a logical grouping of multiple **APIs** or **Components** that achieve a software's organisational goal. Eg. 3 APIs that manage products in an ecommerce application; An API to upload an new product by an administrator or a warehouse employee, one that allows a customer to buy an product, and one that manages the lifecycle of a product (Available, Out of stock or No longer available).<br>
- A **Domain** is logical representation of entities (Groups and Users) alongside Systems, it represents a business inside an Organisation; eg. The e-banking domain: Teams, Components, APIs, Users...<br>

# Registring components in Backstage
There are various methods in order to fill our catalog in Backstage:<br>
1️⃣​