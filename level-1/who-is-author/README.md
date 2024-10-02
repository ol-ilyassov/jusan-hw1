# who-is-author

### Полезное

- `ls`
- `awk`

### Задание

1. Написать команду, которая покажет все содержимое в текущей директории в формате `user filename`. Не показывать в выводе директории `.` и `..`.

Пример вывода:

```
root avatar.png
amurat solution.txt
jchris song.mp3
```

---

### Ответ

```
ls --ignore='.' --ignore='..' -la | awk 'NR > 1 { print $3, $9 }'
```