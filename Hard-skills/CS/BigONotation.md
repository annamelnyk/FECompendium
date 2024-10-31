https://www.rithmschool.com/courses/javascript-computer-science-fundamentals

# Big O Notation
  Way of comparing one algorithm to another is called **big O** notation.
  **big O** notation is used to classify algorithms according to how their run time or space requirements grow as the input size grows. (используется для классификации алгоритмов в соответствии с тем, как растут их требования к времени выполнения или пространству по мере увеличения размера входных данных.)
  ---------------------------------------------------->
  1. Constants are ignored
  2. Smaller components are ignored
  Keeping those rules in mind, the following are equivalent:

  O(500 * n) --> O(n)
  O(99999999999) --> O(1)
  O(10*n2 + 5n + 20) --> O(n2)
  O(n * n) --> O(n2)
  O(n*log(n) + 30000 * n) --> O(n * log(n))
  Notice that in all examples, constant values are replaced with 1, and all smaller components that are added are ignored.
  ---------------------------------------------------->
  * O(1) or constant time
    **1.** 
      `function add(num1, num2, num3) {`
        `return num1 + num2 + num3;`
      `}`
      В приведенном выше примере для добавления требуется две операции сложения. Размер чисел не влияет на то, сколько сложений необходимо выполнить, поэтому в этом случае время выполнения не зависит от размера входных данных.

    **2.** The function is also O(1) if it doesn't have any inputs (функция без аргументов)!
    
  * O(n) or linear time, because the data set is iterated over approximately one time (набор данных повторяется примерно один раз)
    **1.**
      `function sayHello(numberOfTimes) {`
        `for (var i = 0; i < numberOfTimes; i++) {`
            `console.log("Hello");`
        `}`
      `}` 
      This one takes an argument, which controls how many times Hello gets logged to the console.

    **2.**
      `function doubleThenTriple(numbers) {`
        `var doubled = numbers.map(function(num) {`
            `return num * 2;`
        `});`
        `return doubled.map(function(num) {`
            `return num * 3;`
        `});`
      `}`
      In the above example we map over the data set twice. So you could say the runtime is O(n + n) or O(2*n). However, in big O notation, constants are ignored. So, O(2*n) is equivalent to O(n). What matters is that the runtime scales in proportion to the input size, not the details of the proportional relationship.  
  
  * O(n2) - вложенные циклы
    Это полезное эмпирическое правило: в общем случае, если вы видите вложенные циклы, время выполнения будет O (n уровней вложенности). Другими словами, функция с одним циклом for будет O(n), функция с циклом внутри цикла будет O(n2), функция с циклом внутри цикла внутри цикла будет O (n3) и так далее.
  ---------------------------------------------------->
  **Across Time and Space**
    So far we've only been talking about the runtime of different algorithms using Big O Notation. This is often referred to as analyzing the time complexity of the algorithm.

    But Big O isn't just used to talk about the time it takes our programs to run; it's also used to talk about how much space (i.e. memory) our program requires. This is often referred to as analyzing the space complexity of the algorithm.

    Very often we're concerned primarily with auxiliary space complexity, that is, how much additional memory does the algorithm require beyond what needs to be allocated for the inputs themselves?
  ---------------------------------------------------->  
    