# API-Automation-Postman

API Automated test suite using Postman JavaScript Test Cases

# Contact List API Test Cases

This repository contains a collection of positive and negative test cases for the Contact List API. The test cases are organized using the Postman testing framework and are written in JavaScript.

## Table of Contents

- [Introduction](#introduction)
- [Test Cases](#test-cases)
  - [Positive Testing](#positive-testing)
  - [Negative Testing](#negative-testing)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The Contact List API test cases cover various scenarios for testing the functionality of the API endpoints. These test cases are written using the Postman testing framework, which allows us to automate the process of sending requests to the API and verifying the responses.

## Test Cases

### Positive Testing

This section contains positive test cases that cover successful scenarios of using the API.

#### Login

- Tests the login functionality by sending a POST request with user credentials.
- Sets the authentication token in the environment variable for subsequent requests.

#### All Contacts

- Tests fetching all contacts by sending a GET request.
- Verifies that the response status code is 200.

#### Add Contact

- Tests adding a new contact by sending a POST request with contact details.
- Sets the contact ID in the environment variable for later reference.
- Verifies that the response status code is 201.

#### Get Contact ID

- Tests fetching a specific contact by sending a GET request with the contact ID.
- Verifies that the response status code is 200.
- Checks that the correct email, first name, and last name are returned in the response.

#### Update Contact

- Tests updating an existing contact by sending a PUT request with updated details.
- Verifies that the response status code is 200.

#### Delete Contact

- Tests deleting a contact by sending a DELETE request with the contact ID.
- Verifies that the response status code is 200.

### Negative Testing

This section contains negative test cases that cover error scenarios of using the API.

#### All Contacts Unauthorized

- Tests fetching all contacts without proper authentication.
- Verifies that the response status code is 401.

#### Get Contact ID Not Found

- Tests fetching a non-existent contact by sending a GET request with an invalid contact ID.
- Verifies that the response status code is 404.

#### Add Contact Missing Field

- Tests adding a contact with missing required fields by sending a POST request.
- Verifies that the response status code is 400.
- Checks that the response includes an error message about the missing field.

#### Add Contact Too Many Characters

- Tests adding a contact with a field exceeding the maximum allowed characters by sending a POST request.
- Verifies that the response status code is 400.

#### Update Contact Invalid Format

- Tests updating a contact with invalid data format by sending a PUT request.
- Verifies that the response status code is 400.

#### Tear Down Contact

- Tests deleting a contact created during testing.
- Verifies that the response status code is 200.
- Checks that the response time is within an acceptable limit.

## Prerequisites

Before running these test cases, ensure you have the following:

- Postman installed on your machine.
- Access to the Contact List API endpoints to perform the testing.

## Getting Started

1. Clone this repository to your local machine.
2. Open Postman and import the collection using the provided JSON file.
3. Modify the collection variables, such as `{{url}}`, according to your API endpoints.

## Usage

1. Open the imported collection in Postman.
2. Select the desired test suite (Positive Testing or Negative Testing).
3. Run the entire test suite or individual test cases.

## Contributing

Contributions are welcome! If you find any issues or want to add more test cases, feel free to open a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
