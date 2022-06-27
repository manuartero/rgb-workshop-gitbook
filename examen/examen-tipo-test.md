---
description: Marcar todas las opciones que sean correctas
---

# Examen tipo test

#### 1. Metodologías ágiles

* [ ] _Agile_ es una filosofía, _Scrum_ es una posible implementación de _Agile_
* [ ] _Agile_ y _Scrum_ son opuestas. O el equipo usa _Agile_ o usa _Scrum,_ pero nunca ambas ideas a la vez.
* [ ] En el manifiesto ágil, se descarta el valor de una serie de elementos y se fija lo único que tiene validez en el desarrollo de software.
* [ ] En el manifiesto ágil uno de los elementos que se destaca es la adaptación a los cambios.

#### 2. `git`

* [ ] Una vez que un commit no está referenciado por ningún otro commit (ni por una rama ni tag), desaparece para siempre del sistema.
* [ ] Una vez que un commit no está referenciado por ningún otro commit (ni por una rama ni tag), tienes 10 días antes de desaparecer para siempre del sistema.&#x20;
* [ ] Una vez que un commit no está referenciado por ningún otro commit (ni por una rama ni tag), deja de aparecer en el log, pero sigue estando en el sistema y haciendo `git checkout {SHA}` nos moveríamos a él.
* [ ] Una vez que un commit no está referenciado por ningún otro commit (ni por una rama ni tag), deja de aparecer en el log, pero sigue estando en el log de revisiones (`reflog)` en el que se muestran todas las operaciones que se han producido en el repositorio.

#### &#x20;3. Conflictos en `git`

* [ ] Para solucionar un conflicto al mezclar dos ramas, hay que acabar aplicando las dos  versiones de cambios (`theris` y `mine`)
* [ ] Para solucionar un conflicto al mezclar dos ramas, lo mejor es partir de la rama que no conocemos (`theirs`) y sobre esa versión, aplicar nuestro cambios
* [ ] Para solucionar un conflicto al mezclar dos ramas, lo mejor es partir de la rama que conocemos (`mine)` y sobre esa versión, aplicar lo mejor que sepamos los cambios del otro.
* [ ] Para solucionar un conflicto al mezclar dos ramas, lo mejor es borrarlo todo.

#### 4. Testing

* [ ] No hay forma de hacer tests unitarios de la UI de una _webapp_.&#x20;
* [ ] `jest` es el framework que ejecuta los test
* [ ] [`@testing-library`](https://www.npmjs.com/org/testing-library) son una serie de paquetes que ayudan a hacer tests unitarios de la UI de una _webapp_
* [ ] `jest` es un framework de testing e2e (end-to-end)

#### 5. SOLID

* [ ] SOLID son una serie de principios de diseño que nos ayudan a escribir código más legible y mantenible
* [ ] SOLID son una serie de principios de diseño que hay que seguir si quieres convertirte en Maestro Programador.&#x20;
* [ ] La S de SOLID hace referencia a "_1 elemento: 1 funcionalidad_"
* [ ] Es mejor listar un montón de propiedades en la interfaz de un método, aunque luego no vayas a usarlas... "por si acaso"

#### 6. Patrones comunes en React

* [ ] Para manejar el estado de un componente, React ofrece las funciones (hooks) `useState()`, `useContext()` y `useReducer()`
* [ ] Siempre que se pueda, lo mejor es usar un `useEffect()` para manejar el flujo de la aplicación.
* [ ] En la función de cb de un `useEffect()`, se puede devolver una función de _cleanUp_ que sirve para evitar condiciones de carreras entre varias ejecuciones de la función.
* [ ] Se puede conseguir la misma funcionalidad usando `useReducer()` que usando `useState()`

#### 7. Código Limpio

* [ ] Las convenciones en programación son importantes porque hay que seguir la tradición.
* [ ] Al seguir las convenciones en programación, ayudamos a que nuestro código sea más fácil de seguir y además nos podemos beneficiar de herramientas que honren dichas convenciones.&#x20;
* [ ] _KISS_, _Feature Creep_, _Overengineering_ son conceptos que hacen referencia a lo mismo: Cuántas más features y más complejas, mejor.
* [ ] Un buen profesional busca que el código sea fácil de leer y que cuente una historia.&#x20;

#### 8. Nombrado y funciones

* [ ] Buscar nombres reveladores y útiles a variables, clases y funciones es una pérdida de tiempo
* [ ] No existe ninguna guía para encontrar nombres reveladores y útiles a variables clases y funciones
* [ ] Para buscar nombres a las variables, clases y funciones hay que intentar describir para qué sirve, qué hace y por qué; intentar que sea un nombre pronunciable y evitar la desinformación.
* [ ] Las funciones, cuanto más largas y que hagan más cosas, mejor.

#### 9. Documentación (y tipado)

* [ ] En el README de un repositorio espero encontrar cómo instalar y poner a funcionar el proyecto
* [ ] Todos los comentarios son útiles siempre
* [ ] en `js` hay un tipo de comentario (`jsDoc`) con el que podemos marcar el tipado de los argumentos y valor de return de las funciones.
* [ ] Es posible usar `typescript` como una herramienta de análisis estático sobre ficheros `.js` sin la necesidad de escribir en el lenguaje `.ts`

#### 10. Formato del código (y otras herramientas)

* [ ] Los _linter_ son analizadores estáticos de código que buscan posibles errores y construcciones de código sospechosas
* [ ] El principal _linter_ para `js` es `ESLint` al que se le pueden añadir _plugins_ en función de las necesidades de nuestro proyecto
* [ ] _Intellisense_ (de un IDE como el VSCode) __ son las herramientas por las que el IDE permite auto-completar, hacer refactors automáticos o marcar ayudas contextuales.
* [ ] _Prettier_ es un posible formateador de código para `js` `css` `html` `json` (entre otros lenguajes) que nos permite establecer unas reglas de formato comunes en el proyecto.&#x20;

