## Random Variables and Expected Value

When you're working with different variables, how can you tell which ones are normal (or expected) and which ones are out-of-the-blue radom? In this lesson, we'll teach you how to identify and analyze random and expected values.

Cuando trabajas con diferentes variables, como puedes distinguir cuales son normales (o esperadas) y cuales son completamete aleatorias? En esta lección, te enseñaremos a identificar y analizar valores aleatorios y esperados.

## Learning Objectives

By the end of this lesson, you'll be able to:

- Define a random variable.
- Differentiate between a discrete random variable and a continuous random variable.
- Explain the expected value of a random variable.

Al final de esta lección, podrás:

1. Definir una variable aleatoria.
2. Diferenciar entre una variable aleatoria discreta y una variable aleatoria continua.
3. Explicar el valor esperado de una variable aleatoria.

## What are Random Variables?

*Random variables* are numerical outcomes of a chance event. They're important when quantifying an outcome for a random process.

Supppose you flip a coin three times and count the number of times that the result is heads. Let X represent this count.

X can equal 0, 1, 2 or 3 because it is possible for us to flip heads zero, one, two, or three times. X is the random variable here. It represents the outcome of your experiment (flipping three coins) with a number (how many heads you flipped).

Once a categorcical outcome is quantified, we can work with the different forms of probability and statistics from that outcome.

--
Las variables aleatorias son resultados numéricos de un evento aleatorio. Son importantes cuando se cuantifica el resultado de un proceso aleatorio.

Supongamos que lanzas una moneda tres veces y cuentas el número de veces que el resultado es cara. Sea
X la variable que representa este conteo.

X puede ser igual a 0, 1, 2 o 3, ya que es posible que obtengas cara cero, una, dos o tres veces.
X es la variable aleatoria en este caso. Representa el resultado de tu experimento (lanzar tres monedas) con un número (cuántas caras obtuviste).

Una vez que un resultado categórico se cuantifica, podemos trabajar con diferentes formas de probabilidad y estadística a partir de ese resultado.

## Distribution of Random Variables

The *distribution of a random variable* describes all possible values of a random variable and how likely that variable is to take on each of those values.

Returning to our coin flip example - you flipped a coin three times and recorded the number of heads that resulted. The table below lists all possible values of our random variable, X(0,1,2,3), and how likely X is to take on each value (0.125, 0.375, 0.375, 0.125):

Assuming this coin is fair and that each flip is independent of the others, we can derive the probability of each outcome:

<img width="619" alt="image" src="https://github.com/user-attachments/assets/166ddbca-13dc-4da0-bc53-18fdc4599bbd" />

We call this the distribution of a random variable. If we know the distribution of a random variable, we can answer nearly every potential question we have about x, such as:

- If we were to flip a coin three times, what is the probability of observing at least two heads?
- If we were to flip a coin three times, how likely is it that we observe exctly one head?
- If we were to flip a coin three times, what is the probaibilty of seeing either all heads or all tails?

--
La distribución de una variable aleatoria describe todos los valores posibles que puede tomar dicha variable y la probabilidad de que la variable tome cada uno de esos valores.

Volviendo a nuestro ejemplo del lanzamiento de la moneda: lanzaste una moneda tres veces y registraste el número de caras que resultaron. La siguiente tabla enumera todos los valores posibles de nuestra variable aleatoria,
X (0, 1, 2, 3), y la probabilidad de que X tome cada uno de esos valores (0.125, 0.375, 0.375, 0.125):

Suponiendo que esta moneda es justa y que cada lanzamiento es independiente de los demás, podemos derivar la probabilidad de cada resultado.

<img width="619" alt="image" src="https://github.com/user-attachments/assets/166ddbca-13dc-4da0-bc53-18fdc4599bbd" />

A esto lo llamamos la *distribución de una variable aleatoria*. Si conocemos la distribución de una variable aleatoria, podemos responder casi cualquier pregunta potencial que tengamos sobre X, como:

