# Консольная программа "Калькулятор"

## Задание 

По запросу с клавиатуры в консольном приложении вводится строка, которая может содержать: знаки операций +,-,*,/; константы (целые или вещественные) и скобки () для задания приоритета операций. Строка задает некоторое математическое выражение в инфиксной форме, программа осуществляет проверку введенного выражения, в случае ошибок ввода выдает сообщения об ошибках. Если ошибок нет программа вычисляет значение и выдает результат.

## Алгоритм работы программы

1.  Из консоли считывается формула.
2.  Используется алгоритм Дейкстры перевода из инфиксной формы в постфиксную форму.
	1. Если не достигнут конец входной последовательности (очереди), прочитывается 				очередная лексема.
    		1. Если прочитан операнд (число), он (оно) записывается в выходную
    			последовательность
    			(очередь).
       		2. Если прочитана открывающая скобка, она кладется в стек.
     	    	3. Если прочитана закрывающая скобка, выталкивается из стека в
    			выходную последовательность(очередь) все до открывающей скобки. Сами
    			скобки уничтожаются 
          	4. Если прочитан знак операции, вытолкиваются из стека в выходную
    			последовательность (очередь) все операции с большим либо равным
    			приоритетом, а прочитанная операция кладется в стек. 
       2. Если достигнут конец входной последовательности (очереди), выталкивается все из стека
          	в выходную последовательность (очередь).
3. Вычисляется значение выражения в постфиксной форме.
       1. Если не достигнут конец входной последовательности (очереди), прочитывается очередную
		лексема. 
       		1. Если прочитан операнд (число), он (оно) кладется в стек. 
          	2. Если прочитан знак операции, выталкиваются из стека два операнда (для
   			бинарной операции и один для унарной) и кладется в стек результат
   			применения прочитанной операции к этим операндам, взятым в обратном
   			порядке.
5. Вывод значения выражения

