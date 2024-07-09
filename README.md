## CS472-Homework-09-React
Create a React application that displays a list of products. Each product should have a `name`, `price`, and an `in stock` status. Users should be able to toggle the `inStock` status of a product by clicking a button.

## Styling:
Create a CSS file to style the components and import this CSS file into your components.
```css
.product-name {
  font-size: 1.5rem;
}

.out-of-stock {
  color: red;
}

.in-stock {
  color: green;
}

button {
  margin-top: 10px;
}
```
## `App` Component
* The `App` component that maintains the list of products in its state.
* Pass this state down to the `ProductList` component as props.
```typescript
const [products, setProducts] = useState([
    { id: 1, name: 'Apple', price: 1, inStock: true },
    { id: 2, name: 'Banana', price: 1, inStock: false },
    { id: 3, name: 'Cherry', price: 2, inStock: true },
  ]);
```
## `ProductList` Component:
* Create a `ProductList` component that receives a list of products as a prop and displays them each as a re-usable `Product` component.
* Each product should display its `name`, `price`, and `inStock` status.
* Use conditional rendering to display the product name in red if it is not in stock.

## `Product` Component:
* Create a `Product` component that displays an individual product.
* Use props and props spread to pass down the product data.
  
## Event Handling and useState:
* Implement a button in the `Product` component to toggle the in stock status of the product.
* Use the useState hook to manage the in stock status.
