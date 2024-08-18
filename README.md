# Timestamp Microservice

This is a Timestamp Microservice project built as part of the [freeCodeCamp Back End Development and APIs Certification](https://www.freecodecamp.org/learn/back-end-development-and-apis/back-end-development-and-apis-projects/timestamp-microservice).

## Project Overview

The Timestamp Microservice API accepts a date as a parameter, and returns both a Unix timestamp and a UTC string representation of the date. If no date is provided, the API returns the current timestamp.

### Features

- **Unix Timestamp Conversion**: Converts a date string to a Unix timestamp.
- **UTC String Conversion**: Converts a date string to a UTC string.
- **Current Date**: Returns the current Unix timestamp and UTC string if no date is provided.
- **Error Handling**: Returns an error message if the date is invalid.

## API Endpoints

### GET `/api/:date?`

- **Parameters**:
  - `date` (optional): A date string in a valid format (e.g., `YYYY-MM-DD`, `1450137600000`).
  
- **Responses**:
  - **Valid Date**:
    ```json
    {
      "unix": 1451001600000,
      "utc": "Fri, 25 Dec 2015 00:00:00 GMT"
    }
    ```
  - **Invalid Date**:
    ```json
    {
      "error": "Invalid Date"
    }
    ```
  - **No Date Provided**:
    ```json
    {
      "unix": 1627878983000,
      "utc": "Sat, 01 Aug 2021 00:00:00 GMT"
    }
    ```

### Examples

- `/api/2015-12-25` returns `{ "unix": 1451001600000, "utc": "Fri, 25 Dec 2015 00:00:00 GMT" }`
- `/api/1451001600000` returns `{ "unix": 1451001600000, "utc": "Fri, 25 Dec 2015 00:00:00 GMT" }`
- `/api/` returns the current date in Unix and UTC format.
- `/api/invalid-date` returns `{ "error": "Invalid Date" }`

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) installed on your machine.

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/amittannagit/FCC-Timestamp-Microservice.git
   ```
2. **Navigate to the project directory**:
   ```bash
   cd FCC-Timestamp-Microservice
   ```
3. **Install the dependencies**:
   ```bash
   npm install
   ```
4. **Start the server**:
   ```bash
   npm start
   ```

### Running the API Locally

Once the server is running, you can access the API by navigating to `http://localhost:3000/api/` in your web browser or by using tools like `curl` or Postman.

## Deployment

You can deploy this project to platforms like [Heroku](https://www.heroku.com/), [Vercel](https://vercel.com/), or [Replit](https://replit.com/).

## License

This project is open source and available under the [MIT License](LICENSE).

## Acknowledgments

- Thanks to [freeCodeCamp](https://www.freecodecamp.org/) for providing the project guidelines.
```

### Instructions for Using the `README.md`

1. **Add the `README.md` to Your Project**:
   - Create a file named `README.md` in the root of your project directory.
   - Copy and paste the content above into the `README.md` file.

2. **Customize (Optional)**:
   - You can customize the `README.md` by adding additional details, such as your personal notes or additional instructions for deployment.

3. **Commit and Push to GitHub**:
   - After adding the `README.md`, commit the changes:
     ```bash
     git add README.md
     git commit -m "Add README.md"
     git push origin master
     ```
