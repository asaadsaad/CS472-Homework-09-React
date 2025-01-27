## CS472-Homework-09-React
Create a React application that displays a list of products. Each product should have a `name`, `price`, and an `in stock` status. Users should be able to toggle the `inStock` status of a product by clicking a button. You should save the state within a reducer and declare an action for toggling the `inStock` status.

```typescript
interface Product { id: number, name: string, price: number, inStock: boolean; };
type State = Product[];

const initial_state: State = [
    { id: 1, name: 'Apple', price: 1, inStock: true },
    { id: 2, name: 'Banana', price: 1, inStock: false },
    { id: 3, name: 'Cherry', price: 2, inStock: true },
]
```

## Styling:
Create a CSS file to style the components and import this CSS file into your components.
```css
.out-of-stock {
  color: red;
}

.in-stock {
  color: green;
}
```
## `App` Component
* The application container, which renders the `ProductsList` component.

## `ProductsList` Component:
* The list of products is declared within the `ProductsList` component state.
* Create the `ProductsList` component and display each product using a re-usable `Product` component.
* Each product should display its `name`, `price`, and `inStock` status.
* Use conditional rendering to display the product name in red if it is not in stock, and in green otherwise.

## `Product` Component:
* Create a `Product` component that displays an individual product.
* Use props and props spread to pass down the product data.
  
## Event Handling:
* Add a button to the `Product` component to toggle the in stock status of the product.
