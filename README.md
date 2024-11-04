

# AI Image Generator

This is a full-stack application built with the MERN (MongoDB, Express.js, React.js, Node.js) stack that allows users to generate AI-powered images. The app provides an interface for users to input prompts and create images using artificial intelligence, leveraging a backend API to handle requests and a front end to provide a smooth user experience.

## Features

- **AI Image Generation**: Generate images based on user input using an AI model.
- **User Authentication**: Sign up, log in, and secure access to image generation features.
- **Image History**: View previously generated images and search through past creations.
- **Image Filtering**: Add filters to generated images to adjust colors, style, and other visual effects.
- **Share & Save**: Save images to user profiles or download them locally.
- **Responsive Design**: Optimized for both desktop and mobile viewing.

## Tech Stack

### Frontend
- **React.js**: JavaScript library for building user interfaces.
- **Redux**: State management for consistent and predictable state changes.
- **React Router**: Handles routing within the single-page application.

### Backend
- **Node.js**: JavaScript runtime environment to run backend services.
- **Express.js**: Web framework for building RESTful APIs.
- **MongoDB**: Database for storing user data and image generation history.
- **Mongoose**: MongoDB ORM to interact with the database easily.

### AI Model Integration
- **AI API**: Uses a third-party AI image generation API (such as OpenAI’s DALL-E, or another image generation API) to handle image creation based on prompts.

## Getting Started

### Prerequisites

- **Node.js** and **npm** installed
- **MongoDB** installed or access to MongoDB Atlas
- API key for the AI image generation service

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/username/ai-image-generator.git
   cd ai-image-generator
   ```

2. **Install dependencies for both frontend and backend:**

   ```bash
   # Install server dependencies
   cd backend
   npm install

   # Install client dependencies
   cd ../frontend
   npm install
   ```

3. **Set up environment variables:**

   Create a `.env` file in the `backend` folder and add your configuration details:

   ```env
   MONGO_URI=your_mongodb_connection_string
   AI_API_KEY=your_ai_api_key
   JWT_SECRET=your_jwt_secret
   PORT=5000
   ```

4. **Run the application:**

   In separate terminal windows, start both frontend and backend servers:

   ```bash
   # Run the backend server
   cd backend
   npm start

   # Run the frontend server
   cd ../frontend
   npm start
   ```

5. **Access the application:** Open your browser and go to `http://localhost:3000`.

## Folder Structure

```plaintext
ai-image-generator/
├── backend/
│   ├── config/         # Environment and database configurations
│   ├── controllers/    # Business logic for different app functions
│   ├── models/         # Mongoose models
│   ├── routes/         # API endpoints
│   └── server.js       # Main server file
└── frontend/
    ├── public/         # Public assets and index.html
    ├── src/
    │   ├── components/ # React components
    │   ├── pages/      # Application pages
    │   ├── redux/      # Redux actions and reducers
    │   └── App.js      # Main React app file
```

## API Endpoints

- **POST** `/api/generate-image`: Generate an image based on user prompt
- **POST** `/api/auth/register`: Register a new user
- **POST** `/api/auth/login`: Login user
- **GET** `/api/images`: Retrieve all generated images for the logged-in user

## Contributing

Contributions are welcome! If you'd like to improve the application or add new features, please feel free to fork the repository and submit a pull request.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for more information.

---

Happy coding!