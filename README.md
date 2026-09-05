# SpendlyAPI

A comprehensive API project for expense tracking and spending management. SpendlyAPI provides robust endpoints to help users manage their finances efficiently.

## 📋 Table of Contents

- [Features](#features)
- [Getting Started](#getting-started)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)
- [Support](#support)

## ✨ Features

- User authentication and account management
- Expense tracking and categorization
- Budget management and monitoring
- Detailed spending analytics and reports
- Transaction history and records
- Multi-user support
- RESTful API architecture

## 🚀 Getting Started

These instructions will help you get SpendlyAPI up and running on your local machine for development and testing purposes.

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn package manager
- Git
- A code editor (VS Code recommended)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/DharmVGEC/SpendlyAPI.git
   cd SpendlyAPI
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Configure environment variables**
   ```bash
   cp .env.example .env
   # Edit .env with your configuration
   ```

4. **Start the server**
   ```bash
   npm start
   ```

The API should now be running on `http://localhost:3000`

## 💻 Usage

### Basic API Request

```bash
curl -X GET http://localhost:3000/api/expenses \
  -H "Authorization: Bearer YOUR_TOKEN"
```

### Example Request with Authentication

```javascript
const response = await fetch('http://localhost:3000/api/expenses', {
  method: 'GET',
  headers: {
    'Authorization': 'Bearer YOUR_TOKEN',
    'Content-Type': 'application/json'
  }
});
const data = await response.json();
console.log(data);
```

## 📚 API Endpoints

### Authentication
- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout

### Expenses
- `GET /api/expenses` - Get all expenses
- `POST /api/expenses` - Create a new expense
- `GET /api/expenses/:id` - Get expense by ID
- `PUT /api/expenses/:id` - Update an expense
- `DELETE /api/expenses/:id` - Delete an expense

### Budget
- `GET /api/budget` - Get budget information
- `POST /api/budget` - Create a budget
- `PUT /api/budget/:id` - Update a budget
- `DELETE /api/budget/:id` - Delete a budget

### Reports
- `GET /api/reports/summary` - Get spending summary
- `GET /api/reports/by-category` - Get expenses by category
- `GET /api/reports/monthly` - Get monthly report

## ⚙️ Configuration

Create a `.env` file in the root directory with the following variables:

```env
# Server Configuration
PORT=3000
NODE_ENV=development

# Database Configuration
DB_HOST=localhost
DB_PORT=5432
DB_NAME=spendly_db
DB_USER=your_db_user
DB_PASSWORD=your_db_password

# JWT Configuration
JWT_SECRET=your_jwt_secret_key
JWT_EXPIRY=7d

# API Configuration
API_VERSION=v1
LOG_LEVEL=debug
```

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Coding Standards
- Follow the existing code style
- Write meaningful commit messages
- Add tests for new features
- Update documentation as needed

## 📝 License

This project is currently unlicensed. Please contact the project maintainer for licensing information.

## 🆘 Support

For support, please:
- Check existing issues on GitHub
- Create a new issue with a detailed description
- Contact the maintainers directly

---

**Repository:** [DharmVGEC/SpendlyAPI](https://github.com/DharmVGEC/SpendlyAPI)
**Octopus Deploy Project** : SpendlyAPIFargate
**Author:** DharmVGEC

**Last Updated:** September 2026
