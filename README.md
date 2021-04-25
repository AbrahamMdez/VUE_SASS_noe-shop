# neo-shop

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

SOLO ESTA LA VERSION MOVIL, MOBILE FIRST.

Use medidas relativas en lugar de media querys.
Normalmente en mi dia a dia uso los selectores a la hora de realizar stilos css, pero leí vuestra documentación y usé la metodología BEM.
También use SASS como procesador en Vue.

No fuí capaz a hacer funcionar el slide, estuve intentado cambiar el sistema ahora en la mañana, pero tengo algun tipo de error, seguiré intentadolo en estos dias,
no obstante dejo ambas formas que estoy utilizando, la forma de iterar el JSON la dejo comentada para que podais ver como lo hice y dejo funcionando la forma solo con 
CSS.

1. Elegí Vue como framework.
2. Aproveché los JSON, como podrás ver en el componente de Slide y componente Main, en ambos itero los JSON e imprimo la data,
   tuve un problema con las imagenes, lo que hice fué buscar imagenes similares por la web y las metí en los JSON.
3. Use Grid y Flex, como podrás ver en el componente Main, uso Grid para los distintos articulos y tambien en cada articulo decidí usar Grid
   para ubicar tanto la imagen del articulo, precio, boton de compra...
4. Todo son componentes, tanto el Footer, como el Header, Slide...reutilizables.

Espero os guste, creo que es muy mejorable el responsive, pero creo que la parte funcional, está bastante bien,
cualquier cosa, no dudes en escribirme.
