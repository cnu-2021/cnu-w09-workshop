# Week 9 workshop: Using `assert` statements for checking and testing

When writing code, a good principle to follow is to ensure that it **fails fast**. For instance, errors or invalid inputs should be detected early to ensure that no unnecessary computations are performed, which would lead to an error or invalid results.

This week you will work in small groups.

## Task 1: the `assert` statement

The `assert` statement allows you to "assert" that a condition is `True`. The statement

```python
assert condition, error_message
```

produces either:
- nothing, if `condition` is `True`,
- an `AssertionError` with error message given by the string `error_message`, if `condition` is `False`.

The code in `assert_tests.py` contains a few examples of `assert` statements.
- Run the code; nothing should happen.
- Change the value of `a`, `b`, or `c` to trigger the different errors.

## Task 2: checking function input arguments

Before proceeding to the body of a function, it's good practice to check that every input argument is valid. Using `assert` statements is a way to do this.

The function `bisection()` is copied here from the Week 8 tutorial solutions. At the start of the function, check that the input arguments `F`, `a`, `b`, `tol` have been supplied with the correct **type** and **value**. Before getting to coding, you should first figure out a list of everything you will need to check, and the order in which to check them.

Test `bisection()` with invalid inputs to check that the correct error message is displayed every time. Test it with valid inputs to make sure that no errors are triggered.

*Hint:*
- [this thread](https://stackoverflow.com/questions/624926/how-do-i-detect-whether-a-python-variable-is-a-function) discusses possible ways to check whether an object is a Python function.
- you may also find the modules `inspect` ([documentation](https://docs.python.org/3/library/inspect.html#module-inspect)) and `numbers` ([documentation](https://docs.python.org/3/library/numbers.html#numbers.Number)) useful.

## Task 3

If you have finished Tasks 1 and 2, bring up your solutions for CR3 (or one of the previous code review tasks), and use `assert` statements to check the validity of all input arguments at the start of `oscillator()`.

If there are any tests which can be performed by checking whether a condition is `True` or `False`, rewrite these using `assert` statements. Don't forget to write a useful error message for each test -- you can use f-strings, for instance.
