You can't directly have randomized default arguments in Python, because default arguments are evaluated once, when the function is defined, not every time the function is called.

But you can build a workaround by using `None` as a placeholder, and generate random values inside the function.
  ```python
  import random

  def my_function(x=None):
      if x is None:
          x = random.randint(1, 10)
      print(x)

  my_function()   # Random number between 1 and 10
  my_function(5)  # 5
  ``` 
