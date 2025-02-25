# Мікросервісна архітектура (Мікросервіси)

Перед тим як зрозуміти, що таке мікросервіси, варто розібратися з монолітною архітектурою.

### Що таке моноліт (монолітна архітектура)?

> Монолітна архітектура – це підхід, у якому весь додаток об'єднаний в одну кодову базу. Будь-яка зміна потребує оновлення всього додатка, його компіляції та перерозгортання на сервері.

Моноліти зазвичай простіші у створенні та розгортанні на ранніх етапах, але їхня складність зростає з часом.

### Переваги моноліту

- `Простота початкової розробки` - одна кодова база, один процес розгортання.
- `Менші витрати на інфраструктуру` - не потрібно налаштовувати складну систему комунікації між компонентами.
- `Просте розгортання` - один виконуваний файл або каталог спрощує розгортання.
- `Легке налагодження` - коли весь код знаходиться в одному місці, легше відслідковувати запит і знаходити проблему.

### Недоліки моноліту

- `Низька надійність` - помилка в одному модулі може вплинути на весь додаток.
- `Складність розгортання` - невелика зміна в монолітному додатку вимагає перерозгортання всього додатку.
- `Повільніша швидкість розробки` - великий монолітний додаток робить розробку складнішою і повільнішою.
- `Тісні зв'язки` - залежність між компонентами ускладнює їхню модернізацію.
- `Відповідальність` - розробнику потрібно розуміти не лише свій компонент, але й взаємодію з іншими частинами програми.
- `Труднощі в масштабованість` - якщо один модуль перевантажений, це впливає на весь додаток.

### Що таке мікросервіси?

> Мікросервіси - це архітектурний підхід, де додаток складається з незалежних сервісів із власною бізнес логікою та базою даних. Кожен сервіс оновлюється, тестується, розгортається та масштабується окремо. Вони розділяють основні бізнес-проблеми, специфічні для домену, на окремі, незалежні бази коду.

### Переваги мікросервісів

- `Гнучкість технологій` - кожен мікросервіс можна створювати з використанням технологій, які найкраще підходять для його завдань.
- `Ізоляція` - оскільки мікросервіси є автономними, вони дозволяють швидко і легко розгортати окремі функції незалежно один від одного.
- `Масштабованість` - при підвищеному навантаженні можна швидко додати нові екземпляри конкретного сервісу для балансування трафіку.
- `Надійність` - оновлення одного сервісу не впливають на роботу всього додатка, знижуючи ризик збоїв.
- `Розподіл відповідальності` - кожна команда відповідає лише за свій мікросервіс, що підвищує ефективність роботи.

### Недоліки мікросервісів

- `Складність впровадження` - на ранніх етапах розробки мікросервісна архітектура може бути складною для налаштування через необхідність продуманої організації сервісів, їх взаємодії та інфраструктури.
- `Комунікація між сервісами` - налаштування взаємодії між мікросервісами (через API, черги повідомлень та ін.) додає технічної складності та ризику затримок передачі даних.
- `Витрати на інфраструктуру` - кожен сервіс вимагає окремих ресурсів, що збільшує витрати на розробку, тестування та підтримку системи.
- `Складність управління даними` - кожен сервіс може мати свою базу даних, що ускладнує підтримання консистентності даних і виконання транзакцій, які зачіпають кілька сервісів.
- `Відлагодження` - відстеження помилок стає складнішим через розподілені системи. Локалізація проблеми часто потребує аналізу логів з кількох сервісів одночасно.
