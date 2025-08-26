# auth_dashboard

This project is a web application that allows authors to upload book manuscripts, design covers using a simple editor, and generate book descriptions and keywords with an AI assistant. The dashboard provides a real-time view of the book's status and allows authors to download metadata for their published work.

# Install server dependencies
cd server
npm install

# Install client dependencies
cd ../client
npm install

Frontend (React): The user interface is developed with React, using react-router-dom for navigation. The useEffect hook with a polling mechanism ensures the dashboard updates in real-time to show changes in a book's status. The cover designer uses the html-to-image library to convert the user's design into a static image file.

Backend (Node.js/Express): The backend serves as the API for the application. It uses MongoDB for data persistence and Mongoose for object modeling. The multer middleware handles file uploads for manuscripts and cover images.

AI Integration: The OpenAI API is integrated into the backend to generate a book description and keywords based on the book's title and genre. The API response is parsed and sent to the frontend for the user to review and edit.

Data Flow: The user uploads a book, which creates a new entry in the database. When the user designs a cover, the frontend captures the design as a PNG and sends it to a dedicated endpoint, which updates the book's entry. This modular approach ensures each part of the application is independent and scalable.
