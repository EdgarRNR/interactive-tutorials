Обектите са инкапсулация на променливи и функции в една единица. Обектите получават своите променливи и функции от класове. Класовете са по същество шаблон за създаване на обекти.

Един много основен клас би изглеждал по следния начин:

Ще обясним защо трябва да включите "self" като параметър малко по-късно. Първо, за да асоциирате горния клас (шаблон) с обект, трябва да направите следното:

Сега променливата "myobjectx" съдържа обект от класа "MyClass", който съдържа променливата и функцията, дефинирани в класа, наречен "MyClass".

### Достъп до променливи на обекта

За да получите достъп до променливата вътре в новосъздадения обект "myobjectx", трябва да направите следното:

Например, по-долу ще изведе низът "blah":

Можете да създавате множество различни обекти, които са от същия клас (имат дефинирани същите променливи и функции). Въпреки това, всеки обект съдържа независими копия на променливите, дефинирани в класа. Например, ако дефинираме друг обект с класа "MyClass" и след това променим низа в променливата:

### Достъп до функции на обекта

За да получите достъп до функция вътре в обект, използвате нотация, подобна на достъпа до променлива:

Горният пример ще изпечата съобщението "This is a message inside the class."

### __init__()

Функцията `__init__()`, е специална функция, която се извиква, когато класът се инициира. Използва се за присвояване на стойности в класа.

Exercise
--------

Имаме клас, дефиниран за превозни средства. Създайте два нови превозни средства, наречени car1 и car2. Определете car1 като червен кабриолет на стойност $60,000.00 с име Fer, и car2 като син ван на име Jump на стойност $10,000.00.