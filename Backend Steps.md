1. Copy template
2. Install dependencies with bun

```sh
bun add express sequelize mysql2
```

4. Create base folders
```sh
mkdir models controllers routes
```
6. Base server.js app
```js
const express = require('express');
const { sequelize } = require('./models'); // Importa la instancia de Sequelize con los modelos

const app = express();
app.use(express.json());

// Importar y usar las rutas consolidadas desde el archivo index.js
const routes = require('./routes');
app.use('/api', routes); // Prefijo '/api' para todas las rutas

// Sincronizar modelos
sequelize.sync().then(() => {
    console.log('Database & tables created!');
});

// Inicia el servidor
const PORT = 3000;
app.listen(PORT, () => {
    console.log(`Server is running on port ${PORT}`);
});
```
7. Execute server app
```sh
bun run server.js
```
8. Test in CLI with curl
```sh
curl -X GET http://localhost:3000/api/person -H "Content-Type: application/json"
```



```sh
curl -X POST http://localhost:3000/api/person -H "Content-Type: application/json" -d '{"name": "John Doe", "email": "john.doe@example.com"}'
```