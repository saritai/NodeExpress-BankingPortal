# NodeExpress-BankingPortal

A simple banking portal web application built with Node.js and Express as a Pluralsight learning project. This application demonstrates core Express.js concepts including routing, templating with EJS, form handling, and file-based data persistence.

## 📋 Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Available Scripts](#available-scripts)
- [Project Structure](#project-structure)
- [Learning Modules](#learning-modules)
- [Technologies Used](#technologies-used)
- [Testing](#testing)
- [License](#license)

## ✨ Features

- **Account Management**: View savings, checking, and credit account details
- **Transaction History**: Display account transactions
- **Fund Transfers**: Transfer money between accounts
- **Bill Payments**: Make payments on credit account
- **User Profile**: View and manage user information
- **Responsive UI**: Clean interface with EJS templating

## 🔧 Prerequisites

Before you begin, ensure you have the following installed:

- [Node.js](https://nodejs.org/) (version 8.x or higher recommended)
- [npm](https://www.npmjs.com/) (comes with Node.js)

## 📦 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/saritai/NodeExpress-BankingPortal.git
   cd NodeExpress-BankingPortal
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

## 🚀 Usage

1. Start the development server:
   ```bash
   npm start
   ```

2. Open your browser and navigate to:
   ```
   http://localhost:3000
   ```

3. The application will automatically reload when you make changes (using nodemon).

### First Time Setup Verification

To verify everything is set up correctly, run the test suite:

```bash
npm test
```

This will show you the current status of all tests. As you work through the learning modules, you'll fix failing tests.

## 📜 Available Scripts

- `npm start` - Start the development server with auto-reload
- `npm test` - Run all tests
- `npm run test:module1` - Run tests for Module 1
- `npm run test:module2` - Run tests for Module 2
- `npm run test:module3` - Run tests for Module 3
- `npm run test:module4` - Run tests for Module 4
- `npm run test:module5` - Run tests for Module 5

## 📁 Project Structure

```
NodeExpress-BankingPortal/
├── src/
│   ├── app.js                 # Main application entry point
│   ├── data.js                # Data access library
│   ├── routes/                # Route handlers
│   │   ├── accounts.js        # Account-related routes
│   │   └── services.js        # Service routes (transfer, payment)
│   ├── views/                 # EJS templates
│   │   ├── index.ejs          # Home page
│   │   ├── account.ejs        # Account details page
│   │   ├── profile.ejs        # User profile page
│   │   ├── transfer.ejs       # Fund transfer page
│   │   ├── payment.ejs        # Payment page
│   │   └── ...                # Other view components
│   ├── public/                # Static assets (CSS, JS, images)
│   └── json/                  # JSON data files
│       ├── accounts.json      # Account data
│       └── users.json         # User data
├── test/                      # Test files organized by module
├── package.json               # Project dependencies and scripts
└── README.md                  # This file
```

## 📚 Learning Modules

This project is structured as a series of learning modules, each building on the previous one:

### Module 1: Use Express to Create a Server
- Setting up Express application
- Configuring view engine (EJS)
- Serving static files
- Creating basic routes

### Module 2: File Handling and Routing
- Reading JSON data files
- Creating dynamic routes for accounts
- Rendering views with data
- Working with EJS templates

### Module 3: Handling Form Data
- Processing POST requests
- Implementing transfer functionality
- Implementing payment functionality
- Writing data back to JSON files

### Module 4: Creating a Data Access Library
- Extracting data logic into a separate module
- Creating reusable functions
- Using module.exports
- Refactoring for better code organization

### Module 5: Using the Express Router
- Creating route modules
- Organizing routes by functionality
- Using Express Router
- Updating application structure

For detailed instructions on each module, see [tasks.md](tasks.md).

## 🛠 Technologies Used

- **[Node.js](https://nodejs.org/)** - JavaScript runtime
- **[Express](https://expressjs.com/)** - Web application framework
- **[EJS](https://ejs.co/)** - Templating engine
- **[Nodemon](https://nodemon.io/)** - Development auto-reload tool

### Development & Testing

- **[Mocha](https://mochajs.org/)** - Test framework
- **[Chai](https://www.chaijs.com/)** - Assertion library
- **[Sinon](https://sinonjs.org/)** - Test spies, stubs, and mocks
- **[Supertest](https://github.com/visionmedia/supertest)** - HTTP assertion library
- **[Cheerio](https://cheerio.js.org/)** - HTML parsing and manipulation

## 🧪 Testing

The project includes comprehensive tests for each learning module. Tests verify:

- Proper route configuration
- Correct view rendering
- Data handling functionality
- Form processing
- Module organization

Run tests for specific modules as you complete them:

```bash
npm run test:module1  # After completing Module 1
npm run test:module2  # After completing Module 2
# ... and so on
```

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Copyright (c) 2018 Pluralsight

## 🙏 Acknowledgments

- This project is part of a Pluralsight course on Node.js and Express
- Designed for learning fundamental Express.js concepts
- Sample banking data and structure provided for educational purposes

## 📝 Notes

- This is a **learning project** and not intended for production use
- Account data is stored in JSON files (not a real database)
- No authentication or security features are implemented
- For educational purposes only

---

**Happy Learning! 🚀**
