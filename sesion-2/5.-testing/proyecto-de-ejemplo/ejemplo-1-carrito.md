---
layout: landing
---

# Ejemplo 1 - carrito

{% tabs %}
{% tab title="cart.jsx" %}
```jsx
import { ReactComponent as ShoppingCart } from "../assets/shopping-cart.svg"
import "./cart.css"
import { ReactComponent as EthLogo } from "../assets/eth-logo.svg"

function Cart({ items }) {
  const total = items.length

  return (
    <div className="cart" role='banner'>
      <ShoppingCart className="cart-icon" />
      <span>{total}</span>
      <EthLogo className="eth-logo" />
    </div>
  )
}

export default Cart
```
{% endtab %}

{% tab title="cart.spec.jsx" %}
```jsx
import { render, screen } from '@testing-library/react'
import Cart from './simple-ts-app/src/components/cart'

describe('<Cart />', () => {
  it('render happy case', () => {
    const items = [
      { name: 'item 1', price: 0.01 }, 
      { name: 'item 2', price: 0.01 }, 
      { name: 'item 3', price: 1.00 }
    ]
    render(<Cart items={items} />)
    const el = screen.getByRole('banner')
    expect(el).toBeInTheDocument()
  })
})
```
{% endtab %}
{% endtabs %}
