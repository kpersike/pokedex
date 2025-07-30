# Copilot Instructions for This Pokedex Project

## Overview
This project is a simple web-based Pokedex built with vanilla JavaScript, HTML, and CSS. It fetches Pokémon data from the public [PokeAPI](https://pokeapi.co/) and displays it in a styled list. The UI is responsive and styled with custom CSS.

## Key Components
- **index.html**: Main entry point. Loads CSS and JS, and contains the root markup for the Pokedex.
- **assets/js/poke-api.js**: Defines the `PokeAPI` object and its `getPokemons` method, which fetches Pokémon data from the API.
- **assets/js/main.js**: Handles DOM manipulation, rendering Pokémon data into the HTML list, and calls `PokeAPI.getPokemons()`.
- **assets/css/global.css** and **pokedex.css**: Contain global and component-specific styles.

## Data Flow
- `main.js` calls `PokeAPI.getPokemons()` to fetch a list of Pokémon.
- The results are mapped and rendered as HTML list items in the `#pokemonsList` element.
- Each Pokémon's details are fetched individually using their API URLs.

## Patterns & Conventions
- **API Calls**: All API interactions are handled in `poke-api.js`. Use `fetch` and promise chaining for async operations.
- **DOM Manipulation**: Only `main.js` should update the DOM. Use template literals for HTML generation.
- **Styling**: Use the provided CSS files. Do not inline styles in HTML or JS.
- **Extensibility**: Add new features (e.g., filtering, pagination) by extending `main.js` and/or `poke-api.js`.

## Debugging & Development
- No build step or bundler is required; open `index.html` directly in a browser.
- Use browser dev tools for debugging. `poke-api.js` includes a `debugger` statement for inspecting API results.
- No automated tests are present; manual testing is expected.

## External Dependencies
- [PokeAPI](https://pokeapi.co/) for Pokémon data
- [Normalize.css](https://necolas.github.io/normalize.css/) and [Google Fonts](https://fonts.google.com/specimen/Roboto) via CDN

## Example Usage
```js
PokeAPI.getPokemons(0, 10).then(pokemons => {
  // pokemons is an array of detailed Pokémon objects
});
```

## File Structure Reference
- `index.html`
- `assets/js/poke-api.js`
- `assets/js/main.js`
- `assets/css/global.css`
- `assets/css/pokedex.css`

---
If any conventions or workflows are unclear, please ask for clarification or examples from the codebase.
