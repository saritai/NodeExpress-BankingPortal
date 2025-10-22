# NodeExpress-BankingPortal

A banking portal web application built with Node.js and Express.js. This is a sample application created as part of a Pluralsight tutorial to demonstrate fundamental web development concepts including server-side routing, templating with EJS, form handling, and data management.

## Features

- **Account Management**: View account summaries for savings, checking, and credit accounts
- **Transaction History**: Display transaction details for each account
- **User Profile**: View and manage user profile information
- **Money Transfer**: Transfer funds between accounts (savings, checking, credit)
- **Payment Processing**: Make payments towards credit account balance
- **Responsive Design**: Clean, user-friendly interface

## Technologies Used

- **Node.js**: JavaScript runtime environment
- **Express.js**: Web application framework
- **EJS**: Embedded JavaScript templating engine
- **File System (fs)**: For data persistence using JSON files
- **Mocha & Chai**: Testing framework and assertion library

## Prerequisites

Before you begin, ensure you have the following installed:
- [Node.js](https://nodejs.org/) (version 8.x or higher)
- [npm](https://www.npmjs.com/) (comes with Node.js)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/saritai/NodeExpress-BankingPortal.git
   ```

2. Navigate to the project directory:
   ```bash
   cd NodeExpress-BankingPortal
   ```

3. Install dependencies:
   ```bash
   npm install
   ```

## Running the Application

Start the development server:

```bash
npm start
```

The application will be available at [http://localhost:3000](http://localhost:3000)

## Testing

Run all tests:
```bash
npm test
```

Run module-specific tests:
```bash
npm run test:module1  # Module 1: Use Express to Create a Server
npm run test:module2  # Module 2: File Handling and Routing
npm run test:module3  # Module 3: Handling Form Data
npm run test:module4  # Module 4: Creating a Data Access Library
npm run test:module5  # Module 5: Using the Express Router
```

## Project Structure

```
NodeExpress-BankingPortal/
├── src/
│   ├── app.js              # Main application file
│   ├── data.js             # Data access layer
│   ├── routes/
│   │   ├── accounts.js     # Account-related routes
│   │   └── services.js     # Service routes (transfer, payment)
│   ├── views/
│   │   ├── account.ejs     # Account detail view
│   │   ├── index.ejs       # Home page
│   │   ├── profile.ejs     # User profile view
│   │   ├── transfer.ejs    # Money transfer form
│   │   ├── payment.ejs     # Payment form
│   │   ├── header.ejs      # Header partial
│   │   ├── footer.ejs      # Footer partial
│   │   ├── summary.ejs     # Account summary partial
│   │   └── transactions.ejs # Transaction list partial
│   ├── json/
│   │   ├── accounts.json   # Account data
│   │   └── users.json      # User data
│   └── public/             # Static assets (CSS, JS, images)
├── test/                   # Test files organized by module
├── package.json            # Project dependencies and scripts
└── README.md              # This file
```

## Available Routes

### Pages
- `GET /` - Account summary (home page)
- `GET /profile` - User profile page
- `GET /account/savings` - Savings account details
- `GET /account/checking` - Checking account details
- `GET /account/credit` - Credit account details

### Services
- `GET /services/transfer` - Money transfer form
- `POST /services/transfer` - Process money transfer
- `GET /services/payment` - Payment form
- `POST /services/payment` - Process payment

## Data Storage

This application uses JSON files for data persistence:
- **accounts.json**: Stores account information (balance, transactions)
- **users.json**: Stores user profile information

**Note**: If `accounts.json` gets corrupted, you can restore it from `account_backup.json`.

## Development Notes

- The application uses `nodemon` for automatic server restarts during development
- EJS templates are used for server-side rendering
- Express middleware handles URL-encoded form data
- The application follows a modular structure with separated routes and data access layers

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Created as part of a Pluralsight tutorial
- Original copyright © 2018 Pluralsight

## Contributing

This is a tutorial project. Feel free to fork and modify for your own learning purposes!
