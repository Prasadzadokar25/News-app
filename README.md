# News App

A simple web application that displays news articles based on different categories and search queries using the News API.

## How I Made This Project

### 1. HTML Structure

I started by creating the `index.html` file which sets up the basic structure of the webpage. This includes:
- A navigation bar with links for different news categories (IPL, Finance, Politics, Sports).
- A search bar for querying specific news topics.
- A main section to display the news articles using a template for the news cards.

### 2. CSS Styling

The `style.css` file is used to style the webpage, ensuring it is visually appealing and responsive. Key styling elements include:
- Setting global styles and font imports.
- Styling the navigation bar, search bar, and news cards.
- Adding hover effects and responsive design elements.

### 3. JavaScript Functionality

The `script.js` file contains the JavaScript code that fetches news articles from the News API and dynamically updates the DOM. Key functions include:

#### fetchNews(query)
This function fetches news articles based on the provided query:
- It constructs the API URL using the base URL, query, and API key.
- It makes a `fetch` request to the News API and parses the JSON response.
- It calls `bindData` to update the DOM with the fetched articles.

#### bindData(articles)
This function binds the fetched news articles to the DOM:
- It clears any existing news cards in the container.
- It iterates over the articles, clones the news card template for each article, and fills it with article data using `fillDataInCard`.
- It appends the populated news cards to the container.

#### fillDataInCard(cardClone, article)
This function fills the cloned news card template with article data:
- It updates the image, title, source, and description fields of the card.
- It formats the publication date and sets the source information.
- It adds an event listener to the card to open the article in a new tab when clicked.

#### onNavItemClick(id)
This function handles category navigation clicks:
- It fetches news articles for the selected category.
- It updates the active state of the navigation items.

#### Event Listeners
- An event listener on `window` load to fetch default news for "India".
- An event listener on the search button to fetch news based on the search query.

## Conclusion

This project demonstrates a simple yet effective way to create a news web application using HTML, CSS, and JavaScript. The application interacts with the News API to fetch and display news articles dynamically based on user interactions. 