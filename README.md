# Library REST API Design
## Functional Requirements
- CRUD Operations: The API must support Create, Read, Update, and Delete operations for books, authors, and categories.
- Filtering: The API must allow filtering of books, authors, and categories based on various attributes.
- Pagination: The API must support pagination for listing books, authors, and categories.
- Validation: All inputs must be validated to ensure data integrity (e.g., valid UUIDs, dates, and required fields).

## Non-Functional Requirements
- Security: The API must implement authentication and authorization mechanisms (e.g., OAuth, JWT) to protect data.
- Performance: The API should be optimized for performance, ensuring quick response times, especially for search and listing operations.
- Scalability: The API should be designed to scale horizontally to handle increased load.
- Documentation: The API must be well-documented using tools like Swagger or OpenAPI, providing clear information about endpoints, request/response formats, and error codes.
- Error Handling: The API must provide meaningful error messages and HTTP status codes for client and server errors.
- Consistency: The API must follow RESTful principles and provide consistent resource URIs and HTTP methods.

## Entities
1. Book<br>

    Attributes:<br>
        id: Unique identifier for the book (UUID)<br>
        title: Title of the book<br>
        author_id: Reference to the Author entity (UUID)<br>
        category_id: Reference to the Category entity (UUID)<br>
        published_date: Date when the book was published<br>
        isbn: International Standard Book Number<br>
        summary: Short summary of the book<br>

2. Author<br>

    Attributes:<br>
        id: Unique identifier for the author (UUID)<br>
        name: Name of the author<br>
        biography: Short biography of the author<br>
        birth_date: Date of birth of the author<br>
        death_date: Date of death of the author (nullable)<br>

3. Category<br>

    Attributes:<br>
        id: Unique identifier for the category (UUID)<br>
        name: Name of the category<br>
        description: Description of the category<br>

