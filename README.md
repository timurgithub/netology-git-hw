# Домашнее задание к занятию "`Git`" - `Akayev Timur`

### Инструкция по выполнению домашнего задания

   1. Сделайте `fork` данного репозитория к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/git-hw или  https://github.com/имя-вашего-репозитория/7-1-ansible-hw).
   2. Выполните клонирование данного репозитория к себе на ПК с помощью команды `git clone`.
   3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
      - впишите вверху название занятия и вашу фамилию и имя
      - в каждом задании добавьте решение в требуемом виде (текст/код/скриншоты/ссылка)
      - для корректного добавления скриншотов воспользуйтесь [инструкцией "Как вставить скриншот в шаблон с решением](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md)
      - при оформлении используйте возможности языка разметки md (коротко об этом можно посмотреть в [инструкции  по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md))
   4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`);
   5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
   6. Любые вопросы по выполнению заданий спрашивайте в чате учебной группы и/или в разделе “Вопросы по заданию” в личном кабинете.
   
Желаем успехов в выполнении домашнего задания!
   
### Дополнительные материалы, которые могут быть полезны для выполнения задания

1. [Руководство по оформлению Markdown файлов](https://gist.github.com/Jekins/2bf2d0638163f1294637#Code)

---

### Задание 1

```bash
timur@Netology:~/Git/netology$ git status
Текущая ветка: main
Эта ветка соответствует «origin/main».

нечего коммитить, нет изменений в рабочем каталоге
timur@Netology:~/Git/netology$ nano README.md 
timur@Netology:~/Git/netology$ nano README.md 
timur@Netology:~/Git/netology$ git status
Текущая ветка: main
Эта ветка соответствует «origin/main».

Изменения, которые не в индексе для коммита:
  (используйте «git add <файл>...», чтобы добавить файл в индекс)
  (используйте «git restore <файл>...», чтобы отменить изменения в рабочем каталоге)
        изменено:      README.md

индекс пуст (используйте «git add» и/или «git commit -a»)
timur@Netology:~/Git/netology$ git diff
diff --git a/README.md b/README.md
index ece8446..66eaf76 100644
--- a/README.md
+++ b/README.md
@@ -1,2 +1,3 @@
 # netology
 Git Homework 
+Akayev Timur
timur@Netology:~/Git/netology$ git diff --staged
timur@Netology:~/Git/netology$ git add README.md
timur@Netology:~/Git/netology$ git diff
timur@Netology:~/Git/netology$ git diff --staged
diff --git a/README.md b/README.md
index ece8446..66eaf76 100644
--- a/README.md
+++ b/README.md
@@ -1,2 +1,3 @@
 # netology
 Git Homework 
+Akayev Timur
timur@Netology:~/Git/netology$ git commit -m 'First commit'
[main 180b7f7] First commit
 1 file changed, 1 insertion(+)
timur@Netology:~/Git/netology$ git push origin master
error: src refspec master ничему не соответствует
error: не удалось отправить некоторые ссылки в «https://github.com/timurgithub/netology.git»
timur@Netology:~/Git/netology$ git branch
* main
timur@Netology:~/Git/netology$ git push origin main
Перечисление объектов: 5, готово.
Подсчет объектов: 100% (5/5), готово.
Запись объектов: 100% (3/3), 279 байтов | 279.00 КиБ/с, готово.
Всего 3 (изменений 0), повторно использовано 0 (изменений 0), повторно использовано пакетов 0
To https://github.com/timurgithub/netology.git
   a61766f..180b7f7  main -> main
```

`При необходимости прикрепитe сюда скриншоты
![Задание_1](https://github.com/timurgithub/netology-git-hw/blob/main/img/1.png)

[Ссылка на коммит](https://github.com/timurgithub/netology/commit/180b7f74e1ebafa937a86a408074fe7f882d34f8)
---

### Задание 2

`Создание файла .gitignore`
```bash
touch .gitignore```

`Проверка статуса`
```bash
git status
```

`Добавление файла в индекс`
```git add .gitignore```

`Добавление правил в .gitignore`
```bash
nano .gitignore >> *.pyc, cache/
```

`Коммит изменений`
```bash
git commit -m "Add .gitignore to ignore .pyc files and cache directory"
```

`Пуш изменений в удаленный репозиторий`
```bash
git push origin main
```

`При необходимости прикрепитe сюда скриншоты
![Задание_2](https://github.com/timurgithub/netology-git-hw/blob/main/img/2.png)

[Ссылка на коммит](https://github.com/timurgithub/netology/commit/508baaf9a31750586781269d912527c73ddf8e01)
---

### Задание 3

`Создание и переключение на ветку dev`
```bash
git checkout -b dev
```

`Создание и добавление файла test.sh`
```bash
nano test.sh
git add test.sh
git commit -m "Add test.sh"
git push origin dev
```

`Изменение и добавление файла test.sh`
```bash
nano test.sh
git add test.sh
git commit -m "Update test.sh"
git push origin dev
```

`Переключение на основную ветку`
```bash
git checkout main
```

`Создание и добавление файла main.sh`
```bash
echo "#!/bin/bash" > main.sh
echo "echo 'Main branch script'" >> main.sh
git add main.sh
git commit -m "Add main.sh with initial content"
git push origin main
```

`Мердж ветки dev в основную`
```
git checkout main
git merge dev
```

`Пуш в основную ветку`
```bash
git push origin main
```
[Ссылка на граф коммитов](https://github.com/timurgithub/netology-git-hw/network)