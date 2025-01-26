# Central Limit Theorem

## Learning Objectives

By the end of this lesson, you'll be able to:

- Explore the statistical implications of the central limit theorem.
- Identify how and why you would sample a population.

--
Objectivos de Aprendizaje

Al final de esta lección, serás capaz de:
- Explorar las implicaciones estadísticas del teorema del límite central.
- Identificar cómo y por qué se tomaría una muestra de una población.

## Symbols To Look Out For

During this lesson, you'll see some new and unusual mathematical symbols

Symbol Key

<img width="245" alt="image" src="https://github.com/user-attachments/assets/97b8adb3-bc13-416f-91fc-26a16954ece0" />

--
Símbolos a tener en cuenta

Durante esta lección, verás algunos símbolos matemáticos nuevos

Simbolos

Datos: X
Media de la muestra: x
Todas las medias posibles de las muestras: X'
Variable: n
Media de la primera muestra: x₁
Media de la segunda muestra: x₂
Media de la tercera muestra: x₃

## Inferential Statistics

Let's say you work for a polling company. You're interesting in understandig the landscape of voters for an upcoming election.

It's notexactly efficient to survey the preferences of the entire U.S. population, so you choose to collect data from a group of 100 people.

Does that data tell the whole story of all voters? No, not really. But you, being the savvy data scientist that you are, make an inference based on the data you do have.

Enter inferential statistics, where we focus on generalizing results from a sample to a larger population.

--
Estadística Inferencial

Imagina que trabajas para una empresa de encuestas. Estás interesado en comprender el panorama de los votantes para las próximas elecciones.

No es muy eficiente encuestar las preferencias de toda la población de los Estados Unidos, así que decides recolectar datos de un grupo de 100 personas.

Esos datos cuentan toda la historia de todos los votantes? No, no realmente. Pero tú, siendo el astuto científico de datos que eres, hace una inferencia basada en los datos que tienes.

Entra en juego la *estadística inferencial*, donde nos enfocamos en generalizar los resultados de una muestra a una población más grande.


## Populations

To star determining voter trends and preferences, you may want to get to know your target audience, such as all individuals who will vote in an upcoming election.

That group of people? That's your group of interest - your *population*.

<img width="629" alt="image" src="https://github.com/user-attachments/assets/d09a69c4-de8b-4052-9373-16c1ea3ff097" />

## Samples

Now, let's say you want to take a closer look at this population to see which individuals tend to respond to questions about their voting preferences.

That's your *sample* - a subset of the population.

<img width="632" alt="image" src="https://github.com/user-attachments/assets/83f0b72d-18aa-4079-ab5a-67279b31c789" />

Using the mean of this simple, or the *sample mean*, implies that you can use that smaller sample to draw conclusions about the larger population.

