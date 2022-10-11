# tc-test-frontend

Test de uso basico de Vuejs e introducción a diseños de frontend que realizamos actualmente.

## Instalar dependencias:

`npm install`

## Objetivo:

Realizar el diseño estipulado en el componente **./components/Test.vue** utilizando los datos provenientes de la api.

El unico archivo que puede modificarse es el **./components/Test.vue**

## Diseño:

https://www.figma.com/file/adyfg0b2Lxbo9tomDWzv5R/LA---Cuarentena?node-id=2%3A23

## Api:

https://api.turismocity.com/cuarentena/products

## Optativo:

Realizar el header y el footer que aparece en el diseño como parte del ejercicio. 

## Levantar el proyecto:

`npm run serve`

## Url:

http://localhost:8080/

## Descripcion de los archivos:

- **./README.md:** Readme

- **./main.js:** Archivo base del proyecto

- **.App.vue:** Componente base del proyecto

- **./components/Test.vue:** Component de test, este es el componente donde hay que trabajar

## Respecto al formato de los productos:

Cada item en este array representa una marca que contiene: 

- nombre
- titulo
- subtitulo
- imagen
- link a su pagina principal
- links: conjunto de links representando la oferta de productos de la marca 

Cada item del array de links contiene:

- titulo
- imagen
- link
- subtitulo
- precio

## Ejemplo de un item:

```
{
  "name": "Tuenti",
  "title": "¡Llegaron los Gigas que tu celu pedía! Pasate a Tuenti con una promo exclusiva y disfrutá gratis el primer mes",
  "subtitle": "Con el Promocode Turismocity. Tu Primer Combo Power GRATIS con 10GB + 2GB para Youtube y TikTok por 30 días. Tuenti es la telefonía móvil 100% digital.",
  "home": " https://www.tuenti.com.ar/promocion-turismocity?utm_source=turismocity&utm_medium=landingcuarentena&utm_campaign=consideracion",
  "image": "https://blogimagestc.s3.amazonaws.com/Tuenti_Logo_RGB_POS.png",
  "links": [
    {
      "title": "",
      "link": " https://www.tuenti.com.ar/promocion-turismocity?utm_source=turismocity&utm_medium=landingcuarentena&utm_campaign=consideracion",
      "image": "https://blogimagestc.s3.amazonaws.com/Campanas/Turismocity-01.jpg",
      "price": 0,
      "subtitle": ""
    },
    {
      "title": "",
      "link": " https://www.tuenti.com.ar/promocion-turismocity?utm_source=turismocity&utm_medium=landingcuarentena&utm_campaign=consideracion",
      "image": "https://blogimagestc.s3.amazonaws.com/Campanas/Turismocity-02.jpg",
      "price": 0,
      "subtitle": ""
    },
  ]
}
```
