# Desafío evaluado - Clases en ES6

Desafío «Clases en ES6» del módulo 4 del bootcamp Full Stack JavaScript de Talento Digital.

## Descripción

En este desafío se validarán nuestros conocimientos de Programación Orientada a Objetos y ES6. Para lograrlo, se necesitará aplicar lo estudiado previamente en el material
disponibilizado correspondiente a la unidad.

## Requerimientos

1. Mantén un estilo de código (espacios, saltos de línea, indentación) uniforme en el proyecto. (1 Puntos)
2. Utilizar ES6 para el desarrollo de todo el programa. (2 Puntos)
3. Implementar las funcionalidades de Babel instalando las dependencias necesarias para su funcionamiento. (1 Puntos)
4. Crear y configurar el archivo de babel.config.json. (1 Puntos)
5. Crear los tres archivos de JavaScript e implementar la modularidad y clases de ES6. (1 Puntos)
6. Implementar getter y setter para acceder y/o modificar los datos de las clases. (2 Puntos)
7. Implementar un método que permita calcular el impuesto total a pagar por parte del cliente. (1 Puntos)
8. Transpilar el código de ES6 a ES5 utilizando babel desde la terminal. (1 Puntos)

## Instrucciones para ejecutar Babel

## Empezando 🚀

Inicializar el proyecto con npm y crear el archivo package.json

```bash
npm init -y
```

Instalar Babel y sus dependencias como lo son:

- **@babel/preset-env** que es un conjunto de plugins de Babel que permiten transformar el código de JavaScript moderno (ES6+) a JavaScript compatible con versiones anteriores de JavaScript.
- **@babel/cli** que es una interfaz de línea de comandos para Babel.
- **@babel/core** que es el núcleo de Babel.
- **@babel/polyfill** que es un conjunto de polyfills para replicar las funcionalidades de los nuevos métodos y objetos de JavaScript que no son soportados por todos los navegadores.

```bash
npm i -D @babel/preset-env @babel/cli @babel/core @babel/polyfill
```

Crear el archivo de configuración de Babel llamado `babel.config.json` y agregar el siguiente contenido:

```json
{
  "presets": [
    [
      "@babel/env",
      {
        "targets": {
          "edge": "17",
          "firefox": "60",
          "chrome": "67",
          "safari": "11.1"
        },
        "useBuiltIns": "usage",
        "corejs": "3.6.4",
        "forceAllTransforms": true
      }
    ]
  ]
}
```

La librería `core-js` es una dependencia de `@babel/polyfill` que se debe instalar para que Babel pueda usar los polyfills.

```bash
npm i core-js
```

Por ultimo debes correr el siguiente comando para que Babel transforme el código de ES6+ a JavaScript compatible con versiones anteriores de JavaScript.

```bash
npx babel -d dist/ src/ --config-file ./babel.config.json
```
