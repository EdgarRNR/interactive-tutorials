Коли ви програмуєте, виникають помилки. Це просто факт життя. Можливо, користувач ввів некоректні дані. Можливо, мережевий ресурс був недоступний. Можливо, у програми закінчилася пам'ять. Або навіть програміст міг допустити помилку!

Рішенням для обробки помилок у Python є виключення. Ви могли вже стикатися з помилками-різноважами раніше.

    print(a)
    
    #помилка
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    NameError: name 'a' is not defined

Ой! Забули призначити значення змінній 'a'.

Але іноді ви не хочете, щоб виключення повністю зупиняли програму. Вам може знадобитися зробити щось особливе, коли виключення виникає. Це можна зробити в блоці *try/except*.

Ось простий приклад: Припустимо, ви перебираєте список. Вам потрібно перебрати 20 чисел, але список формується з введення користувача і може не містити 20 чисел. Після того, як ви дійдете до кінця списку, ви просто хочете, щоб решта чисел інтерпретувалися як 0. Ось як це можна зробити:

    def do_stuff_with_number(n):
        print(n)
    
    def catch_this():
        the_list = (1, 2, 3, 4, 5)
    
        for i in range(20):
            try:
                do_stuff_with_number(the_list[i])
            except IndexError: # Raised when accessing a non-existing index of a list
                do_stuff_with_number(0)
    
    catch_this()

Бачите, це було не так важко! Ви можете зробити це з будь-яким виключенням. Для отримання додаткової інформації про обробку виключень, зверніться до [документації Python](http://docs.python.org/tutorial/errors.html#handling-exceptions)

Exercise
--------

Обробіть усі виключення! Згадайте попередні уроки, щоб повернути прізвище актора.