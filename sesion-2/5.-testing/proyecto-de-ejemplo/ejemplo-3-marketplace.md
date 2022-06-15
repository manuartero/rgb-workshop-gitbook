# Ejemplo 3 - marketplace

{% tabs %}
{% tab title="marketplace.tsx" %}
```jsx
import React from "react"
import { getItems } from "../services/api.js"
import ItemGrid from "./item-grid"
import Cart from "./cart"
import "./marketplace.css"

function Marketplace() {
  const [items, setItems] = React.useState([])
  const [cartItems, setCartItems] = React.useState([])

  React.useEffect(() => {
    getItems().then(setItems)
  }, [])

  const onItemClick = (item) => {
    setCartItems((carItems) => [item, ...carItems])
  }

  return (
    <main className="marketplace">
      <Cart items={cartItems} />
      <ItemGrid items={items} onItemClick={onItemClick} />
    </main>
  )
}

export default Marketplace
```
{% endtab %}

{% tab title="marketplace.test.tsx" %}
```tsx
import { render, screen, waitFor } from "@testing-library/react";
import * as api from "./simple-ts-app/src/services/api.js";
import Marketplace from "./simple-ts-app/src/components/marketplace";

jest.mock("../services/api.js");

describe("<Marketplace />", () => {
  const items = [
    { name: "item 1", price: 0.01 },
    { name: "item 2", price: 0.03 },
    { name: "item 3", price: 0.04 },
  ];

  test("render happy case", async () => {
    // @ts-ignore
    api.getItems.mockResolvedValue(items);

    render(<Marketplace />);
    const el = screen.getByRole("main");

    await waitFor(() => {
      expect(el).toBeInTheDocument();
    });
  });

  test("fetches the API once: getItems()", async () => {
    // @ts-ignore
    api.getItems.mockResolvedValue(items);

    render(<Marketplace />);
    await waitFor(() => {
      expect(api.getItems).toHaveBeenCalledTimes(1);
    });
  });
});
```
{% endtab %}
{% endtabs %}
