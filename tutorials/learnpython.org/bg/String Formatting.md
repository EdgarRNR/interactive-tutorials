Python използва форматиране на низове в C-стил, за да създаде нови, форматирани низове. Операторът "%" се използва за форматиране на набор от променливи, затворени в "кортеж" (списък с фиксиран размер), заедно с форматен низ, който съдържа обикновен текст заедно със "спецификатори на аргументи", специални символи като "%s" и "%d".

Да кажем, че имате променлива, наречена "name" с вашето потребителско име в нея, и искате да принтирате поздрав към този потребител.

    # Това отпечатва "Hello, John!"
    name = "John"
    print("Hello, %s!" % name)

За да използвате два или повече спецификатора на аргументи, използвайте кортеж (скоби):

    # Това отпечатва "John is 23 years old."
    name = "John"
    age = 23
    print("%s is %d years old." % (name, age))

Всеки обект, който не е низ, може също да бъде форматиран с оператора %s. Низът, който се връща от метода "repr" на този обект, се форматира като низ. Например:

    # Това отпечатва: A list: [1, 2, 3]
    mylist = [1,2,3]
    print("A list: %s" % mylist)

Ето някои основни спецификатори на аргументи, които трябва да знаете:


`%s - Низ (или всеки обект със стрингова репрезентация, като числа)`

`%d - Цели числа`

`%f - Числа с плаваща запетая`

`%.<брой цифри>f - Числа с плаваща запетая с фиксиран брой цифри вдясно от точката.`

`%x/%X - Цели числа в шестнадесетична репрезентация (малки/големи букви)`


Упражнение
--------

Ще трябва да напишете низ за форматиране, който отпечатва данните, използвайки следния синтаксис:
    `Hello John Doe. Your current balance is $53.44.`