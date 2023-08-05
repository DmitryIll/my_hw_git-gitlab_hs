# Домашнее задание к занятию "`GIT`" - `'Илларионов Дмитрий'`


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

1. Зарегистрируйте аккаунт на [GitHub](https://github.com/).
`Зарегистрировал и склонировал репозиторий hw сюда:`
<https://github.com/DmitryIll/my_hw_git-gitlab_hs>

1. Создайте  **новый отдельный публичный репозиторий**. Обязательно поставьте галочку в поле «Initialize this repository with a README».
`Создал еще один репоизторий:`
<https://github.com/DmitryIll/my_repos_2.git>

2. Склонируйте репозиторий, используя https протокол `git clone ...`.
`Склонировал:`
![Склонировал](1.png)

```sh
git clone https://github.com/DmitryIll/my_repos_2.git
```

3. Перейдите в каталог с клоном репозитория.

```sh
git cd my_repos_2
```
1. Произведите первоначальную настройку Git, указав своё настоящее имя и email: `git config --global user.name` и `git config --global user.email johndoe@example.com`.

`Выполнил:`
```
$ git config --global user.name DmitryIll
$ git config --global user.email dnillarionov@gmail.com
```
![Сконфигурировал](image.png)

1. Выполните команду `git status` и запомните результат.

![git status](image-3.png)

1. Отредактируйте файл README.md любым удобным способом, переведя файл в состояние Modified.

`внес правки`
1. Ещё раз выполните `git status` и продолжайте проверять вывод этой команды после каждого следующего шага.

![git status](image-4.png)

1. Посмотрите изменения в файле README.md, выполнив команды `git diff` и `git diff --staged`.

![](image-5.png)


1. Переведите файл в состояние staged или, как говорят, добавьте файл в коммит, командой `git add README.md`.

![](image-6.png)

1. Ещё раз выполните команды `git diff` и `git diff --staged`.

![Alt text](image-7.png)

1. Теперь можно сделать коммит `git commit -m 'First commit'`.

![](image-8.png)

1. Сделайте `git push origin master`.

![](image-9.png)

`ветки master нет, но, есть ветка main:`

![](image-10.png)

`скорректировал:`

![](image-11.png)

В качестве ответа добавьте ссылку на этот коммит в ваш md-файл с решением.

```
код коммита:
0c82cfcc367bab700c853a3db0f8f32b7c34ebaf
```
https://github.com/DmitryIll/my_repos_2/commit/0c82cfcc367bab700c853a3db0f8f32b7c34ebaf

---
### Задание 2

**Что нужно сделать:**

1. Создайте файл .gitignore (обратите внимание на точку в начале файла) и проверьте его статус сразу после создания.

![](image-12.png)

![](image-13.png)

1. Добавьте файл .gitignore в следующий коммит `git add...`.

![](image-14.png)

1. Напишите правила в этом файле, чтобы игнорировать любые файлы `.pyc`, а также все файлы в директории `cache`.

![](image-15.png)

1. Сделайте коммит и пуш.



В качестве ответа добавьте ссылку на этот коммит в ваш md-файл с решением.

---

### Задание 3

**Что нужно сделать:**

1. Создайте новую ветку dev и переключитесь на неё.
2. Создайте в ветке dev файл test.sh с произвольным содержимым.
3. Сделайте несколько коммитов и пушей  в ветку dev, имитируя активную работу над  файлом в процессе разработки.
4. Переключитесь на основную ветку.
5. Добавьте файл main.sh в основной ветке с произвольным содержимым, сделайте комит и пуш . Так имитируется продолжение общекомандной разработки в основной ветке во время разработки отдельного функционала в dev  ветке.
6. Сделайте мердж dev  ветки в основную с помощью git merge dev. Напишите осмысленное сообщение в появившееся окно комита.
7. Сделайте пуш в основной ветке.
8. Не удаляйте ветку dev.

В качестве ответа прикрепите ссылку на граф коммитов https://github.com/ваш-логин/ваш-репозиторий/network в ваш md-файл с решением.

Ваш граф комитов должен выглядеть аналогично скриншоту:   

![скрин для Git](https://github.com/netology-code/sdvps-homeworks/assets/77622076/e73589cf-7e97-40e5-ac01-d1d55376f1b9)

---
## Дополнительные задания* (со звёздочкой)

Их выполнение необязательное и не влияет на получение зачёта по домашнему заданию. Можете их решить, если хотите лучше разобраться в материале.

---
### Задание 4*

Сэмулируем конфликт. Перед выполнением изучите [документацию](https://git-scm.com/book/ru/v2/%D0%98%D0%BD%D1%81%D1%82%D1%80%D1%83%D0%BC%D0%B5%D0%BD%D1%82%D1%8B-Git-%D0%9F%D1%80%D0%BE%D0%B4%D0%B2%D0%B8%D0%BD%D1%83%D1%82%D0%BE%D0%B5-%D1%81%D0%BB%D0%B8%D1%8F%D0%BD%D0%B8%D0%B5).

**Что нужно сделать:**

1. Создайте ветку conflict и переключитесь на неё.
2. Внесите изменения в файл test.sh. 
3. Сделайте коммит и пуш.
4. Переключитесь на основную ветку.
5. Измените ту же самую строчку в файле test.sh.
6. Сделайте коммит и пуш.
7. Сделайте мердж ветки conflict в основную ветку и решите конфликт так, чтобы в результате в файле оказался код из ветки conflict.

В качестве ответа на задание прикрепите ссылку на граф коммитов https://github.com/ваш-логин/ваш-репозиторий/network в ваш md-файл с решением.