1. Si lanzamos una moneda tres veces, cual es la probabilitdad de observar al menos dos caras?
2. Si lanzamos una moneda tres veces, que tan probable es que observemos exactamente una cara?
3. Si lanzamos una moneda tres veces, cual es la probabilidad de ver todas caras o toda cruces?

Con la distribución de la variable aleatoria, podemos calcular estas probabilidades y analizar el comportamiento de los resultados del experimento.

## Distribution of Random Variables IRL

Let's check out some real-world examples.

Suppose we record the number of free throws a basketball player shoots over a season and let Y represent the number of shots successfully made.

- If we were to analyze the data, what is the probability that a randomly selected player makes 80 percent or more of their attempted free throws?
- If we were to analyze the data, what proportion of players make less than 60 percent of their shots and at least seven of the first 10 they attempt?

Can you see how a coach could use this information to better understand how well their players perform throughout a season?

## Discrete vs. Continous Random Variables
Nearly all random variables fit into one of two categories: continuous and discrete.

- if you can list out all of the possible values of a random variable, we call that random variable discrete.
- if you cannot list out all of the possible values of a random variable, we call that random variable *continuous*.

<img width="424" alt="image" src="https://github.com/user-attachments/assets/71c21476-c06d-43c2-a76e-2a41d0d6a011" />

--
Variables Aleatorias Discretas vs. Continuas

Casi todas las variables aleatorias se clasifican en una de dos categorias: continuas y discretas.

- Si puedes enumerar todos los valores posibles de una variable aleatoria, decimos que esa variable aleatoria es discreta.
- Si no puedes enumerar todos los valores posibles de una variable aleatoria, decimos que esa variable aleatoria es continua.

<img width="424" alt="image" src="https://github.com/user-attachments/assets/71c21476-c06d-43c2-a76e-2a41d0d6a011" />

## Discrete Random Variables
Let's refer back to our earlier example of a random variable, X, where X is the number of heads resulting from a coin flip experiment.

In this case, X *is discrete* because you can list all values of X(0,1,2,3).

Now, let's also consider our earlier example of a random variable, Y, where Y is the number of free throws made by a player.

In this case, Y is discrete because you can list all values of Y (all of the possible shots made)/

In a nutshell, if you can list out all of its possible values - even if it's a very large number with thousands of integers - then your random variable is discrete.

--
Variables Aleatorias Discretas
Volvamos a nuestro ejemplo anterior de una variable aleatoria, X, donde X es el número de caras que resultan de un experimento de lanzamiento de monedas.

En este caso, X es discreta porque puedes enumerar todos los valores posibles de X (0, 1, 2, 3).

Ahora, consideremos también nuestro ejemplo anterior de una variable aleatoria, Y, donde Y es el número de tiros libres anotados por un jugador.

En este caso, Y es discreta porque puedes enumerar todos los valores posibles de Y (todos los tiros posibles que podrían anotarse).

En resumen, si puedes enumerar todos sus valores posibles, incluso si es un número muy grande con miles de enteros, entonces tu variable aleatoria es discreta.

## Continuous Random Variables
Let's say that there is a random variable, Z, where Z is the systolic blood pressure of an individual.

In this case, Z *is continuous* because you cannot list all possible values of Z.

For example, someone could have a systolic blood pressure of 120, or 120.1, or 120.01, or 120.001, and so on. You wouldn't be able to write out all possible values of their blood pressure.

--
Variables Aleatorias Continuas
Supongamos que existe una variable aleatoria, Z, donde Z es la presión arterial sistólica de un individuo.

En este caso, Z es continua porque no puedes enumerar todos los valores posibles de Z.

Por ejemplo, alguien podría tener una presión arterial sistólica de 120, o 120.1, o 120.01, o 120.001, y así sucesivamente. No serías capaz de enumerar todos los valores posibles de su presión arterial.

## More on Continuous Random Variables
Another example of a continuous random is one that represents the distance between two objects. Because distance could be any value between zero and infinity, this random variable would be considered *continuous*.

In the image below, as the x axis approaches 10, it appears that the y axis reaches zero. However, it will actually just become an increasingly smaller number on into infinity - 0.001, 0.0001, 0.00001, and so on.

