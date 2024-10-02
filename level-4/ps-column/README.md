# ps-column

### Задание

1. Перечислите все запущенные процессы в отсортированном по использовании CPU порядке по убыванию и отобразите столбцы (см. "user-defined format"):
   - идентификатор процесса
   - имя пользователя
   - имя группы
   - размер виртуальной памяти
   - утилизация CPU
   - команда
2. Получившуюся команду записать в `/home/box/ps-column.sh`.

---

### Ответ

```
cd ~ && touch ps-column.sh
nano ps-column.sh
```
```
#!/bin/sh

ps -eo pid,user,group,vsize,pcpu,cmd --sort=-pcpu
```
```
chmod +x ps-column.sh
```