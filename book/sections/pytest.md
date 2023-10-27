# Testing frameworks

Each time we make changes to a code, we would like to test it. This can be
tedious and that might prevent us from testing. We want to make testing as
easy as version control is. A testing framework can help us.

## py.test

The testing framework we will discuss today is a python library called
[`pytest`](https://pytest.org/en/7.1.x/) to automatically fetch all test files
in the repository and execute them.

> The `pytest` framework makes it easy to write small tests, yet scales to support
> complex functional testing for applications and libraries.

\- [pytest](https://pypi.org/project/pytest/)

In `pytest`, each test is a function whose name begins with the letters test.
We can group tests together in files whose names also begin with the letters test.
To execute our tests we run the command `pytest`.
This automatically searches the current directory and its subdirectories for
test files, and runs the tests they contain.

Consider the following method:

```python
def inc(x):
    return x + 1
```

See the `test_sample.py` example:

```python
# content of test_sample.py
def test_answer():
    assert inc(3) == 5
```

By simple executing `pytest`:

```bash
$ pytest
============================= test session starts =============================
collected 1 items

test_sample.py F

================================== FAILURES ===================================
_________________________________ test_answer _________________________________

    def test_answer():
>       assert inc(3) == 5
E       assert 4 == 5
E        +  where 4 = inc(3)

test_sample.py:5: AssertionError
========================== 1 failed in 0.04 seconds ===========================
```

Stepping back, the most important part of this lesson isn't the details of the
`pytest` library. It's that your time is more valuable than the computer's,
so you should spend it doing the things computers can't, like thinking of
interesting test cases and what your code is actually supposed to do.