<img width="583" alt="image" src="https://github.com/user-attachments/assets/f2531af2-4085-4c8a-93d5-686f9c231743" />

--
Más sobre Variables Aleatorias Continuas

Otro ejemplo de una variable aleatoria continua es aquella que representa la distancia entre dos objetos. Dado que la distancia puede ser cualquier valor entre cero e infinito, esta variable aleatoria se consideraría continua.

En la imagen a continuación, a medida que el eje x se acerca a 10, parece que el eje y llega a cero. Sin embargo, en realidad, el valor de y simplemente se convierte en un número cada vez más pequeño, acercándose a cero de manera infinita: 0.001, 0.0001, 0.00001, 0.000001, y así sucesivamente.

<img width="583" alt="image" src="https://github.com/user-attachments/assets/f2531af2-4085-4c8a-93d5-686f9c231743" />

## Knowledge Check
Which of the following is an example of a continuous value?

Select the best answer.

[ ] The number of home runs hit by Babe Ruth.
[x] The volume of water in all of the world's oceans.
Because volume is a measurement, this is indeed a continuous value. We can always increase the decimal place to which the volume is measured to improve its accuracy.
[ ] The number of employees in a company.
[ ] The number of grains of sand on Earth.

## Knowledge Check
Which of the following random variables are correctly labeled as "CONTINUOUS" or "DISCRETE"?

Select all that apply.

[x] The measurement of the angle made by the hour and minute hands on a clock. Label = CONTINOUS.
[x] The sum of the numbers rolled by a pair of dice. Label = DISCRETE.
[x] The number of times you flip a coin until the result is heads. Label = DISCRETE.
[ ] The length of a shadow cast by a willow tree. Label = DISCRETE.

“The length of a shadow cast by a willow tree.” This is a continuous variable, as we can always increase the decimal place to which the length is measured to improve its accuracy.

## Summaries of Distributions
We generally represent a distribution with a table or histogram. These tell us a lot about the behaviour of a random variable. For example:

<img width="633" alt="image" src="https://github.com/user-attachments/assets/b103be96-6b22-4d55-b130-a61f5725cdc3" />

However, you might be interested in finding ways to communicate information about this distribution without using these representations.

--
Resúmenes de Distribuciones

Generalmente representamos una distribución con una tabla o un histograma. Estos nos dicen mucho sobre el comportamiento de una variable aleatoria. Por ejemplo:

<img width="633" alt="image" src="https://github.com/user-attachments/assets/b103be96-6b22-4d55-b130-a61f5725cdc3" />

Sin embargo, podrías estar interesado en encontrar formas de comunicar información sobre esta distribución sin utilizar estas representaciones.

## Expected Value
There are many different distribution summaries that you'll get to know, but we'll be focusing on *expected value* - the average value of a random variable.

We calculate expected value a bit differently for continuous and discrete distributions.

--
Valor Esperado

Existen muchos resúmenes de distribuciones que llegarás a conocer, pero nos enfocaremos en el valor esperado, que es el valor promedio de una variable aleatoria.

Calculamos el valor esperado de manera un poco diferente para distribuciones continuas y discretas.

## Expected Value of Discrete Distributions
Take the random variable, X, where X is the number of heads observed when we flip a coin three times. We know from before that X can take on the values 0,1,2, and 3. The expected value of X - denoted E[X] - is 1.5.

It's not quite as easy as just averaging 0,1,2, and 3. In this case it happens to work, but typically it won't. Consider if X = 3 occurred 90 percent of the time. If so, do we think we'd want the expected value to be 1.5 or higher?

--
Valor Esperado de Distribuciones Discretas

Consideremos la variable aleatoria X, donde X es el número de caras observadas al lanzar una moneda tres veces. Sabemos que X puede tomar los valores 0, 1, 2 y 3. El valor esperado de 
X, denotado como E[X], es 1.5.

No es tan simple como promediar 0, 1, 2 y 3. En este caso, funciona, pero normalmente no será así. Imagina si 
X=3 ocurriera el 90% de las veces. En ese caso, ¿crees que el valor esperado debería ser 1.5 o más alto?

