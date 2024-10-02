# apt-gcc

В этом уроке разберем подкоманду `show`.

### Полезное

- `apt show`
- [apt для новичков](https://itsfoss.com/apt-get-linux-guide/)

### Задание

- Обновите (англ. "update") базу пакетов.
- Отправьте значение поля `Bugs` от информации по пакету `gcc`.

---

### Ответ

```
sudo apt-get update

sudo apt-cache show gcc | grep Bugs
```