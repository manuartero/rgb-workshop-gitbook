---
cover: https://tsh.io/wp-content/uploads/2020/10/react-hooks-best-practices-lead_.jpg
coverY: 226.77202072538861
---

# 8. Patrones comunes en React

### Estado

| Hook           | Uso                                                         |
| -------------- | ----------------------------------------------------------- |
| `useState()`   | React 101                                                   |
| `useReducer(`) | Actualizar partes específicas de un estado complejo.        |
| `useContext()` | Un componente padre maneja el estado accesible por N hijos. |

### Optimización

| hook            | Uso                                                                  |
| --------------- | -------------------------------------------------------------------- |
| `useMemo()`     | Procesar API y cálculos pesados (solo \*muy\* pesados)               |
| `useCallback()` | Evitar una llamada a función (que es dependencia de un `useEffect()` |
|                 |                                                                      |

### Otros

| Hook       | Uso                             |
| ---------- | ------------------------------- |
| `useRef()` | Mantener un valor entre renders |
