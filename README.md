
# Movie App

A React-based movie application that displays popular, top-rated, and upcoming movies using data from The Movie Database (TMDb) API. It features dynamic theme switching (light/dark mode) and filtering options for movie ratings.

## Features

- **Dynamic Theme Switching**: Toggle between light and dark modes.
- **Movie Listings**: View movies categorized by popularity, top-rated, or upcoming.
- **Filter by Rating**: Filter movies based on user-defined rating thresholds.
- **Sorting**: Sort movies by release date or rating in ascending/descending order.

## Demo

Link to the deployed app (if available).

## Technologies Used

- **React**: Front-end library for building user interfaces.
- **TMDb API**: Fetch movie data such as posters, ratings, and release dates.
- **CSS**: Styling for various components.

## Installation

### Prerequisites

Before you begin, ensure you have [Node.js](https://nodejs.org/) and [npm](https://www.npmjs.com/) installed on your machine.

### Clone the Repository

```bash
git clone https://github.com/yourusername/movie-app.git
cd movie-app
```

### Install Dependencies

```bash
npm install
```

### Run the Development Server

```bash
npm start
```

The application should now be running on `http://localhost:3000`.

## Structure

### `src/App.jsx`

- The main entry point for the app. It imports components such as `Navbar` and `MovieList` to display the movie listings.

### `src/components/Navbar/Navbar.jsx`

- Displays the main navigation bar with links to different movie categories (Popular, Top Rated, Upcoming).
- Contains the `DarkMode` component for toggling the theme.

### `src/components/DarkMode/DarkMode.jsx`

- Handles the dark and light mode functionality.
- Stores the selected theme in `localStorage` and applies it to the body element.

### `src/components/MovieList/MovieList.jsx`

- Fetches and displays a list of movies from TMDb, based on the selected category (Popular, Top Rated, Upcoming).
- Supports filtering by movie rating and sorting by release date or rating.

### `src/components/MovieList/MovieCard/MovieCard.jsx`

- Represents an individual movie card, displaying the poster, title, release date, rating, and description.
- Links to the movie's official page on TMDb.

### `src/components/MovieList/FilterGroup/FilterGroup.jsx`

- Displays a list of available rating filters that can be applied to the movie list.

### `src/components/Navbar/Navbar.css`

- Contains styling for the navbar and dark/light mode toggle.

### `src/components/MovieList/MovieList.css`

- Contains styling for the movie list, sorting options, and filter buttons.

### `src/components/MovieList/MovieCard/MovieCard.css`

- Contains styling for individual movie cards.

### `src/components/MovieList/FilterGroup/FilterGroup.css`

- Contains styling for the filter group and its items.

### `src/components/DarkMode/DarkMode.css`

- Contains styling for the dark mode toggle switch and its appearance.

## API Key

To use the movie data from The Movie Database (TMDb) API, you will need an API key. Follow these steps:

1. Go to the [TMDb website](https://www.themoviedb.org/).
2. Create an account or log in.
3. Go to your account settings and find your API key.
4. Replace the API key in `MovieList.jsx` with your own.

```js
const response = await fetch(
  `https://api.themoviedb.org/3/movie/${type}?api_key=YOUR_API_KEY`
);
```

## Contributing

If you'd like to contribute to this project, please follow these steps:

1. Fork this repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -am 'Add new feature'`).
5. Push to your branch (`git push origin feature-branch`).
6. Create a pull request.

## License

This project is licensed under the MIT License.
