# The 20-Second Turtle Logo Contest

Write a Python turtle program that draws a picture in 20 seconds or less.

The theme of the picture is: A logo for an introduction to programming course.

## Prizes

1st place: $30
2nd place: $20
3rd place: $10


## Rules

1. Submissions must be from individuals. If you work with a partner, you should
   submit different programs. 

2. Your program should have this structure:

    ```python
    #
    # logo_contest.py
    #

    #
    #  Author: <your name>
    #    Date: <day, month, year> of submission
    #  School: <your school>
    # Teacher: <your teacher>
    #

    #
    # These are the only allowed imports!
    #
    import turtle
    import math
    import random
    import time

    start_time = time.time()

    #
    # ... your program goes here...
    #

    end_time = time.time()
    elapsed_time = end_time - start_time
    print(f'Time taken: {elapsed_time:.1f} seconds')
    ```

3. Once started, your program must finish without any user intervention.

4. The output should all be to the turtle graphics window. You can use print
   statements for debugging. Do not read/write any files.

5. Source code style counts! See the judging criteria below.

6. If you get any help from the internet, other people, or tools like ChatGPT,
   cite that assistance in a comment at the top of your program.

Programs that do not follow these rules may be disqualified!


## Judging

- How detailed, pleasing, and original is the final image?
- How well does the final image meet the requirements of the contest?
- Does it use a variety of features of Python turtle graphics?
- Is it fun to watch it draw?
- Is it done in 20 seconds or less? Time will be measured using a computer
  that is modern and efficient, but it might run slower than yours. So an
  extra 2 seconds grace period will be given to all programs. 
- Is the source code easy to read?


## Submitting

When it's ready, submit your program in a file named `logo_contest.py` to your
teacher no later than 5pm Friday October 4.

## Hints

You can add "from ... import ..." to the imports if you like, e.g. you could write:

```python
from turtle import forward, left, right, penup, pendown
```

The Python turtle documentation is at
https://docs.python.org/3/library/turtle.html


Since drawing time is limited, here's a trick for drawing faster:

```python
turtle.tracer(0, 0)   # turn off drawing

# ... turtle code ...

turtle.update()       # draw it all at once
```

Using this trick, you can draw much faster because you are combining multiple
turtle commands into a single `turtle.update()` call.

While you could wrap your entire program in `turtle.tracer(0, 0)` and
`turtle.update()`, you should use it selectively so that the user can see some
of the drawing process. Part of the judging criteria is how much fun it is to
watch the drawing process.
