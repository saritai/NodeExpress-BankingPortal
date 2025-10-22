# NodeExpress-BankingPortal

A sample banking portal application built with Node.js and Express. This project serves as a hands-on learning resource for understanding web application development with Express, featuring account management, fund transfers, and payment processing.

## Features

- **Account Management**: View account summaries for savings, checking, and credit accounts
- **Fund Transfers**: Transfer money between different accounts
- **Payment Processing**: Make payments on credit accounts
- **User Profiles**: View and manage user profile information
- **Transaction History**: Track all account transactions
- **Responsive Design**: Clean, user-friendly interface using EJS templates

## Prerequisites

Before you begin, ensure you have the following installed:
- [Node.js](https://nodejs.org/) (version 8.x or higher recommended)
- npm (comes with Node.js)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/saritai/NodeExpress-BankingPortal.git
   cd NodeExpress-BankingPortal
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

## Running the Application

Start the development server:

```bash
npm start
```

The application will be running at `http://localhost:3000`

## Testing

Run all tests:
```bash
npm test
```

Run module-specific tests:
```bash
npm run test:module1
npm run test:module2
npm run test:module3
npm run test:module4
npm run test:module5
```

## Project Structure

```
NodeExpress-BankingPortal/
├── src/
│   ├── app.js              # Main application file
│   ├── data.js             # Data access layer
│   ├── routes/             # Express route definitions
│   │   ├── accounts.js     # Account-related routes
│   │   └── services.js     # Service routes (transfer, payment)
│   ├── views/              # EJS templates
│   ├── public/             # Static assets (CSS, JS, images)
│   └── json/               # JSON data files
├── test/                   # Test files organized by module
├── package.json
└── README.md
```

## Learning Modules

This project is organized into progressive learning modules:

1. **Module 1**: Use Express to Create a Server
2. **Module 2**: File Handling and Routing
3. **Module 3**: Handling Form Data
4. **Module 4**: Creating a Data Access Library
5. **Module 5**: Using the Express Router

For detailed module instructions, see [tasks.md](tasks.md).

## Technology Stack

- **Backend**: Node.js, Express.js
- **Templating**: EJS (Embedded JavaScript)
- **Testing**: Mocha, Chai, Supertest, Sinon
- **Development**: Nodemon for auto-reloading

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Copyright (c) 2018 Pluralsight

## Acknowledgments

This is a Pluralsight project sample application designed for educational purposes.
