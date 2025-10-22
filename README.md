# NodeExpress-BankingPortal

A sample banking portal application built with Node.js and Express.js as part of a Pluralsight learning project. This application demonstrates core Express.js concepts including routing, middleware, templating with EJS, and form handling.

## 📋 Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Available Routes](#available-routes)
- [Testing](#testing)
- [Technologies Used](#technologies-used)
- [Learning Modules](#learning-modules)
- [Contributing](#contributing)
- [License](#license)

## ✨ Features

- **Account Management**: View savings, checking, and credit account details
- **Money Transfers**: Transfer funds between different accounts
- **Credit Card Payments**: Make payments towards credit card balance
- **User Profile**: View and manage user profile information
- **Transaction History**: Track all account transactions
- **Responsive Design**: Clean and simple user interface

## 🔧 Prerequisites

Before you begin, ensure you have met the following requirements:

- **Node.js**: Version 12.x or higher
- **npm**: Version 6.x or higher (usually comes with Node.js)

To check your installed versions, run:

```bash
node --version
npm --version
```

## 📦 Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/saritai/NodeExpress-BankingPortal.git
   cd NodeExpress-BankingPortal
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Verify installation**

   Run the test suite to ensure everything is set up correctly:

   ```bash
   npm test
   ```

## 🚀 Usage

### Starting the Application

To start the development server with auto-reload:

```bash
npm start
```

The application will be available at [http://localhost:3000](http://localhost:3000)

### Accessing the Application

Once the server is running, you can:

- Visit the homepage at `http://localhost:3000`
- View account summaries for savings, checking, and credit accounts
- Transfer money between accounts
- Make credit card payments
- View user profile information

## 📁 Project Structure

```
NodeExpress-BankingPortal/
├── src/
│   ├── app.js                 # Main application file
│   ├── data.js                # Data access layer
│   ├── json/                  # JSON data files
│   │   ├── accounts.json      # Account information
│   │   └── users.json         # User information
│   ├── routes/                # Route handlers
│   │   ├── accounts.js        # Account-related routes
│   │   └── services.js        # Service routes (transfer, payment)
│   ├── views/                 # EJS templates
│   │   ├── account.ejs        # Account detail view
│   │   ├── index.ejs          # Homepage
│   │   ├── profile.ejs        # User profile view
│   │   ├── transfer.ejs       # Money transfer form
│   │   ├── payment.ejs        # Payment form
│   │   └── ...                # Other view templates
│   └── public/                # Static assets (CSS, JS, images)
├── test/                      # Test files organized by module
├── package.json               # Project dependencies and scripts
└── README.md                  # This file
```

## 🔗 Available Routes

### Account Routes (`/account`)

- `GET /account/savings` - View savings account details
- `GET /account/checking` - View checking account details
- `GET /account/credit` - View credit account details

### Service Routes (`/services`)

- `GET /services/transfer` - Display money transfer form
- `POST /services/transfer` - Process money transfer
- `GET /services/payment` - Display payment form
- `POST /services/payment` - Process credit card payment

### Other Routes

- `GET /` - Homepage with account summary
- `GET /profile` - User profile page

## 🧪 Testing

This project includes a comprehensive test suite organized by learning modules.

### Run All Tests

```bash
npm test
```

### Run Module-Specific Tests

```bash
npm run test:module1  # Express server setup
npm run test:module2  # File handling and routing
npm run test:module3  # Form data handling
npm run test:module4  # Data access library
npm run test:module5  # Express Router
```

## 🛠 Technologies Used

- **[Node.js](https://nodejs.org/)** - JavaScript runtime
- **[Express.js](https://expressjs.com/)** - Web application framework
- **[EJS](https://ejs.co/)** - Embedded JavaScript templating
- **[Mocha](https://mochajs.org/)** - Testing framework
- **[Chai](https://www.chaijs.com/)** - Assertion library
- **[Nodemon](https://nodemon.io/)** - Development auto-reload

## 📚 Learning Modules

This project is structured into five progressive learning modules:

1. **Module 1**: Using Express to create a server
2. **Module 2**: File handling and routing
3. **Module 3**: Handling form data with POST requests
4. **Module 4**: Creating a data access library
5. **Module 5**: Using the Express Router for better organization

Each module builds upon the previous one, teaching fundamental Express.js concepts step by step. See [tasks.md](tasks.md) for detailed module objectives and tasks.

## 🤝 Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for details on how to contribute to this project.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- This project is part of a Pluralsight learning course
- Original template and structure by Pluralsight
- Built for educational purposes to demonstrate Express.js fundamentals
