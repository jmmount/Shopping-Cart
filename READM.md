# React Shopping Cart

This is a simple React application that displays a list of items with their stock numbers and allows the user to move items into a shopping cart.

## Getting Started

To run this application, follow these steps:

1. Clone the repository or download the source code.
2. Install the necessary dependencies by running the command `npm install` or `yarn install`.
3. Start the development server with `npm start` or `yarn start`.
4. Open your web browser and navigate to `http://localhost:3000` to view the application.

## Features

- Displays a list of items with their stock numbers.
- Provides a button for each item to move it into the shopping cart.
- Keeps track of items in the shopping cart using React's `useState` hook.
- Lists out the items in the shopping cart in a separate column.

## Code Overview

### `NavBar` Component

The `NavBar` component is responsible for rendering the list of items and managing the stock and cart states. It receives the `menuitems` prop, which is an array of objects containing the name and stock of each item.

- The `stock` state is initialized with the `menuitems` prop and is used to keep track of the available stock of each item.
- The `cart` state is initialized as an empty array and is used to store the items that are moved into the shopping cart.
- The `moveToCart` function is called when a button is clicked. It updates the stock and cart states accordingly.
- The `updatedList` variable maps over the `menuitems` array and creates a button for each item.
- The component returns a JSX fragment containing the list of items, a heading for the shopping cart, and the `Cart` component.

### `Cart` Component

The `Cart` component is responsible for rendering the items in the shopping cart. It receives the `cartitems` prop, which is an array of objects representing the items in the cart.

- The `updatedList` variable maps over the `cartitems` array and creates a button for each item.
- The component returns an unordered list containing the buttons representing the items in the cart.

## Usage

Modify the `menuItems` array to add or remove items from the list. Each item should have a `name` and `instock` property representing its name and available stock, respectively.

```javascript
const menuItems = [
  { name: "apple", instock: 2 },
  { name: "pineapple", instock: 3 },
  { name: "pear", instock: 0 },
  { name: "peach", instock: 3 },
  { name: "orange", instock: 1 },
];
```

To move an item into the shopping cart, click on the corresponding button next to the item. The stock count will decrease, and the item will be added to the cart.

## Dependencies

This application uses the following dependencies:

- [React](https://reactjs.org) - A JavaScript library for building user interfaces.
- [React Bootstrap](https://react-bootstrap.github.io) - A popular front-end framework rebuilt for React.

Make sure these dependencies are installed before running the application.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.