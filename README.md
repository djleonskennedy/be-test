## Backend Developer Interview Test: Node.js

### Objective:
Create a backend service using Node.js that manages data between multiple tables with various relationships. The service should authenticate requests using an API key and optionally include an authentication mechanism using Self-Sovereign Identity (SSI) based on the Aries framework.

### Requirements:

1. **Setup and Configuration**:
   - Use Node.js with the NestJS framework.
   - Use Prisma as the ORM.

2. **Database Design**:
   - Tables:
     1. `Users`
     2. `Groups`
     3. `Interests`
   - Relationships:
     1. `Users` & `Groups`: Many-to-many relation.
     2. `Users` & `Interests`: One-to-many relation.

3. **Endpoints**:
   - CRUD operations for each table.
   - Endpoint to add a user to a group.
   - Endpoint to remove a user from a group.
   - Endpoint to retrieve all groups for a specific user.
   - Endpoint to retrieve all interests for a specific user.

4. **Authentication**:
   - Simple API Key-based authentication:
     - Requests should include an `x-api-key` header.
     - Store a valid API key in an environment variable.
   - [Bonus] Self-Sovereign Identity (SSI) using the Aries framework:
     - Implement a basic connection protocol.
     - Store DIDs after verification.

5. **Testing**:
   - Unit tests for GET requests:
     - Retrieve a user.
     - Retrieve groups for a user.
     - Retrieve interests for a user.
   - Integration test to simulate adding a user to a group.

### Deliverables:

1. Repository with the backend code.
2. Documentation:
   - Setup instructions.
   - Endpoint descriptions.
   - Additional assumptions or decisions.
3. Postman or equivalent tool setup for testing.

### Evaluation Criteria:

1. **Code Quality**:
   - Clarity and modularity.
   - Error handling.
   - Proper use of async/await.
2. **Database Design**:
   - Normalization.
   - Relationship setup in Prisma.
3. **Authentication**:
   - API key authentication implementation.
   - [Bonus] SSI implementation.
4. **Testing**:
   - Scenario coverage.
   - Test correctness.
5. **Bonus**:
   - NestJS best practices: modules, decorators, and guards.
   - [Bonus] Provide Postman/Insomnia collections for the API.

