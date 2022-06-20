# ✔ Ejercicio sesión 2

En el Ejemplo 4 (Hook) hemos visto como podemos hacer un test unitario de un Hook creando un componente `TestingComponent()` que llame al hook que queremos testear (`useCart()`)

Otra forma para testear hooks en react es usar la función [`renderHook()`](https://testing-library.com/docs/react-testing-library/api/#renderhook)``

¿Cómo quedaría el test del ejemplo 4 usando la función `renderHook()` en lugar de creando un componente `TestingComponent()` al vuelo ?

{% content-ref url="proyecto-de-ejemplo/ejemplo-4-hook.md" %}
[ejemplo-4-hook.md](proyecto-de-ejemplo/ejemplo-4-hook.md)
{% endcontent-ref %}

```jsx
import { useCart } from "./octo-marketplace/src/hooks/use-cart";
import {renderHook} from '@testing-library/react'

test('render happy case', () => {
  // given
  
  // when
  renderHook(...)
  
  // then
})
```
