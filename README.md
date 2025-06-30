# 🎬 MovieFlix - A React Movie Application

Welcome to MovieFlix! A sleek and responsive web application built with React for discovering and exploring movies. Users can search for movies, view details such as ratings and summaries, and browse through curated lists of popular and top-rated films.

---

## ✨ Features

*   **Dynamic Search:** Instantly search for any movie by its title.
*   **Trending Movies:** See what's currently popular.
*   **Detailed Views:** Click on any movie to see a detailed page with its poster, synopsis, user rating, and release date.
*   **Responsive Design:** A mobile-first approach ensures a seamless experience on any device, from desktops to smartphones.
*   **Modern UI:** A clean and intuitive user interface for the best user experience.

---

## 🛠️ Technology Stack

This project was built using modern web technologies:

*   **[React](https://reactjs.org/):** A JavaScript library for building user interfaces.
*   **[Vite](https://vitejs.dev/):** A fast build tool for modern web projects.
*   **[Tailwind CSS](https://tailwindcss.com/):** A utility-first CSS framework for rapid UI development.
*   **[Appwrite](https://appwrite.io/):** An open-source backend platform for building web and mobile applications. Used here for tracking trending movies.
*   **[The Movie Database (TMDB) API](https://www.themoviedb.org/documentation/api):** For fetching movie data.
*   **[ESLint](https://eslint.org/):** To enforce code quality and style consistency.

---

## 🚀 Getting Started

Follow these instructions to get a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

Make sure you have the following installed on your system:
*   [Node.js](https://nodejs.org/en/) (v14 or newer)
*   [NPM](https://www.npmjs.com/) or [Yarn](https://yarnpkg.com/)

### Installation & Setup

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/your-username/Movie-Application.git
    cd Movie-Application
    ```

2.  **Install dependencies:**
    ```sh
    npm install
    # or
    yarn install
    ```

3.  **Set up environment variables:**
    This project requires API keys from TMDB and Appwrite.

    *   Create a `.env` file in the root of the project:
        ```sh
        touch .env
        ```
    *   Add your API keys to the `.env` file. You can get free keys from their respective websites.
        ```
        VITE_TMDB_API_KEY=your_tmdb_api_key
        VITE_APPWRITE_PROJECT_ID=your_appwrite_project_id
        VITE_APPWRITE_DATABASE_ID=your_appwrite_database_id
        VITE_APPWRITE_COLLECTION_ID=your_appwrite_collection_id
        VITE_APPWRITE_ENDPOINT=your_appwrite_endpoint
        ```

4.  **Run the application:**
    ```sh
    npm run dev
    ```
    The application will be available at `http://localhost:5173`.

---

## 📜 Available Scripts

In the project directory, you can run:

*   `npm run dev`: Runs the app in development mode.
*   `npm run build`: Builds the app for production to the `dist` folder.
*   `npm run lint`: Lints the code using ESLint.
*   `npm run preview`: Serves the production build locally.

---

## 📂 Project Structure

```
/
├── public/
│   ├── hero-bg.png
│   ├── hero.png
│   ├── logo.png
│   ├── no-movie.png
│   ├── search.svg
│   ├── star.svg
│   └── vite.svg
├── src/
│   ├── assets/
│   │   └── react.svg
│   ├── components/
│   │   ├── MovieCard.jsx
│   │   ├── Search.jsx
│   │   └── Spinner.jsx
│   ├── App.css
│   ├── App.jsx
│   ├── appwrite.js
│   ├── index.css
│   └── main.jsx
├── .gitignore
├── eslint.config.js
├── index.html
├── package.json
├── README.md
└── vite.config.js
```

### Key Files

*   **`src/App.jsx`**: The main component of the application. It manages the state of the movie list, search term, and loading status.
*   **`src/components/`**: This directory contains all the reusable React components.
    *   **`MovieCard.jsx`**: Displays a single movie with its poster, title, and rating.
    *   **`Search.jsx`**: The search bar component.
    *   **`Spinner.jsx`**: A loading spinner component.
*   **`src/appwrite.js`**: This file contains all the logic for interacting with the Appwrite backend. It handles updating the search count and fetching trending movies.
*   **`src/index.css`**: Contains the global styles and Tailwind CSS configuration.
*   **`vite.config.js`**: The configuration file for Vite.
*   **`package.json`**: Lists the project dependencies and scripts.

---

## 🤔 How It Works

The application fetches movie data from the TMDB API. When a user searches for a movie, the search term is debounced to avoid making too many API requests. The search results are then displayed in a grid of movie cards.

The Appwrite backend is used to track trending movies. Every time a user searches for a movie, the search term and the first result are sent to Appwrite. Appwrite then increments a counter for that search term. The "Trending Movies" section displays the top 5 most searched movies.

---

## 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for more details.