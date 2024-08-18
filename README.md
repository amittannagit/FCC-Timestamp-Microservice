# Timestamp Microservice

This is a Timestamp Microservice project built as part of the [freeCodeCamp Back End Development and APIs Certification](https://www.freecodecamp.org/learn/back-end-development-and-apis/back-end-development-and-apis-projects/timestamp-microservice).

## Project Overview

The Timestamp Microservice provides an API to convert timestamps in various formats and respond with the corresponding Unix timestamp and natural language date.

### Features

- **Convert Unix Timestamps**: Accepts a Unix timestamp and returns the corresponding natural language date.
- **Convert Natural Language Dates**: Accepts a natural language date and returns the corresponding Unix timestamp.
- **Error Handling**: Handles invalid date formats with appropriate error messages.

## API Endpoints

### GET `/api/timestamp/:date_string`

- **Parameters**:
  - `date_string`: A Unix timestamp or a natural language date string.

- **Example Requests**:
  - `GET /api/timestamp/1450137600`
  - `GET /api/timestamp/December%2015,%202015`

- **Example Responses**:
  - For Unix Timestamp:
    ```json
    {
      "unix": 1450137600,
      "natural": "December 15, 2015"
    }
    ```
  - For Natural Language Date:
    ```json
    {
      "unix": 1450137600,
      "natural": "December 15, 2015"
    }
    ```
  - For Invalid Date Format:
    ```json
    {
      "unix": null,
      "natural": null
    }
    ```

### How It Works

1. **Conversion of Unix Timestamps**: 
   - When a Unix timestamp is provided, the API responds with the corresponding natural language date.

2. **Conversion of Natural Language Dates**:
   - When a natural language date is provided, the API responds with the Unix timestamp and the natural language date.

3. **Error Handling**:
   - If the input is not a valid Unix timestamp or date format, the API responds with `{ "unix": null, "natural": null }`.

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v12 or higher)
- [npm](https://www.npmjs.com/) (comes with Node.js)

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/amittannagit/FCC-Timestamp-Microservice.git
    ```

2. Navigate to the project directory:

    ```bash
    cd FCC-Timestamp-Microservice
    ```

3. Install dependencies:

    ```bash
    npm install
    ```

4. Start the application:

    ```bash
    npm start
    ```

    The server will start and listen on port 3000 or the port specified in the environment variable `PORT`.

## Testing

To test the endpoints, you can use tools like [Postman](https://www.postman.com/) or `curl`.

### Test Cases

1. **Convert Unix Timestamp**:
    - **Request**: `GET /api/timestamp/1450137600`
    - **Expected Response**: `{ "unix": 1450137600, "natural": "December 15, 2015" }`

2. **Convert Natural Language Date**:
    - **Request**: `GET /api/timestamp/December%2015,%202015`
    - **Expected Response**: `{ "unix": 1450137600, "natural": "December 15, 2015" }`

3. **Invalid Date Format**:
    - **Request**: `GET /api/timestamp/invalid-date`
    - **Expected Response**: `{ "unix": null, "natural": null }`

## Deployment

For deploying the application, you can use services like [Heroku](https://www.heroku.com/), [Vercel](https://vercel.com/), or any cloud provider that supports Node.js applications. Ensure to set the `PORT` environment variable if deploying.

## Contributing

Feel free to open issues or submit pull requests to contribute to the project. Follow the standard GitHub workflow for contributing.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
