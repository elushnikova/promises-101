# Промисы

Маленькое упражнение на базовое использование промисов.

## Подготовка

Установи все пакеты.

Проверь `package.json` и ответь себе на эти вопросы:

1. Как называется главный файл проекта?
2. Как запускать приложение?

Запусти приложение и открой главный файл — в нём ты будешь писать код. Познакомься с подключённым к нему модулем `Quote`.

## 1. Одна случайная цитата

Получи случайную цитату, используя модуль `Quote`.

Запиши автора этой цитаты и её текст в файл `quotes/random.txt`.

Например:

```plain
Good judgment comes from experience, and experience comes from bad judgment.

-- Rita Mae Brown
```

Для этого тебе пригодится модуль [`fsPromises`](https://nodejs.org/docs/latest-v18.x/api/fs.html#fspromiseswritefilefile-data-options). Позаботься, чтобы твоя цепочка промисов была прямой, а не "съезжала" по горизонтали в ад callback-функций.

Обработай ошибку при получении цитаты или записи в файл — пока для этого достаточно вывести сообщение об ошибке в консоль.

Сделай не менее 1 коммита для этого функционала.

## 2. Несколько случайных цитат

Сгенерируй `N` случайных цитат. Получи от пользователя желаемое количество — от 1 до 10 (не меньше и не больше) — это можно сделать через `process.argv`.

Создай `N` промисов на получение цитат. Когда они все выполнятся, запиши результаты в файл `quotes/random-N.txt` — вместо `N` в названии должно быть соответствующее число.

Например, `quotes/random-2.txt`:

```plain
The more people you help become successful the more successful you become.

-- Steve Harvey


Those who can make you believe absurdities can make you commit atrocities.

-- Voltaire
```

Убедись, что записываешь в файл только один раз. Для этого может пригодиться [`Promise.all()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/all).

Обработай ошибку при получении цитат или записи в файл — пока для этого достаточно вывести сообщение об ошибке в консоль.

Сделай не менее 1 коммита для этого функционала.

## 3. Тематическая цитата (бонус)

Получи 50 цитат по заданной теме, используя модуль `Quote`.

Создай 50 промисов для записи одной цитаты в файл `quotes/THEME.txt` — вместо `THEME` в названии должна быть соответствующая тема.

Каждый из этих промисов должен вывести в консоль сообщение со своей цитатой после того, как прошла запись в файл.

Например, содержимое файла `quotes/choice.txt`:

```plain
Quality is not an act, it is a habit.

-- Aristotle
```

Вывод в консоль:

```bash
"Quality is not an act, it is a habit."
```

Устрой гонку между этими промисами — нужно, чтобы выполнился лишь один. Для этого может пригодиться [`Promise.race()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/race).

Обработай ошибку при получении цитат или записи в файл — пока для этого достаточно вывести сообщение об ошибке в консоль.

Сделай не менее 1 коммита для этого функционала.

## Всё готово?

- Позволь пользователю выбирать тему из уже существующих.
- Поймай и обработай всевозможные ошибки через `catch`. Собери их все! :D