## Calculating The Expected Value of Discrete Distributions
The formula for calculating the expected value of some discrete random variable X is:

<img width="230" alt="image" src="https://github.com/user-attachments/assets/e69b376d-39f7-448a-ba94-c777afcc0ff3" />

In this case, X is the random variable itself and Xi are the different values of X. We take each value of X, multiply it by the probability of observing that particular value of X, and sum these products.

--
Cálculo del Valor Esperado de Distribuciones Discretas

La fórmula para calcular el valor esperado de una variable aleatoria discreta X es:

<img width="230" alt="image" src="https://github.com/user-attachments/assets/e69b376d-39f7-448a-ba94-c777afcc0ff3" />

En este caso, X es la variable aleatoria en sí misma y Xi son los diferentes valores de X. Tomamos cada valor de X, lo multiplicamos por la probabilidad de observar ese valor particular de X, y sumamos estos productos.

## Expected Value of Discrete Distributions (Cont.)

Lets use that formula for calculating the expected value of a discrte random variable, X:

<img width="241" alt="image" src="https://github.com/user-attachments/assets/821ef5c6-243e-4a0d-9353-1c1a534488eb" />

And our table of values of X and their associated probabilities:

<img width="633" alt="image" src="https://github.com/user-attachments/assets/203b48f7-4631-4096-94f2-39e9a971af50" />

Now, let's calculate the expected value of X here:

<img width="579" alt="image" src="https://github.com/user-attachments/assets/1e4305b1-e2e7-4d7e-bd32-d6797e84dca9" />

--
Valor Esperado de Distribuciones Discretas (Continuación)

Usemos esa fórmula para calcular el valor esperado de una variable aleatoria discreta, X:

<img width="241" alt="image" src="https://github.com/user-attachments/assets/821ef5c6-243e-4a0d-9353-1c1a534488eb" />

Y nuestra tabla de valores de XX y sus probabilidades asociadas:

<img width="633" alt="image" src="https://github.com/user-attachments/assets/203b48f7-4631-4096-94f2-39e9a971af50" />

Ahora, calculemos el valor esperado de X aquí:

<img width="579" alt="image" src="https://github.com/user-attachments/assets/1e4305b1-e2e7-4d7e-bd32-d6797e84dca9" />

## Finding The Expected Value of Continuous Distributions

To find the expected value of a continuous random variable, we'll need to integrate. In other words, we'll need to find the probabiity of each given point and solve for the cumulative sum of all those values.

Recall the formula for expected value applied o a discrete random variable:

<img width="231" alt="image" src="https://github.com/user-attachments/assets/81b28cd4-2ee5-4875-bf62-971dfbb9be17" />

In this case of a continuous random variable, we can't calculate xi . P(X = xi) for each i - there's an uncountably infinite number of is!

So, for a continuous random variable, X, the formula i's:

<img width="171" alt="image" src="https://github.com/user-attachments/assets/1aa54f41-8f3b-432e-a4db-f007c990d505" />

f(x) is the probability density function for the random variable X.

--
Encontrando el Valor Esperado de Distribuciones Continuas

Para encontrar el valor esperado de una variable aleatoria continua, necesitaremos integrar. En otras palabras, necesitaremos encontrar la probabilidad de cada punto dado y resolver la suma acumulativa de todos esos valores.

Recordemos la fórmula para el valor esperado aplicada a una variable aleatoria discreta:

<img width="231" alt="image" src="https://github.com/user-attachments/assets/81b28cd4-2ee5-4875-bf62-971dfbb9be17" />

En el caso de una variable aleatoria continua, no podemos calcular xi · P(X = xi) para cada i - hay un número infinito incontable de i's!

Por lo tanto, para una variable aleatoria continua, X, la fórmula es:

<img width="171" alt="image" src="https://github.com/user-attachments/assets/1aa54f41-8f3b-432e-a4db-f007c990d505" />

f(x) es la función de densidad de probabilidad para la variable aleatoria X.

