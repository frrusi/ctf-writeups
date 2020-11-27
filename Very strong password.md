Задание 2.2

# Задание 2.2
## Очень стойкий пароль
### Очки: 100

> Один из заказчиков нашей компании был атакован APT "Вялые Питоны". Мы разгребаем последствия атаки, твоя задача - проверить пароли на стойкость. Вот тебе один из них.
> \xa0\xb8\xb4\xb9\xbf\xda\xaa\xdd\xa9\xac\xb6\xa9\xa5\xb6\xdd\xad\xbe\xa8\xdc\xaa\xa9\xb6\xdd\xb7\xa9\xac\xb4\xa8\xd8\xa3\xa2\xba\xa2\xdb\xbc\xb9\xb7\xa0\xaa\xba\xa1\xa3\xb7\xb9\xa9\xd9\xa4\xaf\xab\xaf\xd3\xd3\xd3\xd3\xd3\xd3
---
Обращаемся за помощью к [CyberChef](https://gchq.github.io/CyberChef/).
В окно **input** вставляем данный пароль, после чего в поиске ищем **Magic**.
В окно **Recipe** переносим **Magic**, включаем **intensive mode**:
- [x] intensive mode

Листаем вниз и видим, что с настройками **From Hex**, **XOR** (**key**: **ee**), **From** **Base32** найден ответ на таск.

---
```
Флаг:
mshp{0ne_byt3_x0r_1s_cl4ss1c}