# apt-delete-nginx

В этом уроке полностью удалим nginx из сервера.

На сервере заранее установлен nginx.

Полезные ссылки:

- [apt для новичков](https://itsfoss.com/apt-get-linux-guide/)

### Задание

1. Удалить (англ. "delete") полностью nginx вместе с конфигурационными файлами.

---

### Ответ

```
sudo apt purge nginx nginx-common

sudo apt autoremove
```
