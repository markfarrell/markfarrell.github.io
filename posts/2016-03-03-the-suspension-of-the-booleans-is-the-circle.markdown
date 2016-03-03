---
title: The Suspension of the Booleans Is the Circle
---

I would like to expand on the discussion that I started about homotopy type theory in my previous posts. In this post, I would like to discuss a proof that the suspension of the booleans is the circle, using the latest ideas for a formal system for doing homotopy theory synthetically.

Recall the definition of the booleans as an inductive data type. In code, this looks like:

```
data Boolean : Type where
  True  : Boolean
  False : Boolean
```

Meanwhile, the booleans, viewed as a logical space with points inside of it, pictorially looks like:

<img src="/images/boolean_space.png" width="30%"/>

Here, the booleans are identical to what would be called the *0-sphere* in the context of traditional homotopy theory.

As mentioned in a previous post, in the context of homotopy type theory, we seek to have a formal system that allows us to define what are known as higher inductive data types: these are logical spaces (data types) that can be defined not only by constructors for their points, but also paths between their points, paths between their paths, and so on and so forth. Higher inductive data types allow us to introduce ideas from traditional homotopy theory into our formal system for doing synthetic homotopy theory. In particular, we can define the analogue of the suspension of a space from traditional homotopy theory, as a higher inductive data type. As a higher inductive data type, the constructor for the suspension takes a type and produces a type, with point constructors for two logical poles, as well path constructors between the poles for each point constructor in the type that is parameterized by.

Pictorially, the suspension of the booleans looks like:

<img src="/images/one_sphere.png" width="45%"/>

However, in code, the suspension as a higher inductive data type looks like:

```
data Suspension : (A : Type) -> Type where
  North : Suspension A
  South : Suspension A
  Meridian : (a : A) -> Path (Suspension A) North South
```

For the purposes of illustration, we can define the suspension of the booleans explicitly as:

```
data S1 : Type where
  North : S1
  South : S1
  MeridianTrue : Path (Suspension A) North South
  MeridianFalse : Path (Suspension A) North South
```

However, more generally we can simply define the suspension of the booleans as:

```
type S1 = (Suspension Boolean)
```