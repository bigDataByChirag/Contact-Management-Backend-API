# Contact Management Backend API

The Contact Management Backend API is a powerful and scalable Node.js application designed to simplify contact management for individuals and businesses. It provides a robust set of RESTful API endpoints to handle user authentication, user registration, and various CRUD operations (Create, Read, Update, Delete) on contacts. This backend API is built with the Express.js framework and utilizes MongoDB with Mongoose for data storage and modeling.

## Features

### User Authentication and Registration

The API offers user authentication and registration functionality to ensure secure access to the application. The features include:

- **User Registration**: New users can create an account by providing a unique username, valid email address, and strong password. The API hashes the password using bcrypt for security.
- **Email Uniqueness Check**: The API verifies the uniqueness of the provided email address during user registration to prevent duplicate accounts.
- **User Login**: Registered users can log in using their email and password. Upon successful login, the API generates a JSON Web Token (JWT) to be used for future authenticated requests.
- **JWT-Based Authentication**: All protected routes in the API require a valid JWT in the Authorization header to ensure that only authenticated users can access them.

### Contact Management Operations

The API enables users to manage their contacts efficiently, offering the following functionalities:

- **Create Contacts**: Authenticated users can create new contacts by providing a name, email address, and phone number. Each contact is associated with the user who created it.
- **Retrieve Contacts**: Users can fetch all their contacts or view a specific contact by providing its unique ID. The API ensures data privacy, allowing users to access only their contacts.
- **Update Contacts**: Users can update the information of their existing contacts, such as the name, email address, or phone number, ensuring their address book remains up-to-date.
- **Delete Contacts**: Authenticated users have the option to delete contacts they no longer need, streamlining their contact list management.

### Error Handling and Middleware

The API incorporates a robust error handling mechanism to ensure smooth operation and consistent responses. It includes the following features:

- **Error Handling Middleware**: The application employs a middleware to handle errors gracefully. It categorizes errors based on their HTTP status codes and sends appropriate error messages to the client.
- **JWT Validation Middleware**: To protect certain routes from unauthorized access, the API uses middleware to validate JWTs. This ensures that only authenticated users can access protected routes, ensuring data security and user privacy.

## Installation

Follow these steps to set up and run the Contact Management Backend API on your local machine:

1. Clone the repository:

```bash
git clone https://github.com/your-username/Contact-Management-Backend-API.git
cd Contact-Management-Backend-API
```

2. Install the dependencies:

```bash
npm install
```

3. Configure MongoDB Connection:
   - Make sure you have MongoDB installed and running locally or provide the MongoDB connection URI in a configuration file (e.g., "config.js").

4. Set Environment Variables:
   - Create a `.env` file in the root of the project and define the following variables:
     ```
     ACCESS_TOKEN_SECRET=your-secret-key
     ```

5. Run the application:

```bash
npm start
```

The API will be accessible at `http://localhost:5000`.

## Usage

After successfully setting up and running the API, you can interact with it using various HTTP clients, such as `curl`, Postman, or through your front-end application. Before accessing any protected routes, ensure you obtain a valid JWT by registering or logging in as a user.

Please refer to the API documentation for detailed information about each endpoint, including request formats, response data, and authentication requirements.

Thank you for exploring the Contact Management Backend API! ~ **Chirag Singh**
