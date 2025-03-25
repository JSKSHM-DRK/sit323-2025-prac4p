**Calculator Microservice**

Overview

This project is a simple calculator microservice built using Node.js and Express. The service provides basic arithmetic operations through RESTful API endpoints.

Features

Supports addition, subtraction, multiplication, and division

Handles errors gracefully (e.g., invalid inputs, division by zero)

Provides meaningful error messages

Lightweight and easy to deploy

Prerequisites

Ensure you have the following installed before running the project:

Node.js: Download here

Git: Download here

Setup and Installation

Follow these steps to set up and run the microservice:

1. Clone the Repository

git clone https://github.com/username/sit323-2025-prac4p.git
cd sit323-2025-prac4p

2. Install Dependencies

npm install

3. Run the Microservice

node server.js

The service will be available at: http://localhost:3000

API Endpoints

All operations are performed via GET requests with query parameters num1 and num2.

Endpoint

Description

Example Usage

/add

Adds num1 and num2

/add?num1=5&num2=3

/subtract

Subtracts num2 from num1

/subtract?num1=10&num2=4

/multiply

Multiplies num1 and num2

/multiply?num1=6&num2=7

/divide

Divides num1 by num2

/divide?num1=20&num2=5

Error Handling

Invalid Input: If num1 or num2 are missing or non-numeric, the service returns:

{ "error": "Invalid input. Please provide two numbers." }

Division by Zero: If num2 is 0 in a division request, the service returns:

{ "error": "Division by zero is not allowed." }

Unsupported Routes: If an unknown endpoint is accessed, the service returns:

{ "error": "Endpoint not found" }

Deployment

You can deploy this microservice using a cloud platform such as Heroku, AWS, or Docker.

Example Docker Deployment

Create a Dockerfile:

FROM node:18
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
CMD ["node", "server.js"]
EXPOSE 3000

Build and run the container:

docker build -t calculator-microservice .
docker run -p 3000:3000 calculator-microservice

Contributing

Fork the repository

Create a new branch (git checkout -b feature-branch)

Commit your changes (git commit -m "Added a new feature")

Push to the branch (git push origin feature-branch)

Open a Pull Request

License

This project is licensed under the MIT License.

Author: Your Name

GitHub: Your GitHub Profile

