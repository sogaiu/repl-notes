# Questions

The following are some questions that might be nice to get answers to.

* Does there exist any useful language-agnostic documentation for
  nREPL somewhere?

* Suppose a file with two definitions in it is evaluated.  Let's refer
  to the definitions as `x` and `z`.

    ```clojure
    (def x 1)

    (def z 3)
    ```

  Suppose a third definition (call it `y`) is added between the two
  definitions and only it is evaluated.

    ```clojure
    (def x 1)

    (def y 2)

    (def z 3)
    ```

  If an error occurs that involves `z` (so the "lowermost" one), will
  the error information that involves `z` have appropriate location
  info?

  For the location information to be correct, when `y` was evaluated,
  it seems like `z`'s location information would have had to have been
  updated (because it was shifted down) or there would have to be some
  other mechanism to account for "things having shifted around".

  Does nREPL / Clojure somehow arrange for these kinds of adjustments?

