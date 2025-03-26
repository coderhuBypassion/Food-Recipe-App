# Food Recipe App Project Documentation

## Project Overview

The Food Recipe App is a frontend-focused application that allows users to browse and upload recipes. The application fetches data about recipes and other backend features via an external API. It also includes features such as adding custom recipes and getting recipes based on custom criteria such as available time and the number of people.

## Features

1. **Browse Recipes**: Users can browse a wide variety of recipes fetched from an external API.
2. **Custom Recipe Uploads**: Users can upload their own recipes to the application.
3. **Custom Recipe Search**: Users can search for recipes based on custom criteria such as the available time and the number of people.
4. **Responsive Design**: The application is designed to be responsive and user-friendly on all devices.

## API Usage

The application interacts with an external API to fetch and manage recipe data. The following endpoints are used:

- **GET /recipes**: Fetch a list of recipes.
- **POST /recipes**: Upload a new recipe.
- **GET /recipes/:id**: Fetch details of a specific recipe.
- **PUT /recipes/:id**: Update a specific recipe.
- **DELETE /recipes/:id**: Delete a specific recipe.

The API base URL is `https://forkify-api.herokuapp.com/v2`.

### Example API Calls

1. **Fetch Recipes**
   ```javascript
   fetch('https://forkify-api.herokuapp.com/v2/recipes')
     .then(response => response.json())
     .then(data => console.log(data));
   ```

2. **Upload a New Recipe**
   ```javascript
   fetch('https://forkify-api.herokuapp.com/v2/recipes', {
     method: 'POST',
     headers: {
       'Content-Type': 'application/json'
     },
     body: JSON.stringify({
       title: 'New Recipe',
       ingredients: ['ingredient1', 'ingredient2'],
       instructions: 'Step by step instructions'
     })
   })
     .then(response => response.json())
     .then(data => console.log(data));
   ```

## Custom Features

### Adding Your Own Recipe

Users can add their own recipes to the application by filling out a form with the recipe details. The form includes fields for the recipe title, ingredients, and instructions. Once the form is submitted, the data is sent to the API endpoint to create a new recipe.

### Getting Recipe with Custom Time and Person

Users can search for recipes based on custom criteria such as the available time and the number of people. This feature allows users to find recipes that fit their specific needs and preferences.

## Setup and Installation

To run the project locally, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/coderhuBypassion/Food-Recipe-App.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Food-Recipe-App
   ```
3. Install the dependencies:
   ```bash
   npm install
   ```
4. Start the development server:
   ```bash
   npm run start
   ```

## Conclusion

The Food Recipe App is a versatile and user-friendly application that allows users to browse and upload recipes. With its custom features and API integration, it provides a seamless experience for managing and discovering new recipes.

For more details, visit the [GitHub repository](https://github.com/coderhuBypassion/Food-Recipe-App).