When we calculate a sample mean (x), we treat it as one observation from the distribution of all possible sample means (X').

## Normal Distribution

Lots of real-world phenomena follow a *normal distribution*: data near the mean occurring more frequently than data that is further from the mean.

If we know that X' followis a normal distribution, we can then rely on this when conducting inference on a sample mean.

Take a look at this figure reflecting *three normal distributions*. It highlights how norma l distributions typically appear - symmetrical around their mean, denser in the center, a less around the tails.

1. *Green (left) distribution*: Has a mean of -3 and a standard deviation of 0.5.
2. *Red (middle) distribution*: Has a mean of 0 and a standard deviation of 1.
3. *Black (right) distribution*: Has a mean of 2 and a standard deviation of 3.

<img width="617" alt="image" src="https://github.com/user-attachments/assets/ff9f3666-ed98-40ef-af20-f6317def0d87" />

## Sampling Distribution

Suppose we take a sample of n observations from a population and record the mean of this sample.

We then replace all observations, pull another sample of n observations from the same population, and record the mean of that sample.

Now, say we do this over and over again until we've recorded the mean of every possible sample of size n from the population. This is known as the sampling distribution of X'.

## Central Limit Theorem in Practice

Let's take a closer look at the central limit theorem and sampling distribution.

In the example below, we can see that as the sample size gets larger, the graph approaches a more normal distribution.

If n is larger than 30, then X' is sufficienlty close to normal. The larger the value of n, the better basis you'll have for decision-making.

## Visuaizing the Central Limit Theorem

Take a look at these four histograms and what they represent:

- *One die*: Distribution of the sample mean for all possible samples of size 1.
- *Two dice*: Distribution for samples of size 2.
- *Three dice*: Distribution for samples of size 3.
- *Four dice*: Distribution for samples of size 4.

Notice that, as n increases, the distribution becomes more normal.

<img width="635" alt="image" src="https://github.com/user-attachments/assets/beea548f-0ad4-4899-904a-c849240a3d01" />

## Exploring the Central Limit Theorem

Let's look at another example:

Suppose you roll a six-sided dice. You roll it once and get 5.

If you were to calculate the average of that roll, that average would be 5. We'd indicate this with x1 = 5, saying that the mean of our sample is 5.

You decide to roll again, and this time you get a 3.

The mean of this second sample (x2) is 3.

Let's do this again, but instead use sample size n = 2. In this case, we'll rool the dice twice and find the average:

Sample 1: {1,1} => x1 = 1
Sample 2: {1,2} => x1 = 1
Sample 3: {1,3} => x1 = 1
...
Sample 36: {6,6} => x36 = 6

## More on the Central Limit Theorem

What if we were to do this for every possible sample of size 1? That would mean rolling a 1, 2, 3, 4, 5, and 6 exactly once each.

We'd use the random variable (X') to represent all possible values of the sampling distribution (x'), along with how frequently we observer the sample mean of those values.

If we were to visualize this with a histogram, we get a flat chart in which values 1 through 6 are all equally likely.

<img width="617" alt="image" src="https://github.com/user-attachments/assets/0d51a364-a24d-4728-b338-f2d05519fab4" />

## Knowledge Check

Suppose you have the following variables:

- X = A random variable representing the blood pressure of everyone in one country.
- A sample size of 50 individuals.
- X' = The mean of this sample's blood pressure.

If we know that blood pressure (X) follows a normal distributions, then we know that the sampling distribution of X' follows a normal distribution as well.

If we don't know that blood pressure (X') follows a normal distribution, can we assume that the sampling distribution, can we assume that the sampling distribution of X' is approximately normally distributed?

[x] Yes
Correct: Yes, we can! If we don't know that blood pressure (X) follows a normal distribution, we can assume that the sampling distribution of X' is approximately normally distributed, because our sample size is greater than 30. We can apply the central limit theorem there.

[ ] No

## Experimental Design

What would you do to ensure that your means of data collection, or your experiment, has been handled in the right manner?

*Experimental design* is concerned with validity, reliability, and replicabiity. It ensures that:

1. The question the experiment is trying to answer is clearly defined.
2. Sources of variability in the experiment are identified.
3. Descriptions exist of how participants were allocated - i.e., if they were randomly chosen or other methods were used.

## Experimental Desing IRL (In Real Life)

In data science, *sample protocol* is an important part of dealig with survey data (or experiments). Statistical significance should always be used when making decisions based on data, but it's also important to consider the types of questions bieng asked and who is answering them.

For example, customers with bad experiences may be more likely to wite reviews on a website than those with good experiences. Therefore, this does not necessarily mean that users are having more negative experiences than positive ones! Instead, it suggests that the results are biased toward dissatisfied customers.

If you know your data set contains biased answers, it's up to you to decide how to deal with the data so that you can still get meaningful results.

## Knowledge Check

We want to estimate the average age among our coworkers. We sample 25 individuals and ask the their age. We don't know if the population of age would follow a normal distribution.

Which of the following statements is true?

Select the best answer.

[x] We cannot rely on a normal distribution. Our sample size is fewer than 30 and we don't know that our original data follows a normal distribution.

Correct: Because the population is fewer than 30, we cannot assume that our sample data will follow a normal distribution.

[ ] We should have a large enough sample size to apply the central limit theorem.

## Knowledge Check

If we visualize the distribution of rolling a dice six times and getting 1, 2, 3, 4, 5,and 6 exactly once, the histogram would be...

Select the best answer.

[ ] Normally distributed.
[ ] Round on the sides but flat on top.
[x] Flat.
Correct: If we were to roll a dice six times and get each number exactly once, the histogram will be flat. As we increase the number of rolls, the shape of the distribution will become more normal and eventually reach the central limit theorem.
[ ] Skewed to the right.

## Knowledge Check

We want to test if 66 inches is a reasonable guess for the average height of employees at our company. We know that the employees' heights follow a normal distribution and we sample 15 people for the test.

Which of the following statements is *true*?

Select the best answer.

[x] We do not need to apply the central limit theorem.

We do not need to apply the central limit theorem because our original data is normally distributed, and the sampling distribution will be approximately normally distributed, regardless of sample size.

[ ] We need to apply the cental limit theorem.

