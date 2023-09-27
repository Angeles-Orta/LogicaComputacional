[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/u8dlMkLj)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=11634731&assignment_repo_type=AssignmentRepo)
# Práctica 1

> Lógica Computacional.  
> Semestre 2024-1.  
> Dra. Lourdes del Carmen González Huesca.  
> Fausto David Hernández Jasso.  
> Juan Pablo Yamamoto Zazueta.  

## Instrucciones

**Resolver en equipos de 2 a 4 integrantes.**

- Completa las definiciones de las funciones que se indican a continuación.
- Las firmas de funciones y tipos a utilizar ya están dados, sólo debes escribir las soluciones en las definiciones de función marcadas con `{-- Por completar. --}`.
- Debes dar todas las definiciones para poder compilar el proyecto. Si deseas probar tu código en GHCI sin haber escrito todas las definiciones, puedes dar la definición `error "por completar"`, o comentar la firma de la función incompleta.
- No cambies los nombres de las firmas de función, pues son los nombres que utilizan las pruebas.

## Ejercicios

Todos los ejercicios tienen un valor de $\frac{1}{16}$ de la calificación.

1. `subconj`: Dada una lista, regresa las `2^n` posibles sublistas, donde `n` es la longitud de la lista original.
2. `eliminaRepetidos`: Dada una lista de elementos que se pueden comparar bajo igualdad, regresa una lista con los mismos elementos, pero sin repeticiones presentes..
3. `interp`: Dado un estado y una fórmula proposicional, decide si la fórmula se satisface o no..
4. `vars`: Dada una proposición, devuelve los nombres de las variables presentes.
5. `estados`: Dada una proposición, devuelve todos los posibles estados de sus variables.
6. `tautologia`: Dada una proposición, devuelve todos los estados de sus variables que son modelos de la proposición; es decir, la satisfacen.
7. `satisfacibleEn`: Dada una proposición, decide si la fórmula es una tautología.
8. `satisfacible`: Dado un estado y una proposición, decide si esta se satisface.
9. `insatisfacibleEn`: Dado un estado y una proposición, decide si esta no se satisface.
10. `contrad`: Dada una proposición, decide si la fórmula es una contradicción.
11. `estadosConj`: Dada una lista de proposiciones, devuelve todos los posibles estados de las variables presentes en las fórmulas.
12. `satisfacibleEnConj`: Dado un estado y una lista de proposiciones, decide si se satisfacen todas con el estado.
13. `consecuencia`: Dada una lista de proposiciones como premisas y una fórmula como conclusión, decide si se sigue la conclusión de las premisas.
14. `equiv`: Dadas 2 fórmulas de la lógica proposicional, decide si son equivalentes entre sí; es decir, si su evaluación siempre es la misma dado un estado.
15. `elimEquiv`: Dada una fórmula de la lógica proposicional, elimina las equivalencias presentes, usando la equivalencia: `a <-> b = (a -> b) ^ (b -> a)`.
16. `elimImpl`: Dada una fórmula de la lógica proposicional, elimina las implicaciones presentes, usando la equivalencia: `a -> b = -a ^ b`.

## Estructura

La práctica está estructurada como un proyecto de [Cabal](https://www.haskell.org/cabal/) que permite ejecutar código de Haskell con sus dependencias, así como realizar pruebas de manera sencilla.

El código a modificar se encuentra en la carpeta `src/`, en 3 archivos:
- `LProp.hs`: Los tipos de datos que se utilizarán en la práctica para modelar la lógica proposicional. Es muy recomendable leer estas definiciones para comprender el resto de la práctica. **No modifiques estas definiciones, o las pruebas pueden fallar.**
- `Semantica.hs`: Funciones relacionadas con la semántica de la lógica proposicional.
- `Equivalencias.hs`: Funciones relacionadas con equivalencias entre fórmulas de la lógica proposicional.

Puedes revisar las pruebas que se ejecutan en el archivo `test/Practica1Test.hs`. Si lo deseas, puedes agregar pruebas más exhaustivas. No obstante, está prohibido borrar las pruebas ya existentes.

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


## Notas

- No puedes utilizar ninguna función de la biblioteca estándar de Haskell o de alguna biblioteca externa que te dé la solución directamente.
- Puedes utilizar funciones de la biblioteca estándar siempre y cuando no resuelvan directamente el ejercicio, y puedas explicar su uso.
- Si tienes dudas sobre el código dado, sobre Cabal o algún otro aspecto del proyecto, pregunta al ayudante.
- Si lo deseas, puedes agregar comentarios extras o explicaciones sobre el código, directamente como comentarios en los archivos fuente, o en un apartado en el README.
- Tu código debe ser de tu propia autoría. Esto quiere decir que está estrictamente prohibido compartir o utilizar código de otros compañeros, ya sea de este grupo, de otros grupos (incluyendo aquellos que tomaron el curso anteriormente), o de cualquier solución (si la hubiera) accesible en internet. Ten presente la [Política de Honestidad](https://sites.google.com/ciencias.unam.mx/logicacomp/evaluacion) del curso.
- Las pruebas sirven para encontrar algunas fallas en el código, pero no representan la correctez de este, ni mucho menos la calificación que corresponde. Aún cuando se pasan todas las pruebas, se revisará manualmente el código fuente y se tomará en cuenta para la evaluación.
