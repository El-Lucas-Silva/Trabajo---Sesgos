# Análisis de sesgos en noticias

Este trabajo tiene como objetivo **detectar posibles sesgos en el lenguaje** de un corpus de noticias en español. Analizando relaciones semánticas entre palabras potencialmente sesgadas.

> El corpus se obtuvo de la columna "news" del archivo CSV "df_total.csv"

## Procedimiento

Se instalaron y cargaron las librerías necesarias, en conjunto al corpus (df_total.csv). Luego, se tokenizo el texto y se convirtieron palabras a minusculas, para seguidamente realizar un entrenamiento del modelo con ayuda de Word2Vec.
Posteriormente, se eligieron las palabras...
> mujer, hombre, joven, viejo, gordo, gorda, inmigrante, refugiado, extranjero, turista, experto, ángel, villano, rico, pobre | NOTA: No todas fueron graficadas.

Esta elección de palabras se realizo con el fin de detectar sesgos en las mismas con una grafica 2D hecha con PCA.


## Conclusiones
**"Hombre", "viejo" y "rico"** aparecieron demasiado cerca entre si, lo que podría indicar que el corpus asocia frecuentemente lo masculino con la vejez, la experiencia o la clase alta.
Por otro lado, **"Mujer" y "joven"** se encuentran relativamente cerca abajo en la derecha, pero considerablemente lejos de tanto **hombre** como **viejo**, lo que puede sugerir una asociación entre las mujeres y lo juvenil o novedoso.
**"Refugiado"** se encuentra alejado de las demás palabras, especialmente de **mujer**, lo que puede verse como que no hay relación entre **mujeres** y **refugiados**, o que practicamente no hay mujeres refugiadas.
**"Pobre"** esta en un punto medio entre **"Hombre"** y **"Refugiado"**, esto se puede considerar como que la pobreza se encuentra mucho mas presente en los hombres o refugiados, antes que en las mujeres.
En cuanto al resto de palabras que se tomaron, todas se encuentran demasiado distanciadas como para detectar algún sesgo en particular. Aun así, esto no quita el hecho de que los sesgos son presentes y que se deben de tener en cuenta al momento de querer trabajar con información delicada.

<img width="810" height="590" alt="image" src="https://github.com/user-attachments/assets/a0372fbd-645c-418f-9948-cd8504ea6cb8" />
