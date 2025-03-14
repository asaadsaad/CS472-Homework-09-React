## CS472-Homework-09-React
Create a React application that displays a list of products. Each product should have a `name`, `price`, and an `in stock` status. Users should be able to toggle the `inStock` status of a product by clicking a button. 

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
Install [Tailwindcss](https://tailwindcss.com/docs/guides/vite) and extend the `components` layer with the following styles:
```css
@layer components {
   .out-of-stock {
        @apply text-red-500;
    }
   .in-stock {
        @apply text-green-500;
    } 
}
```
## `App` Component
* The application container, which renders the `ProductsList` component.

## `ProductsList` Component:
* The list of products is declared within the `ProductsList` component state.
* Create the `ProductsList` component and display each product using a re-usable `Product` component.
* Each product should display its `name`, `price`, and `inStock` status.
* Use conditional rendering to display the product name in red if it is not in stock, and in green otherwise.

## `SingleProduct` Component:
* Create a `SingleProduct` component that displays an individual product.
* Use props spread to pass down the product data.
  
## Event Handling:
* Add a button to the `SingleProduct` component to toggle the in stock status of the product. Because all props are readonly, to change the state of a parent component from a child component, the parent component must pass down a function reference, when called it changes the state of the parent component.

Note: Solve the question in two different ways; first declare the state with `useState()`, later declare the state with `useReducer()`.
