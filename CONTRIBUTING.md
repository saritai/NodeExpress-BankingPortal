# Contributing to NodeExpress-BankingPortal

Thank you for your interest in contributing to the NodeExpress-BankingPortal project! This document provides guidelines and instructions for contributing.

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [How to Contribute](#how-to-contribute)
- [Development Workflow](#development-workflow)
- [Coding Standards](#coding-standards)
- [Module Structure](#module-structure)
- [Testing Guidelines](#testing-guidelines)
- [Pull Request Process](#pull-request-process)
- [Reporting Issues](#reporting-issues)

## 📜 Code of Conduct

This project is intended for educational purposes. We expect all contributors to:

- Be respectful and constructive in all interactions
- Welcome newcomers and help them learn
- Focus on what is best for the learning community
- Show empathy towards other community members

## 🚀 Getting Started

1. **Fork the repository** on GitHub
2. **Clone your fork** locally:
   ```bash
   git clone https://github.com/YOUR-USERNAME/NodeExpress-BankingPortal.git
   cd NodeExpress-BankingPortal
   ```
3. **Install dependencies**:
   ```bash
   npm install
   ```
4. **Create a new branch** for your contribution:
   ```bash
   git checkout -b feature/your-feature-name
   ```

## 🤝 How to Contribute

There are several ways you can contribute:

### 1. Improve Documentation

- Fix typos or clarify existing documentation
- Add examples or additional explanations
- Translate documentation (if applicable)
- Improve code comments

### 2. Fix Bugs

- Look for issues labeled `bug`
- Reproduce the issue
- Create a fix with appropriate tests
- Submit a pull request

### 3. Add Features

- Discuss major changes in an issue first
- Ensure the feature aligns with the project's educational goals
- Add tests for new functionality
- Update documentation accordingly

### 4. Improve Tests

- Add missing test cases
- Improve test coverage
- Fix flaky tests
- Enhance test documentation

## 🔄 Development Workflow

### Setting Up Your Development Environment

1. **Start the development server**:
   ```bash
   npm start
   ```
   This uses `nodemon` to automatically restart the server when files change.

2. **Run tests in watch mode** (if needed):
   ```bash
   npm test
   ```

3. **Test specific modules** as you work on them:
   ```bash
   npm run test:module1  # Replace with the module you're working on
   ```

### Making Changes

1. **Make your changes** in the appropriate files
2. **Test your changes** frequently:
   - Run the application and verify manually
   - Run the test suite
   - Check for any console errors

3. **Follow the coding standards** (see below)

4. **Commit your changes** with clear, descriptive messages:
   ```bash
   git add .
   git commit -m "Add feature: brief description of changes"
   ```

## 🎨 Coding Standards

### JavaScript Style

- Use **ES6+ syntax** where appropriate (arrow functions, const/let, destructuring)
- Use **2 spaces** for indentation
- Use **semicolons** at the end of statements
- Use **single quotes** for strings (unless using template literals)
- Keep lines under **80-100 characters** when possible

### Example:

```javascript
// Good
const express = require('express');
const router = express.Router();

router.get('/savings', (req, res) => {
  res.render('account', { account: accounts.savings });
});

// Avoid
var express = require("express")
var router = express.Router()

router.get("/savings", function(req, res) {
  res.render("account", {account: accounts.savings})
})
```

### Naming Conventions

- **Variables and functions**: camelCase (`accountData`, `writeJSON`)
- **Constants**: camelCase for regular constants, UPPER_CASE for true constants
- **Files**: lowercase with hyphens or camelCase matching content (`accounts.js`, `services.js`)
- **Routes**: lowercase with hyphens (`/account/savings`, `/services/transfer`)

### Comments

- Add comments for complex logic or non-obvious code
- Use JSDoc-style comments for functions when appropriate
- Keep comments concise and meaningful

```javascript
/**
 * Writes the accounts object to JSON file
 */
const writeJSON = () => {
  const stringData = JSON.stringify(accounts);
  fs.writeFileSync(path.join(__dirname, 'json/accounts.json'), stringData, 'utf8');
};
```

## 📚 Module Structure

This project is organized into five learning modules. Each module builds upon the previous one:

### Module 1: Express Server Setup
- Setting up Express
- Configuring views and static files
- Creating basic routes

### Module 2: File Handling and Routing
- Reading JSON files
- Parsing data
- Creating multiple routes

### Module 3: Form Data Handling
- Processing POST requests
- Handling form submissions
- Data validation

### Module 4: Data Access Layer
- Separating concerns
- Creating reusable functions
- Modular code organization

### Module 5: Express Router
- Using Router for better organization
- Splitting routes into separate files
- RESTful routing patterns

When contributing, ensure your changes align with the appropriate module's learning objectives.

## 🧪 Testing Guidelines

### Running Tests

- **All tests**: `npm test`
- **Specific module**: `npm run test:module1` (replace number as needed)

### Writing Tests

If you add new functionality, please include tests:

1. Place tests in the appropriate module folder under `/test/`
2. Follow existing test patterns
3. Use descriptive test names
4. Test both success and failure cases
5. Ensure tests are independent and can run in any order

### Test Structure Example

```javascript
const { expect } = require('chai');

describe('Feature Name', () => {
  it('should do something specific', () => {
    // Arrange
    const input = 'test';
    
    // Act
    const result = someFunction(input);
    
    // Assert
    expect(result).to.equal('expected output');
  });
});
```

## 📥 Pull Request Process

1. **Ensure your code passes all tests**:
   ```bash
   npm test
   ```

2. **Update documentation** if needed:
   - Update README.md for new features
   - Add or update code comments
   - Update relevant module documentation in tasks.md

3. **Create a Pull Request**:
   - Use a clear, descriptive title
   - Reference any related issues
   - Describe what changes you made and why
   - Include screenshots for UI changes (if applicable)

4. **PR Template**:
   ```markdown
   ## Description
   Brief description of changes
   
   ## Type of Change
   - [ ] Bug fix
   - [ ] New feature
   - [ ] Documentation update
   - [ ] Test improvement
   
   ## Testing
   - [ ] All tests pass
   - [ ] Added new tests for new functionality
   - [ ] Manually tested the application
   
   ## Related Issues
   Closes #issue_number
   ```

5. **Review Process**:
   - Address any feedback from reviewers
   - Make requested changes
   - Keep the PR updated with the main branch if needed

6. **After Approval**:
   - Your PR will be merged by a maintainer
   - Delete your feature branch after merging

## 🐛 Reporting Issues

### Before Creating an Issue

- Check if the issue already exists
- Verify it's actually a problem (not expected behavior)
- Ensure you're using the latest version

### Creating a Good Issue

Include the following information:

1. **Clear title** describing the issue
2. **Description** of the problem
3. **Steps to reproduce**
4. **Expected behavior**
5. **Actual behavior**
6. **Environment details**:
   - Node.js version
   - npm version
   - Operating system

### Issue Template

```markdown
## Description
Clear description of the issue

## Steps to Reproduce
1. Go to '...'
2. Click on '...'
3. See error

## Expected Behavior
What should happen

## Actual Behavior
What actually happens

## Environment
- Node.js version: 
- npm version:
- OS:

## Additional Context
Any other relevant information
```

## 📞 Questions?

If you have questions about contributing:

- Check the [README.md](README.md) for general project information
- Review [tasks.md](tasks.md) for module-specific details
- Open an issue with the `question` label

## 🙏 Thank You!

Your contributions help make this project better for everyone learning Express.js. Thank you for taking the time to contribute!
