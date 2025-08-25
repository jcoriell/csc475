
## First Program

1. Create a file named `family.pl`

2. In that file, place the following code.

    ```Prolog
    % declaring facts
    % you can read the next line as "tom is the parent of bob"
    parent(tom, bob).  % these arguments begin with lowercase letters
    parent(pam, bob).
    parent(bob, sam).

    % declaring rules
    % You can read this rule as "X is the grandparent of Y if X is the parent of Z and Z is the parent of Y
    grandparent(X,Y) :- parent(X, Z), parent(Z, Y).  % Variables begin with capital letters
    ```

    Notice that `tom` and `bob` start with lowercase letters. All non-numeric constants start with a lowercase letter.

    Notice that `X` and `Y` start with capital letters. Variables always begin with an uppercase letter.

3. In your terminal, run `swipl` or `gprolog` depending on if you installed SWI Prolog or GNU Prolog. If successful, a prompt that looks like the following will appear:

    ```Prolog
    ?- 
    ```

4. Load in the `family.pl` file by typing the following:

    ```Prolog
    ?- [family].
    ```

5. Now you can ask it a question such as whether or not `tom` is a grandparent of `sam`.

    ```Prolog
    ?- grandparent(tom, sam).
    ```

6. If you want to ask **Who is a grandparent of `sam`?** you can use a variable in the prompt. Note that in the following prompt, X is capitalized.

    ```Prolog
    ?- grandparent(X, sam).
    X = tom
    ```

7. If you wanted to know if sam has more granparents, you can use a semicolon after each answer. It will respond with false once all of the options have been exhausted.

    ```Prolog
    ?- grandparent(X, sam).
    X = tom ;
    X = pam ;
    false.
    ```

7. If you wanted to ask, **To whom is `tom` the grandparent of?** you can use a variable as the second argument.

    ```Prolog
    ?- grandparent(tom, X).
    ```







