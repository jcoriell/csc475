---
title: "First Program"
---


## Overview 

Prolog is composed of three types of clauses: facts, rules, and queries. In this file we look at how to declare facts and rules inside a Prolog file.

## Declaring Facts

Create a file named `family.pl`. 

We start by declaring facts in Prolog. To declare a fact, you simply define information about a single entity, or a relation between two entitites. 


To declare a fact about one entity, it simply looks like you are calling a function in most langauges. To point out a few details, constants all start with a lowercase letter (such as `jim` and `pam`) and we end each line with a period.

```Prolog
man(jim).       % jim is a man
woman(pam).     % pam is a woman
woman(cecelia). % cecelia is a woman
man(phillip).   % phillip is a 
```

To declare a relation between two entities, it looks like you are calling a function with two arguments. 

```Prolog
parent(jim, cecelia).   % jim is a parent of cecelia
parent(pam, cecelia).   % pam is a parent of cecelia
parent(jim, phillip).   % jim is a parent of phillip
parent(pam, phillip).   % pam is a parent of phillip
```

To declare a rule, we use the notation `conclusion :- condition`

```Prolog
mom(X,Y) :- parent(X, Y), woman(X).  % X is a mom of Y if X is a parent of Y and X is a woman
```

Notice that `X` and `Y` start with capital letters. Variables always begin with an uppercase letter.



## Full Program

Combining the various pieces of code from above, we arrive at our final program. The next file will discuss how to make queries on this program.

```Prolog
man(jim).       % jim is a man
woman(pam).     % pam is a woman
woman(cecelia). % cecelia is a woman
man(phillip).   % phillip is a 

parent(jim, cecelia).   % jim is a parent of cecelia
parent(pam, cecelia).   % pam is a parent of cecelia
parent(jim, phillip).   % jim is a parent of phillip
parent(pam, phillip).   % pam is a parent of phillip

% declaring rules
mom(X,Y) :- parent(X, Y), woman(X).  % X is a mom of Y if X is a parent of Y and X is a woman
```