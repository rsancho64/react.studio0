# react studio0

## Infraestructura: pilas .. Node +?

### El team `node`-`npm` en ubuntu

3 formas de instalar/comprobar:

<https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-20-04>

- [ ] `node.js` con apt desde repositorios: { node; npm }
- [ ] `node.js` con apt desde el repo repositorios (w ppa)
- [ ] usar nvm

```bash
node -v
v18.13.0
npm -v
9.2.0
```

tener actualizado ..que?

- a `node` no tanto, pero
- **`npm`** ***si*** *hay que* tenerlo actualizado.

#### ¿varias versiones en node? `nvm` y el paquete `n`

A **must**: <https://www.sobyte.net/post/2022-04/node-mvn-n/>

- **`n`** depende de node. Es un paquete npm
- **`nvm`** **no** depende de node. **no** es un paquete npm. Instalación separada.
  - A `nvn` *también hay que* tenerlo actualizado.

- [ ] opcion clasica: **`nvm`**
- [x] lightweight user : opcion **[n](https://github.com/tj/n)** (de Tj)
  - [asi](https://github.com/tj/n?tab=readme-ov-file#installation)
  - osea: `sudo npm install -g n` y usandolo como sudoer (`sudo n`)

```bash
sudo n lts    ## 20.11.0
sudo n latest ## 21.6.0
```

- [ ] futuro: ¿tener ambos e instalar versiones node con nvm y conmutarlas con n?

#### best NODE in ubunto (from [nodesource](https://deb.nodesource.com/))  

```bash
sudo apt-get update && sudo apt-get install -y ca-certificates curl gnupg

curl -fsSL https://deb.nodesource.com/gpgkey/nodesource-repo.gpg.key | sudo gpg --dearmor -o /etc/apt/keyrings/nodesource.gpg
NODE_MAJOR=20

echo "deb [signed-by=/etc/apt/keyrings/nodesource.gpg] https://deb.nodesource.com/node_$NODE_MAJOR.x nodistro main" | sudo tee /etc/apt/sources.list.d/nodesource.list

sudo apt-get update && sudo apt-get install nodejs -y
```

## Algunas extensiones

leer [esto](https://www.freecodecamp.org/espanol/news/que-es-linting-y-eslint/)

## Algunas extensiones en code para js

de aqui: <https://www.arsys.es/blog/extensiones-vscode#npm_Intellisense>

- [x] ESLint // linter: un elemento de analisis estático.
- [x] Prettier
- [x] npm Intellisense
- [x] NPM (kasper)
- [ ] JavaScript (ES6) code snippets
- [ ] Import Cost
- [ ] ~~Quokka.js~~
- [ ] Angular TypeScript Snippets for VSCode
- [ ] Angular Language Service
- [ ] ES7 React/Redux/GraphQL/React-Native snippets
- [ ] Simple React Snippets

## React 101

Concepto JS:

Un in-browser JS puede hacer: *todo lo relativo a*

- la manipulación* de la pag. web,
- interaction with the user,
- interaction w the webserver.

Una referencia javascript accesible: <https://javascript.info/intro>

- [ ] recorrer [first-steps](https://javascript.info/first-steps)

Conceptos React:

1. Recorriendo [**react.dev**](https://react.dev/learn)

**app** ~ { componentes }
**componente**:

- *elemento* presente en la UI y que tiene:
  - logica y
  - apariencia.
- van desde un simple *boton* hasta una *pagina*

¿app? try:

`export default` keyword ~ main component (into file).

- [ ] `app0.js` Contiene `export default function MyApp()`
- [ ] `sandbox.html` (wrapped app)(into html) No contiene `export default`. Tiene un `let App = function MyApp()`
- [ ] ejercicio: hacer el sandbox dependiente de app0.js (la importacion)
- [ ] ejercicio: parametrizar el boton replicado (a "i'm the boton1" y "i'm the boton2")

Marcado **JSX** (JS syntax eXtension): es más estricto que HTML (,, mejor)(bueno, todo es mejor que html)

Un componente puede devolver un flujo (secuencia, sucesión de tags JSX. Envueltos:

- en div <div></div>o
- en la marca más simple: `<></>`
  
Dentro de un marcado JSX: escape de datos (acceso a valores js) con curly brackets `{}` ~ operador evaluador

- [ ] ejercicio: css: sacar el estilo de recorte redondo de foto (de Hedi Lamarr) en fichero externo css

```css:
.avatar {
  border-radius: 50%;
}
```

- [ ] elementos condicionales (de renderizado condicional) : proponer ejemplo nuevo
- [ ] elementos listados (sucesión de renderizados) : proponer ejemplo nuevo construyendo una lista de componentes con un `map()` sobre una lista de datos.
- [ ] responsividad con un event-handler

Build too **from scratch** (y subir a un repo):
- [ ] the [tic-tac-toe example](https://react.dev/learn/tutorial-tic-tac-toe) // intro 2 react concepts: **element** + **component** + **property** + **state**. 
- [ ] the [fruits store example](https://react.dev/learn/thinking-in-react) ( to see the same concepts building a UI app )
  
## NEXT steps

- We need a framework, really? [**YES**](https://react.dev/learn/start-a-new-react-project#can-i-use-react-without-a-framework)
- [start-a-new-react-project](https://react.dev/learn/start-a-new-react-project)





