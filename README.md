# exercisetracker

# Exercise Tracker

### Key Features

- **User Management:**
  - Create new users or retrieve existing ones with a simple API endpoint.

- **Exercise Logging:**
  - Log exercises for specific users, including details like description, duration, and date.

- **Data Retrieval:**
  - Retrieve user information and exercise logs through dedicated API endpoints.

- **Responsive Web Interface:**

## API Endpoints



- **POST /api/users**
  - Description: Create a new user or retrieve an existing one.
  - Input:
    - `username`: String
  - Output:
    - `username`: String
    - `_id`: String

- **GET /api/users**
  - Description: Retrieve a list of all users.
  - Output:
    - `username`: String
    - `_id`: String

- **POST /api/users/:_id/exercises**
  - Description: Add exercise for a specific user.
  - Input:
    - `description`: String
    - `duration`: Number
    - `date` (optional): Date
  - Output:
    - `username`: String
    - `_id`: String
    - `description`: String
    - `duration`: Number
    - `date`: String

- **GET /api/users/:_id/logs**
  - Description: Retrieve exercise logs for a specific user.
  - Query Parameters:
    - `from` (optional): Date
    - `to` (optional): Date
    - `limit` (optional): Number
  - Output:
    - `username`: String
    - `_id`: String
    - `count`: Number
    - `log`: Array
