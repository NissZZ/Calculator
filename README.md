# Консольная программа "Калькулятор"

## Задание 

По запросу с клавиатуры в консольном приложении вводится строка, которая может содержать: знаки операций +,-,*,/; константы (целые или вещественные) и скобки () для задания приоритета операций. Строка задает некоторое математическое выражение в инфиксной форме, программа осуществляет проверку введенного выражения, в случае ошибок ввода выдает сообщения об ошибках. Если ошибок нет программа вычисляет значение и выдает результат.

## Алгоритм работы программы

1.  Из консоли считывается формула.
2.  Используется алгоритм Дейкстры перевода из инфиксной формы в постфиксную форму.
	1. Если не достигнут конец входной последовательности (очереди), прочитать очередную лексему. 
		- Если прочитан операнд (число), записать его в выходную последовательность (очередь). 
		- Если прочитана открывающая скобка, положить ее в стек. 
		- Если прочитана закрывающая скобка, вытолкнуть из стека в выходную последовательность (очередь) все до открывающей скобки. Сами скобки уничтожаются. 
		- Если прочитан знак операции, вытолкнуть из стека в выходную последовательность (очередь) все операции с большим либо равным приоритетом, а прочитанную операцию положить в стек. 
	2. Если достигнут конец входной последовательности (очереди), вытолкнуть все из стека в выходную последовательность (очередь) и завершить работу.

3. Вычисляется значение выражения в постфиксной форме.
       1. Если не достигнут конец входной последовательности (очереди), прочитывается очередную
		лексема. 
       		- Если прочитан операнд (число), он (оно) кладется в стек. 
          	 - Если прочитан знак операции, выталкиваются из стека два операнда (для
   			бинарной операции и один для унарной) и кладется в стек результат
   			применения прочитанной операции к этим операндам, взятым в обратном
   			порядке.
5. Вывод значения выражения

