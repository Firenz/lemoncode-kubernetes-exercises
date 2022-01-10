# Ejercicios Kubernetes
## Pre-requisitos para ejecutar las aplicaciones en local
* Docker
* node 12.* >

## Ejercicio 1. Monolito en memoria.
Se trata de una aplicación web que expone una aplicación de UI (la típica aplicación TODO), y una API para gestionar en servidor los 'TODOS'. La persistencia de los TODOS es en memoria, eso significa que cuando apaguemos la aplicación dejarán de persistir los datos.

Para construir la imagen de esta aplicación los pasos están expuestos en [00-monolith-in-mem/README.md](https://github.com/Lemoncode/bootcamp-devops-lemoncode/blob/master/02-orquestacion/exercises/00-monolith-in-mem/README.md)

El enunciado del ejercicio lo encontraremos en [00-monolith-in-mem/exercise-monolith-in-memory.md](https://github.com/Lemoncode/bootcamp-devops-lemoncode/blob/master/02-orquestacion/exercises/00-monolith-in-mem/exercise-monolith-in-memory.md)

## Ejercicio 2. Monolito.
Se trata de la misma aplicación pero en este caso la persistencia en memoria se hace a través de una base de datos.

Para ejecutar la aplicación en local podemos seguir los pasos están expuestos en [01-monolith/README.md](https://github.com/Lemoncode/bootcamp-devops-lemoncode/blob/master/02-orquestacion/exercises/01-monolith/README.md)

El enunciado del ejercicio lo encontraremos en [01-monolith/exercise-monolith.md](https://github.com/Lemoncode/bootcamp-devops-lemoncode/blob/master/02-orquestacion/exercises/01-monolith/exercise-monolith.md)

## Ejercicio 3. Aplicación Distribuida
Se trata de dos aplicaciones, una UI expuesta a través de un `nginx` y una `API` que corre sobre `express/nodejs` y se conecta con una base de datos `postgres`.

Para ejecutar en local podemos seguir los pasos expuestos en [02-distributed/README.md](https://github.com/Lemoncode/bootcamp-devops-lemoncode/blob/master/02-orquestacion/exercises/02-distributed/README.md)

El enunciado del ejercicio lo encontramos en [02-distributed/exercise-ingress.md](https://github.com/Lemoncode/bootcamp-devops-lemoncode/blob/master/02-orquestacion/exercises/02-distributed/exercise-ingress.md)
