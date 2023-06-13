https://localhost:3001 

### Iniciar el servicio 

"Hay que tener 2 cmd abiertos simultáneamente uno con el server y otro con el client"

Entras en la carpeta de server desde el cmd y usas el comando npm start

Entras en la carpeta de client desde cmd  y usas el comando npm start

Una vez ya esta corriendo todo, puedes entrar desde la url de uso en localhost para checkear el desarrollo (ambiente de pruebas)

Luego se tiene que pasar a un servidor para el uso en un ambiente de producción

### Parar el servicio 

Se hace desde la carpeta de servidor usando la combinación rápida de teclas en cmd

Desde la carpeta server y en la carpeta client se usa esta combinación para parar los servicios levantados desde node del Experience Builder Developer

ctrl + C


### Para poder observar que contiene una variable usada en un elemento de react 

Se puede usar la herramienta de react (palabra reservada)

```typescript
debugger
```

Con esta palabra reservada el código del widget // app se para en ese elemento cosa que permite observar que está establecido en cada una de las variables usadas en el código desde la consola del navegador. 

