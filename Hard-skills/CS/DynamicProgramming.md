# Dynamic Programming
  
  **Dynamic programming** is a useful problem solving technique that often helps to make your programs more efficient. The basic idea is that you solve smaller problems and remember the result of those smaller problems in case you encounter them again. By remember solutions to smaller problems, you can more quickly figure out the larger problem.
  
  **Идея динамического программирования** состоит в разбиении задачи на несколько независимых подзадач, решении каждой из них, а затем вычислении исходного результата. Для решения подзадач этот же алгоритм применяется рекурсивно.

  # Memoization vs. Tabulation
    To solve problems using dynamic programming, there are two approaches that we can use, **memoization** and **tabulation**.

    Идея «сохранения» результата дорогостоящей функции (fib, последовтельность Фиббоначи) известна как **мемоизация**. Мемоизация реализуется путем ведения таблицы поиска предыдущих решенных подзадач. Этот подход также известен как «сверху вниз», поскольку сначала вы решаете «верхнюю» проблему (которая обычно рекурсивно переходит к решению подзадач).

    Когда вы решаете задачу динамического программирования с помощью **табуляции**, вы решаете сначала все связанные с ней подзадачи. Это означает, что вы должны решить, в каком порядке решать ваши подзадачи в первую очередь, что добавляет еще один шаг, но дает вам больше гибкости, чем запоминание. Этот подход традиционно известен как подход «снизу вверх», поскольку сначала вычисляются подзадачи.

    https://stackoverflow.com/questions/6164629/what-is-the-difference-between-bottom-up-and-top-down
    https://www.rithmschool.com/courses/javascript-computer-science-fundamentals/dynamic-programming