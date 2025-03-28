# Contact Form Email Sender API

This is a simple Express.js backend service that allows users to send emails via a contact form. It uses **Node.js, Express, Nodemailer, and CORS** to send emails securely using a Gmail SMTP server.

## Features
- Accepts contact form submissions (First Name, Last Name, Email, and Message)
- Sends emails using **Nodemailer** via Gmail SMTP
- Supports **CORS** for cross-origin requests
- Implements basic input validation

## Tech Stack
- **Node.js**
- **Express.js**
- **Nodemailer**
- **Body-parser**
- **CORS**
- **dotenv** (for environment variables)

## Prerequisites
Make sure you have the following installed:
- [Node.js](https://nodejs.org/)
- [NPM](https://www.npmjs.com/) (comes with Node.js)

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/contact-form-email-api.git
   cd contact-form-email-api
   ```
2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the root directory and add the following:
   ```env
   EMAIL_USER=your-email@gmail.com
   EMAIL_PASS=your-app-password
   PORT=5000
   ```
   **Note:** Use an **App Password** instead of your regular Gmail password. [Set up an App Password here](https://myaccount.google.com/security).

## Running the Server
Start the development server with:
```bash
npm start
```
The server will run at: [http://localhost:5000](http://localhost:5000)

## API Endpoint
### **POST /send-email**
- **Description:** Sends an email using the form data
- **Headers:** `Content-Type: application/json`
- **Request Body:**
  ```json
  {
    "firstName": "John",
    "lastName": "Doe",
    "email": "johndoe@example.com",
    "message": "Hello, this is a test message."
  }
  ```
- **Response:**
  - **Success (200):** `{ "success": true, "message": "Email sent successfully!" }`
  - **Error (400/500):** `{ "success": false, "message": "Error message here" }`

## Deployment
You can deploy this API on platforms like:
- **Heroku**
- **Vercel**
- **Render**
- **AWS / DigitalOcean**

## License
This project is **MIT Licensed**.

