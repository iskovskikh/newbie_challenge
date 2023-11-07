# Тестовые вопросы

## Python

- Какие типы данных есть в Python? 

- Что такое PEP? Расскажите про PEP8.

- Контекстный менеджер - что это? 

- Есть ли в Python множественное наследование? Что такое MRO? 

- Что такое магические методы?

- В чем отличие `is` от `==`?

- Что делает `(i+1 for i in range(5))`? В чем отличие от `[i+1 for i in range(5)]`?


## Django + DRF

- Что такое модель в Django?

- Что такое миграции?

- Что такое сериализатор?

- Как в Django реализовать ManyToOne отношения? 

- Какие View есть в DRF? (ApiView, GenericApiView, ViewSet, GenericViewSet, ModelViewSet)

- Аутентификация - какие бывают подходы. (Пароль, Одноразовый пароль, токен, сертификат, биометрия)

- Где лучше всего хранить бизнес-логику в Django?



## Сети

- Какие бывают методы HTTP запросов?

- Что такое GET и POST параметры. Чем отличаются, какие ограничения?

- Что такое SOAP, REST, GraphQL?

- Сетевая модель OSI.

- IP адресация. Что такое маска подсети. Зачем нужны адреса `127.0.0.1` и `0.0.0.0`, в чем разница?

- Опишите что происходит когда мы вводим адрес в url-строке браузера.


## Общее

- Кратко расскажите про MVC.

- Что такое Docker? В чем преимущества его использования?

- Что такое DRY, KISS, SOLID, GRASP?


## Тестовые задания:

- Как поменять местами 2 переменных без использования третьей?

  <details>
  <summary>Решение:</summary>

  ```
  a = 4
  b = 5
  a = a + b
  b = a - b
  a = a - b
  ```

  </details>

- Напишите функцию, которая выводит разницу между двумя листами.

  <details>
  <summary>Решение:</summary>
	
  ```
  array_diff([1,2], [1]) == [2]
  array_diff([1,2,2], [1]) == [2,2]
  array_diff([1,2,2], [2]) == [1]
  array_diff([1,2,2], []) == [1,2,2]
  array_diff([], [1,2]) == []
  array_diff([1,2,3], [1, 2]) == [3]
  ```

  </details>

- Напишите функцию, которая преобразует строку по следующему паттерну:

  ```
  accum("abcd") == "A-Bb-Ccc-Dddd"
  accum("bUjPi") == "B-Uu-Jjj-Pppp-Iiiii"
  accum("whTosD") == "W-Hh-Ttt-Oooo-Sssss-Dddddd"
  ```

  \* На вход функции может быть передана строка содержащая символы только из набора `[a-zA-Z]`.
  
  <details>
  <summary>Решение:</summary>

  ```
  def accum(s):    
      return '-'.join([(item * (index+1)).capitalize() for index, item in enumerate(list(s))])
  ```
  </details>
  
- Напишите функцию-генератор паролей.

  <details>
  <summary>Решение:</summary>

  ```
  import string
  import random
  
  def pw_gen(size = 8, chars=string.ascii_letters + string.digits + string.punctuation):
      return ''.join(random.choice(chars) for _ in range(size))
  ```
  </details

- Вы разрабатываете бекенд-часть для интернет-магазина. Какие API методы Вы создали бы для каталога, товаров и корзины?

- Вы разрабатываете бекенд-часть для приложения, которое регистрирует заявки. На фронте должен отображаться номер, который будет присвоен заявке, и форма, куда пользователь вводит данные заказа. Как вы организуете обмен данными?
