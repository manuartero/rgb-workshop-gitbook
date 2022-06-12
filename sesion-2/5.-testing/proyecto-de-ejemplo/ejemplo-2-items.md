# Ejemplo 2 - items



```jsx
import { ReactComponent as EthLogo } from "../assets/eth-logo.svg"
import "./item-grid.css"
import "./scheleton.css"

function Scheleton() {
  return (
    <section className="item-grid">
      {Array.from({ length: 5 }).map((_, i) => (
        <article className="scheleton-item" key={`scheleton-${i}`}>
          <div className="scheleton-title" />
          <div className="scheleton-img" />
          <div className="scheleton-card-info" />
        </article>
      ))}
    </section>
  )
}

function ItemGrid({ items, onItemClick }) {
  if (items.length === 0) {
    return <Scheleton />
  }

  return (
    <section className="item-grid">
      {items.map((item, i) => (
        <article className="item-card" onClick={() => onItemClick(item)} key={`item-${i}`}>
          <span>{item.name}</span>
          <img src={item.imageUrl} alt={`item named ${item.name}`} />
          <div className="item-card-info">
            <span className="item-price">{item.price}</span>
            <EthLogo className="eth-logo" />
          </div>
        </article>
      ))}
    </section>
  )
}

export default ItemGrid

```

```jsx
import { fireEvent, render, screen } from "@testing-library/react";
import ItemGrid from "./simple-ts-app/src/components/item-grid";

describe("<ItemGrid />", () => {
  const items = [
    { name: "item 1", price: 0.01 },
    { name: "item 2", price: 0.02 },
    { name: "item 3", price: 0.03 },
  ];

  test("renders scheleton if no items", () => {
    render(<ItemGrid items={[]} onItemClick={() => {}} />);
    const elements = screen.getAllByRole("article");
    elements.forEach((el) => {
      expect(el).toHaveClass("scheleton-item");
    });
    expect(elements.length).toEqual(5);
  });

  test("renders every item as an article", () => {
    render(<ItemGrid items={items} onItemClick={() => {}} />);
    const elements = screen.getAllByRole("article");
    elements.forEach((el) => {
      expect(el).toHaveClass("item-card");
    });
    expect(elements.length).toEqual(3);
  });

  test("each item is clickable", () => {
    const onClick = jest.fn();
    render(<ItemGrid items={items} onItemClick={onClick} />);
    const item = screen.getByText("item 2");

    fireEvent.click(item);

    expect(onClick).toHaveBeenCalledTimes(1);
    expect(onClick).toHaveBeenCalledWith({ name: "item 2", price: 0.02 });
  });
});

```
