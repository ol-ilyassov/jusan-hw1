# project-structure

### Задание

1. В корневой директории `/home/box` создайте папку `project` в корневой директории. В ней создайте такую структуру файлов и папок как показано ниже:

```
.
├── README.md
├── usecase
│   └── registration
│       ├── registration.go
│       └── registration_test.go
└── pkg
    └── util
        ├── helper.go
        ├── util_test.go
        └── util.go

```

---

### Ответ

```
mkdir -p ~/project && cd ~/project

mkdir -p usecase/registration pkg/util
touch usecase/registration/registration.go 
touch usecase/registration/registration_test.go
touch pkg/util/helper.go
touch pkg/util/util_test.go
touch pkg/util/util.go
```