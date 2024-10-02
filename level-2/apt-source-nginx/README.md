# apt-source-nginx

В этом уроке установим nginx из официального репозитория разработчика.

### Полезное

- [официальный nginx инструкция](https://docs.nginx.com/nginx/admin-guide/installing-nginx/installing-nginx-open-source/#installing-a-prebuilt-debian-package-from-the-official-nginx-repository)

### Задание

1. Обновите (англ. "update") базу пакетов.
2. Установить (англ. "install") nginx из официального репозитория.

Подсказки:

1. Чтобы узнать `CODENAME`

```bash
cat /etc/os-release
```

---

### Ответ

```
sudo apt install curl gnupg2 ca-certificates lsb-release debian-archive-keyring

curl https://nginx.org/keys/nginx_signing.key | gpg --dearmor \
    | sudo tee /usr/share/keyrings/nginx-archive-keyring.gpg >/dev/null

gpg --dry-run --quiet --no-keyring --import --import-options import-show /usr/share/keyrings/nginx-archive-keyring.gpg

echo "deb [signed-by=/usr/share/keyrings/nginx-archive-keyring.gpg] \
http://nginx.org/packages/debian `lsb_release -cs` nginx" \
    | sudo tee /etc/apt/sources.list.d/nginx.list

echo -e "Package: *\nPin: origin nginx.org\nPin: release o=nginx\nPin-Priority: 900\n" \
    | sudo tee /etc/apt/preferences.d/99nginx

sudo apt update

sudo apt install nginx

sudo nginx
```