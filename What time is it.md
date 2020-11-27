Задание 4.2

# Задание 4.2
## Не подскажете, сколько время?
### Очки: 300

> Вам пришло это сообщение, когда вы уже собирались закрыть архив. После, на ваших часах возник странный адрес...
> 84.201.172.73:7001
---
Нам дан IPv4, попробуем обратиться к нему через клиент:
```python
import socket

domain = ('84.201.172.73', 7001)

s = socket.socket()
s.connect(domain)

s.send("hi".encode())

data = s.recv(1024).decode()

print(data)
```

Ответ от сервера: 
> What time is it?

Таск CTF. Спрашивают: "Сколько времени?". Было принято решение отправить в виде ответа строчку `ctftime`.
Получаем код клиента:
```python
import socket

domain = ('84.201.172.73', 7001)

s = socket.socket()
s.connect(domain)

s.send("ctftime".encode())
data = s.recv(1024).decode()
print(data)
```

Ответ от сервера: 
> What time is it?

Результата не дало, пробуем принять еще какое-либо сообщение от сервера.
Получаем код клиента:
```python
import socket

domain = ('84.201.172.73', 7001)

s = socket.socket()
s.connect(domain)

s.send("ctftime".encode())
data = s.recv(1024).decode()
print(data)
data = s.recv(1024).decode()
print(data)
```

Ответ от сервера: 
> What time is it?
> mshp{y34p_1ts_ctf_t1me!!!}

---
```
Флаг:
mshp{y34p_1ts_ctf_t1me!!!}