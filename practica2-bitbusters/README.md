[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/ay-dy5DR)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=11759193&assignment_repo_type=AssignmentRepo)
# Práctica 2

> Lógica Computacional.  
> Semestre 2024-1.  
> Dra. Lourdes del Carmen González Huesca.  
> Fausto David Hernández Jasso.  
> Juan Pablo Yamamoto Zazueta.  
> Juan Alfonso Garduño Solís.  

## Equipo
Lista aquí los nombres de los integrantes del equipo:
> Camacho Gutiérrez Karla Alejandra.

> Hernández Vela Daniel.

> Moreno Castro Fernanda.

> Orta Castillo Angeles.

## Instrucciones

**Resolver en equipos de 2 a 4 integrantes.**

Completa las definiciones de las funciones que se indican a continuación.  
Las firmas de funciones y tipos a utilizar ya están dados, sólo debes escribir las soluciones en las definiciones de función marcadas con `undefined`.  

## Ejercicios

Todos los ejercicios tienen un valor de $\frac{1}{10}$ de la calificación.

1. `esAtomica`: Decide si una fórmula proposicional es atómica. Es decir, es una variable proposicional, o una constante lógica.
2. `numOper`: Devuelve el número de operadores lógicos que contiene una fórmula.
3. `profundidad`: Devuelve la profundidad del árbol de sintaxis que genera una fórmula.
4. `numAtom`: Calcula el número de subfórmulas atómicas presentes en una fórmula dada.
5. `elimDobleNeg`: Elimina todas las dobles negaciones presentes en una fórmula: $$\lnot\lnot A\equiv A$$.
6. `deMorgan`: Aplica las leyes de De Morgan a una proposición.
7. `neg`: Calcula la negación de una fórmula de la lógica proposicional, sin generar dobles negaciones.
8. `fnn`: Calcula la forma normal negativa. Esta consiste en transformar la fórmula de manera que no contenga equivalencias ni implicaciones, y que todas las negaciones presentes afecten únicamente a fórmulas atómicas.
9. `distr`: Aplica leyes distributivas sobre formas normales conjuntivas.
10. `fnc`: Calcula la forma normal conjuntiva. Esta consiste en transformar la fórmula de manera que sea una conjunción de disyunciones.

## Estructura

La práctica está estructurada como un proyecto de [Cabal](https://www.haskell.org/cabal/) que permite ejecutar código de Haskell con sus dependencias, así como realizar pruebas de manera sencilla.

El código a modificar se encuentra en la carpeta `src/`, en 2 archivos:
- `LProp.hs`: Los tipos de datos que se utilizarán en la práctica para modelar la lógica proposicional. Es muy recomendable leer estas definiciones para comprender el resto de la práctica. **No modifiques estas definiciones, o las pruebas pueden fallar.**
- `Practica2.hs`: Funciones variadas sobre lógica proposicional.

Puedes revisar las pruebas que se ejecutan en el archivo `test/Practica2Test.hs`. Si lo deseas, puedes agregar pruebas más exhaustivas. No obstante, está prohibido borrar las pruebas ya existentes.

## Comandos

Para compilar tu código

```shell
cabal build
```

Para ejecutar las pruebas

```shell
cabal test
```

Para abrir tu código en GHCI

```shell
cabal repl

ghci> import LProp
ghci> import Semantica
ghci> import Equivalencias
```


## Errores Comúnes

Para garantizar que todos estamos trabajando bajo el mismo conjunto de herramientas, podemos auxiliarnos de `ghcup` para instalar el mismo compilador y dependencias.

En caso de tener un error relacionado a incompatibilidades de bibliotecas, ejecuta los siguientes comandos en tu terminal:

```shell
ghcup install ghc base-4.14.1.0
ghcup set ghc base-4.14.1.0
cabal update
```

## Notas

- No puedes utilizar ninguna función de la biblioteca estándar de Haskell o de alguna biblioteca externa que te dé la solución directamente.
- Puedes utilizar funciones de la biblioteca estándar siempre y cuando no resuelvan directamente el ejercicio, y puedas explicar su uso.
- Si tienes dudas sobre el código dado, sobre Cabal o algún otro aspecto del proyecto, pregunta al ayudante.
- Si lo deseas, puedes agregar comentarios extras o explicaciones sobre el código, directamente como comentarios en los archivos fuente, o en un apartado en el README.
- Tu código debe ser de tu propia autoría. Esto quiere decir que está estrictamente prohibido compartir o utilizar código de otros compañeros, ya sea de este grupo, de otros grupos (incluyendo aquellos que tomaron el curso anteriormente), o de cualquier solución (si la hubiera) accesible en internet. Ten presente la [Política de Honestidad](https://sites.google.com/ciencias.unam.mx/logicacomp/evaluacion) del curso.
- Las pruebas sirven para encontrar algunas fallas en el código, pero no representan la correctez de este, ni mucho menos la calificación que corresponde. Aún cuando se pasan todas las pruebas, se revisará manualmente el código fuente y se tomará en cuenta para la evaluación.
