# NodeExpress-BankingPortal

A sample banking portal web application built with Node.js and Express as part of a Pluralsight course project. This application demonstrates fundamental web development concepts including server-side routing, templating with EJS, and basic CRUD operations.

## Features

- **Account Management**: View details for savings, checking, and credit accounts
- **Account Summary**: Dashboard displaying all account balances and information
- **Fund Transfers**: Transfer money between different accounts
- **Bill Payment**: Make payments on credit card accounts
- **User Profile**: View and manage user profile information
- **Transaction History**: Track account transactions

## Technologies Used

- **Node.js**: JavaScript runtime environment
- **Express**: Web application framework
- **EJS**: Embedded JavaScript templating engine
- **CSS**: Styling and layout

## Prerequisites

- Node.js (v8 or higher)
- npm (Node Package Manager)

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

## Usage

### Running the Application

Start the development server:
```bash
npm start
```

The application will be available at `http://localhost:3000`

### Available Routes

- `/` - Account summary dashboard
- `/profile` - User profile page
- `/account/savings` - Savings account details
- `/account/checking` - Checking account details
- `/account/credit` - Credit card account details
- `/services/transfer` - Transfer funds between accounts
- `/services/payment` - Make credit card payments

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
│   ├── app.js              # Main application entry point
│   ├── data.js             # Data management and JSON file operations
│   ├── routes/             # Route handlers
│   │   ├── accounts.js     # Account-related routes
│   │   └── services.js     # Service routes (transfer, payment)
│   ├── views/              # EJS templates
│   │   ├── index.ejs       # Account summary page
│   │   ├── profile.ejs     # User profile page
│   │   ├── account.ejs     # Individual account details
│   │   ├── transfer.ejs    # Fund transfer page
│   │   ├── payment.ejs     # Payment page
│   │   └── ...             # Other view templates
│   ├── public/             # Static assets (CSS, client-side JS)
│   └── json/               # JSON data files
├── test/                   # Test files
├── package.json            # Project dependencies and scripts
└── README.md              # This file
```

## Learning Objectives

This project is designed to teach:

- Setting up an Express server
- Configuring view engines and static file serving
- Creating routes and route handlers
- Working with EJS templates
- Handling form submissions (POST requests)
- Managing application data with JSON files
- Implementing basic banking operations (transfers, payments)
- Writing and running tests with Mocha and Chai

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Created as part of a Pluralsight course on Node.js and Express
- Copyright (c) 2018 Pluralsight

## Contributing

This is a learning project. Feel free to fork and experiment with the code to enhance your understanding of Node.js and Express.
