# missing-line

### Задание

1. В корневой директории `/home/box` создать папку `sandbox` и в ней создать файл `jusan`.
2. В файл `jusan` записать слово `singularity` без новой линии в конце.

Пример для проверки:

```bash
box@dec74273716e: ~ $ cat jusan | wc -l
     0
```

---

### Ответ

```
mkdir -p ~/sandbox && cd ~/sandbox 

touch jusan && echo -n "singularity" > ./jusan
```
