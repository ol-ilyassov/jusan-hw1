# ping

Чтобы убедиться, что вы можете связаться с системами, доступными в сети, используйте команду `ping`. Она отправляет специальные пакеты в удаленную систему, ожидая от них ответа, например:

```bash
$ ping google.com
PING google.com (209.85.233.113): 56 data bytes
64 bytes from 209.85.233.113: icmp_seq=0 ttl=101 time=87.974 ms
64 bytes from 209.85.233.113: icmp_seq=1 ttl=101 time=80.757 ms
64 bytes from 209.85.233.113: icmp_seq=2 ttl=104 time=102.039 ms
64 bytes from 209.85.233.113: icmp_seq=3 ttl=101 time=171.253 ms
64 bytes from 209.85.233.113: icmp_seq=4 ttl=101 time=135.148 ms
^C
--- google.com ping statistics ---
5 packets transmitted, 5 packets received, 0.0% packet loss
round-trip min/avg/max/stddev = 80.757/115.434/171.253/33.587 ms
```

Команда `ping` в примере непрерывно "пингует" `google.com`. После нескольких пингов нажмите сочетание клавиш `Ctrl+C`, чтобы завершить процесс, и в последних нескольких строках вывода будет показано, сколько запросов команде удалось выполнить.

### Задание

1. Проверьте командой `ping` домен `jusan.kz`.
2. Отправьте `Да`, если сервер пингуется. Отправить `Нет` в обратном случае.

---

### Ответ

```
ping jusan.kz

# Нет, 100% packet loss.
```