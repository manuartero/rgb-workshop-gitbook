# Testing Unitario y de integración

### Jest

{% tabs %}
{% tab title="Sintaxis BDD" %}
```javascript
  describe('module', () => {
    it('test case', () => {
      /* ... */`
      
    })
  })
```
{% endtab %}

{% tab title="Métodos 'ciclo de vida'" %}
```javascript
  beforeEach()
  afterEach()

  beforeAll()
  afterAll()
```
{% endtab %}

{% tab title="Aserciones básica" %}
```javascript
  expect(value)

    .not
    .toBe(value)
    .toBeInstanceOf(Class)
    .toBeTruthy()
    .toEqual(value)
    .toHaveProperty(keyPath, value)
    .toMatch(regexOrString)
    .toMatchObject(object)
    .toThrow(error)
    .toThrowErrorMatchingSnapshot()
```
{% endtab %}

{% tab title="Mocks" %}
```javascript
  const fn = jest.fn()
  const fn = jest.fn(() => 'hello')

  expect(fn)
    .toHaveBeenCalled()
    .toHaveBeenCalledTimes(number)
    .toHaveBeenCalledWith(arg1, arg2, ...)
```
{% endtab %}
{% endtabs %}

{% embed url="https://devhints.io/jest" %}

### @testing-library/react

{% tabs %}
{% tab title="Métodos de renderizado" %}
```javascript
  render()
  renderHook()
  act()
```

{% embed url="https://testing-library.com/docs/react-testing-library/api#render" %}
{% endtab %}
{% endtabs %}

### @testing-library/jest-dom

{% tabs %}
{% tab title="métodos de búsqueda" %}
```javascript
getBy()
findBy()
queryBy()
getAllBy()
findAllBy()
queryAllBy()
```

{% embed url="https://testing-library.com/docs/react-testing-library/cheatsheet/#queries" %}
{% endtab %}
{% endtabs %}
