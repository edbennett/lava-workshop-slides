## Objectives

- Learners should be able to engage with code exercises
  without significant overhead/extra cognitive load
- Learners should see examples of good practice
  to pattern their own software development practice on
- Learners should not be encouraged to develop bad habits
- Ultimately,
  learners should be able to read and understand production code,
  add their own contributions to it,
  and write their own analyses from scratch.

-

## Simplicity is in the eye of the beholder

- We would like to write "simple" code that removes
  "unnessary" distractions
- But no two people will agree on what "simple" means
  - Reduce number of function definitions?
  - Reduce number of calls to external libraries?
  - Reduce number of lines of code? (Code golf)
- Can we instead agree on a set of guidelines
  to give consistent, readable code?
  - Probably not,
    but we should still try!

---

## Languages

- How many languages do we expect learners to know already?
  - Python is standard in many (most?) curricula now
  - Julia? <!-- .element: class="fragment fade-in" data-fragment-index="2" -->
  - Matlab? <!-- .element: class="fragment fade-in" data-fragment-index="2" -->
  - Fortran? <!-- .element: class="fragment fade-in" data-fragment-index="2" -->
  - C/C++? <!-- .element: class="fragment fade-in" data-fragment-index="2" -->
  - Mathematica?? <!-- .element: class="fragment fade-in" data-fragment-index="3" -->

-

## Functions are friends

- Humans working memory can hold a limited number of items
- So we can only understand a handful of lines of code
  - Especially when reading for the first time
- $\Rightarrow$ break code down into short (<20 lines),
  well-named functions

-

## External Libraries

- Some external libraries are essential for idiomatic/fluent code
  - e.g. Numpy, Matplotlib in Python
- Others can be introduced if they significantly simplify code
  - e.g. `gvar`, `pyerrors`
  - Only if the simplification doesn't obviate the exercise!

-

## Internal libraries

- A flat file might be "simple"
- But splitting off utility functions allows learners to concentrate on the aspects being studied
  - e.g. "read a bunch of correlators from disk",
    "do an effective mass plot with plateau highlighted"
- Students can/will still read the implementations
  - But function names should mean they don't _need_ to

-

## Naming things

- One of the top two problems in computing
  (along with cache invalidation and off-by-one errors)
- Don't be afraid of long names
  - Completion tools help here
- Where names align with notes,
  this should be explicitly stated in comments
  - Especially where there are one-letter names
    (what is $U$, $a$, $F$, $x$ _in the specific context_?)

-

## Comments/Documentation

- "The best code is self-documenting"
  - This doesn't mean documentation isn't needed!
- Assume that the reader knows the language
  - Don't have a comment for every line rephrasing its contents
- Where you diverge from how you would implement in production,
  add a comment
  - E.g. `# Bootstrap samples would be imported/saved here`
- Use language features for documentation
  - E.g. [docstrings](https://docs.python.org/3/glossary.html#term-docstring)
  in Python will show up when you type `help(function_name)`

---

## "Write one function"?

- One possible exercise format:
  - Provide an empty function
  - Provide a harness that calls the function
  - Ask the student to write the body
- Allows learner to focus specifically on point being taught
- Harness could verify solution gives correct answer

-

## Write one function example

```python
def eff_mass(correlator: npt.NDArray) -> npt.NDArray:
    """
    Compute the effective mass of a given correlator.

    Args:
        correlator: A 2D Numpy array containing a single correlation function.
            Axis 0 indexes the time dimension;
            Axis 1 indexes different measurements of this correlation function.

    Returns:
        A 2D Numpy array containing the effective mass.
            Axis 0 indexes the time dimension;
            Axis 1 indexes different measurements of this effective mass.
    """
    
    pass
```

- The harness would handle reading data
  and plotting the effective mass
  (with appropriate axis labels, etc).
- It could also plot at shadow effective mass plot for comparison

---

## Other considerations

- Linters and autoformatters are friends
- Distribute a tarball, or use GitHub/Zenodo?
- Include automated tests?
