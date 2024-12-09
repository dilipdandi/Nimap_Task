Java-Machine-Test--Nimap-Task
Spring Boot Setup:
Spring Boot simplifies the development of stand-alone, production-ready Spring-based applications. Start by creating a Spring Boot project using Spring Initializr or your favorite IDE.
Ensure to include dependencies such as Spring Web, Spring Data JPA, and a database driver (e.g., H2, MySQL, or PostgreSQL).

REST Controllers:
Develop REST controllers to manage CRUD operations for categories and products.
Use annotations like @GetMapping, @PostMapping, @PutMapping, and @DeleteMapping to define API endpoints.

Database Configuration (RDBMS):
Configure database connectivity in your application.properties or application.yml file.
Opt for an RDBMS like MySQL, PostgreSQL, or H2 (for local testing).

Annotation-Based Configuration:
Spring Boot encourages annotation-based configuration over XML.
Use annotations like @Entity, @Table, @Column, and @OneToMany to define your data model and relationships.
Category CRUD Operations:

Implement the following APIs for categories:
GET /api/categories?page=3: Retrieve all categories (with pagination).
POST /api/categories: Create a new category.
GET /api/categories/{id}: Retrieve a category by ID.
PUT /api/categories/{id}: Update a category by ID.
DELETE /api/categories/{id}: Delete a category by ID.
Product CRUD Operations:

Implement similar APIs for products:
GET /api/products?page=2: Retrieve all products (with pagination).
POST /api/products: Create a new product.
GET /api/products/{id}: Retrieve a product by ID.
PUT /api/products/{id}: Update a product by ID.
DELETE /api/products/{id}: Delete a product by ID.
One-to-Many Relationship:

Define a one-to-many relationship between categories and products.
Annotate the appropriate fields in your entities (e.g., @OneToMany in the Category entity).
Server-Side Pagination:

Implement server-side pagination by using query parameters (e.g., page, size, sort).
In your repository, use methods like findAll(Pageable pageable) to retrieve paginated results.
Fetching Product Details with Category:

When fetching a single product, ensure that the response includes the relevant category details.
You can use DTOs (Data Transfer Objects) to customize the response format.
