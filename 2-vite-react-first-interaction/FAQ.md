# Uso das Bibliotecas do Reactjs

## React
Ela pode ser chamada da seguinte forma:
```js
import React from 'react'
```
Importando ela, torna possível utilizar componentes JSX.

Por exemplo, no arquivo `main.jsx` neste projeto possui o componente `<React.StrictMode>` mas também pode ser chamado com `<StrictMode>`

### Hooks (useState)
Hooks são funcionalidades de transformação da biblioteca React. Neste projeto usamos o State.

Para importar:
```js
import { useState } from 'react'
```

Para criar uma variável de estado:
```js
const initialState = 0
const [ count, setCount ] = useState( initialState )
```

Para usar o setter há duas formas:
- passando um valor
- passando uma função -> é tratado como updater function. Para saber mais: [doc](https://pt-br.react.dev/reference/react/useState)

```js
setCount(counter + 1)                // valor
setCounter((counter) => counter + 1) // updater
```

Exemplo de uso:
```html
<button onClick={() => setCount((count) => count + 1)}>
    count is {count}
</button>
```

## React DOM (client)
Existe formas de criar elementos DOM no cliente ou servidor. Aqui usamos o de cliente.

Para importar:
```js
import ReactDOM from 'react-dom/client'
```

Essa biblioteca é utilizada basicamente para criar a raiz e fazer o link com o HTML.
```js
const root = document.getElementById('root')
ReactDOM.createRoot(root).render(
    <App />
)
```

## HTML vs Componentes
O React diferencia a partir de:
- apenas minúsculas: HTML (ex: `<section>`)
- primeira letra maiúscula: Componente (ex: `<Card>`)

## Regras do JSX
- Deve retornar só um elemento (pode usar um Fragmento para encapsular `<> </>`)
- Feche todas as tags: `<img>` vira `<img />`
- use camelCase: `stroke-width` vira `strokeWidth`. `class` vira `className`
    - exceção: `aria-*` e `data-*`

## Javascript no JSX
Só usar chaves `{}`

```js
export default function Avatar() {
  const avatar = 'https://i.imgur.com/7vQD0fPs.jpg';
  const description = 'Gregorio Y. Zara';
  return (
    <img
      className="avatar"
      src={avatar}
      alt={description}
    />
  );
}
```

## Objetos no JSX
Só usar chaves duplas `{{}}`

```js
export default function TodoList() {
  return (
    <ul style={{
      backgroundColor: 'black',
      color: 'pink'
    }}>
      <li>Improve the videophone</li>
      <li>Prepare aeronautics lectures</li>
      <li>Work on the alcohol-fuelled engine</li>
    </ul>
  );
}
```

## Props
Informações passadas de elemento pai para filho

### Passando
```js
<Avatar
    person={{ name: 'Lin Lanying', imageId: '1bX5QH6' }}
    size={100}
/>
```

### Recebendo
```js
function Avatar({ person, size }) {
  // person e size estão disponíveis aqui
}
```

## Tags aninhadas
Podemos fazer que nem no HTML e abrir e fechar tags.
```html
<Card>
    <Avatar/>
</Card>
```

Nesse caso, a tag maior tem acesso às tags filhas por `children`
```js
function Card({ children }) {
  return (
    <div className="card">
      {children}
    </div>
  );
}
```