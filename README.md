# Plant Store

A plant store application built using **React** that allows users to browse, add, update, and delete plants. This application interacts with a backend API to persist data across sessions.

## Table of Contents

- [Description](#description)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [File Structure](#file-structure)
- [Contributing](#contributing)
- [License](#license)

---

## Description

The Plant Store application allows users to:

- View a list of plants available in the store.
- Add new plants with a name, price, and image.
- Edit the price of existing plants.
- Toggle the stock status (in-stock or out-of-stock).
- Delete plants from the inventory.

The app is built using **React** and fetches data from a RESTful backend API hosted locally. All changes made by users (adding, updating, and deleting plants) are persisted in the backend.

---

## Features

- **Browse Plants**: Display a list of plants with their names, prices, images, and stock status.
- **Add Plants**: Users can add new plants to the store by providing a name, image URL, and price.
- **Edit Plant Prices**: Users can update the price of a plant directly from the UI.
- **Toggle Stock Status**: Users can toggle the availability of plants by switching between "In Stock" and "Out of Stock."
- **Delete Plants**: Users can delete a plant from the inventory.
- **Persistent Data**: All changes (add, update, delete) are reflected in the backend and persist across sessions.
- **Search Functionality**: Users can search plants by name.

---

## Tech Stack

- **Frontend**: React, JSX, CSS
- **Backend**: Node.js (Express) with a JSON database (or mock API server)
- **State Management**: React's `useState` and `useEffect`
- **HTTP Requests**: Fetch API
- **UI Components**: Custom components built using functional components in React

---

## Installation

### Prerequisites

- **Node.js** and **npm** installed on your system. You can check if they are installed by running the following commands:
  ```bash
  node -v
  npm -v
Steps to Run the Project
Clone the repository:

bash
git clone https://github.com/yourusername/plant-store.git
Navigate to the project directory:

bash
cd plant-store
Install the dependencies:

bash
npm install
Start the project:

bash
npm start
This will start the development server and the app should be available at http://localhost:3000 in your browser.

Usage
Once the app is running, you can:

View available plants: The plant list will automatically load and display all plants.
Add a new plant: Use the "Add Plant" form to provide a name, image URL, and price. After submitting, the plant will be added to the list.
Update a plant's price: Click "Edit Price" to change the price of a plant. The change will be reflected both in the UI and in the backend.
Delete a plant: Use the "Delete" button next to any plant to remove it from the inventory.
Toggle stock status: Click on "In Stock" or "Out of Stock" to toggle the plant's availability status.
API Endpoints
The following API endpoints are used by the frontend:

GET /plants
Description: Fetches all plants in the store.
Response: A JSON array of plants.
POST /plants
Description: Adds a new plant to the store.
Request Body:
{
  "name": "Plant Name",
  "image": "Image URL",
  "price": "Plant Price"
}
PUT /plants/:id
Description: Updates the price of a specific plant.
Request Body
yaml
Copy code

---:
{
  "price": "New Price"
}
DELETE /plants/:id
Description: Deletes a plant from the store.
Response: No response body; returns HTTP status 200 on success.
File Structure
The project follows a modular file structure to keep things organized:

bash
/plant-store
│
├── /public             # Public assets, including index.html and images
│   └── index.html      # Main HTML file
│
├── /src
│   ├── /components     # React components (PlantCard, PlantList, NewPlantForm, Search, etc.)
│   ├── /hooks          # Custom hooks (optional)
│   ├── /styles         # CSS files for styling
│   ├── App.js          # Main app component
│   ├── index.js        # Entry point for React
│   └── serviceWorker.js # Optional: for offline caching
│
├── package.json        # Project metadata and dependencies
└── README.md           # This file
Contributing
We welcome contributions! If you'd like to help improve this project, please follow these steps:

Fork the repository.
Create a new branch (git checkout -b feature-branch).
Make your changes and commit them (git commit -am 'Add feature').
Push to the branch (git push origin feature-branch).
Create a pull request explaining your changes.
License
This project is licensed under the MIT License.

Additional Notes
Error Boundaries: The application uses React's error boundaries to handle potential errors gracefully during rendering.
State Management: We use React’s built-in useState and useEffect hooks to manage the state and side effects of the app.
Search Feature: The search functionality filters the list of plants based on the user's input and displays matching results.