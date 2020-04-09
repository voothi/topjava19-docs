Git
==============

### <a href="http://info.javarush.ru/idea_help/2014/02/14/Руководство-пользователя-IntelliJ-IDEA-Основы-работы-с-системами-контроля-версий-.html">Основы работы с системами контроля версий в IntelliJ IDEA</a>

## Правила работы с патчами на проекте
- Как накатывать патчи есть в видео вступительного занятия <a href="https://github.com/JavaOPs/topjava#-3-работа-с-проектом-выполнять-инструкции">Работа с проектом<a/>
- **Все изменения в проекте производятся только патчами из урока в ветке `master`, а cвой код (домашние задания) пишете только в ветках `HWxx`. Модификация кода в ветке master только через патчи в материалах урока (`Apply Patch`), иначе придется мержить код.  Все патчи объязательны и применяются по порядку. Если при применении патча предлагается мердж, cмотрите: [Patch не накатывается (предлагает merge)](#patch-%D0%BD%D0%B5-%D0%BD%D0%B0%D0%BA%D0%B0%D1%82%D1%8B%D0%B2%D0%B0%D0%B5%D1%82%D1%81%D1%8F-%D0%BF%D1%80%D0%B5%D0%B4%D0%BB%D0%B0%D0%B3%D0%B0%D0%B5%D1%82-merge)
.** 
> ВНИМАНИЕ! проверьте при коммите, что галочка справа `Optimize imports` выключена, иначе ваши классы будут отличаться от тех, что в репозитории.

- **Делать Apply Patch лучше по одному, непосредственно перед видео на эту тему, а при просмотре видео сразу отслеживать все изменения кода проекта по изменению в патче (`Version Control->Local Changes-> Ctrl+D на файле, Alt + Left/Right для просмотра следующего изменения`):**
 
![image](https://cloud.githubusercontent.com/assets/13649199/18313728/b4d683bc-7518-11e6-8150-f6719385b338.png)


- **при первом Apply надо выбрать имя локального ченджлиста `Name: Default`. Все остальные патчи (если имя не менять) будут также в него попадать.**

![image](https://user-images.githubusercontent.com/13649199/28166049-1b0b9924-67df-11e7-8506-122f0c2781f3.png)

- `commit` **настоятельно рекомендую** делать после каждого патча (тогда изменения в проекте смотреть легче и искать ошибки в комитах гораздо проще), а `push` после всех патчей/коммитов урока (откатываться проще и работы меньше).

- **После патча часто полезно запустить и посмотреть на работу приложения** (если оно запускается).

- **Правило**: Перед каждым изменением проверяйте что меняется: Ctrl+D по всем файлам ченджлиста.
Если только пробелы - делайте revert.


## Как вести проект в локальном репозитории
#### Вступительное занятие:
- apply patch `Prepare_to_HW0.patch`
- `git commit`
- проверить, что все корректно закомитилось (в `Version Control:Local Changes` **пусто**) -> **push**

#### Домашнее задание HW0:
- создать ветку `HW0`: в IDEA внизу справа `+ New Branch ->HW0`

![new_branch](https://cloud.githubusercontent.com/assets/13649199/13717279/8fcf7a42-e7f1-11e5-862f-b1fd3e302666.png)

- выполняете Домашнее Задание (HW0)
- проверить каждое изменение в `Version Control:Local Changes` -> **commit**
- выполняете HW0 Optional
- проверить каждое изменение в `Version Control:Local Changes` -> **commit**
- проверить в `Version Control:Log`, что все патчи корректно закомитились и в `Version Control:Local Changes` **пусто**  -> **push**

#### Урок 1:
- переключаемся на `master`:  в IDEA внизу справа `Local Branches -> master -> checkout`
- apply **каждый** патч урока `Lesson01`. 
- проверить каждое изменение в `Version Control:Local Changes` -> **commit**
- проверить в `Version Control:Log`, что все патчи корректно закомитились и в `Version Control:Local Changes` **пусто**  -> **push**

#### Домашнее задание HW1:
- создать ветку `HW1`: в IDEA внизу справа `+ New Branch ->HW1`
- выполняете HW1
- проверить каждое изменение в `Version Control:Local Changes` -> **commit**
- выполняете HW1 Optional
- проверить каждое изменение в `Version Control:Local Changes` -> **commit**
- проверить, что все патчи корректно закомитились в `Version Control:Log`, в `Version Control:Local Changes` **пусто** -> **push**

#### Урок 2:
- переключаемся на `master`:  в IDEA внизу справа `Local Branches -> master -> checkout`
- apply **каждый** патч урока `Lesson02`. 
- проверить каждое изменение в `Version Control:Local Changes` -> **commit**
- проверить в `Version Control:Log`, что все патчи корректно закомитились и в `Version Control:Local Changes` **пусто**  -> **push**
- ...

Так должна выглядеть ваш Version Control -> Log:
![branch](https://cloud.githubusercontent.com/assets/13649199/13716918/15c2a456-e7ef-11e5-9db2-8f2db69ff1e3.png)

## Как откатить patch?

Version control -> Log
Правой кнопкой на нужной ревизии -> `Reset Current Branch to Here`
`Soft`- оставить все изменения, `Hard` - все затереть (в том числе локальные изменения)

![resetcurrentbranch](https://cloud.githubusercontent.com/assets/13649199/10559911/03be0a98-7503-11e5-98c6-eea3f062aba5.png)

### Если изменения уже запушили, то нужно <a href="http://stackoverflow.com/questions/5509543/how-do-i-properly-force-a-git-push#12610763">их перетереть новым `push --force`</a>

В IDEA в `protected branches` убрать ветки, на которые требуется force push:

![git_force](https://user-images.githubusercontent.com/13649199/68410238-7b640d00-0199-11ea-8b45-577493455777.png)
![git_force2](https://user-images.githubusercontent.com/13649199/28743999-5632a780-7460-11e7-8b57-8340b6c1c16c.png)
<hr>

## Обновить проект из github: `Ctrl+T`
![update](https://user-images.githubusercontent.com/13649199/28744034-2fafcae2-7461-11e7-9d0d-dfb4fe0c4ae8.png)

## Сравнить файл после определенного патча на github с локальным
1. Идем в историю коммитов репозитория проекта:

![image](https://user-images.githubusercontent.com/13649199/39063950-59ffafd4-44d5-11e8-8b97-276fca11d460.png)

2. Выбираем просмотр репозитория после нужного патча 

![image](https://user-images.githubusercontent.com/13649199/39064172-2f1c88d6-44d6-11e8-8388-ac3782f3902b.png)

3. Выбираем проблемный файл в формате `Raw`

![image](https://user-images.githubusercontent.com/13649199/39064293-afa1d164-44d6-11e8-9ecf-46b669976852.png)

4. Копируем в буфер и сравниваем со своим в IDEA

![image](https://user-images.githubusercontent.com/13649199/39064400-0f345dc2-44d7-11e8-8a79-5faad4bd75f8.png)

## Patch не накатывается (предлагает merge)

**Вероятнее всего Ваша ветка master не соответствует моей. Нужно просто сравнить проблемный файл.**

 Например открываете проблемный класс на github в режиме Raw (кнопка справа вверху над классом, например `https://raw.githubusercontent.com/JavaWebinar/topjava02/master/src/main/java/ru/javawebinar/topjava/web/meal/UserMealRestController.java`, копируете его (`Ctrl+A, Ctrl+C`) и сравниваете со своим в IDEA: `View->Compare with Clipboard`.

В более общем случае (когда github уже ушел вперед) посмотреть содержимое файла для определенной версии в IDEA можно
через Git->History на файле:
![idea_history](https://cloud.githubusercontent.com/assets/13649199/10560189/9f6b6046-750b-11e5-863e-6084cdeeb3ed.png)
или на истории изменений Version Control->Log

![idea_revision](https://cloud.githubusercontent.com/assets/13649199/10560200/e585d67e-750b-11e5-865c-a9485c68435f.png)
и двойном щелчке на файле.

Сравнивать можно в github с текущей версией проекта либо с соответствующей ревизией:

![github_revision](https://cloud.githubusercontent.com/assets/13649199/10560234/347dbeda-750d-11e5-8b03-a1b62b94166d.png)

<hr>
Сравнить содержимое можно скопировав содержимое из github в буфер:


![github_raw](https://cloud.githubusercontent.com/assets/13649199/10560439/304104e2-7514-11e5-9aea-16bf2466da83.png)

и сделать Compare with clipboard в IDEA:

![compare_with_clipboard](https://cloud.githubusercontent.com/assets/13649199/10560411/4be3809a-7513-11e5-914e-94b4efb5b08e.png)

Если ваш файл совпадает с тем, что в репозитории и патч все равно не накатывается, напришите мне в личку- имя файла, номер патча и проблемные строки, я поправлю патч. Картинок с вашими ошибками слать НЕ НАДО, учимся грамотно определять и описывать проблему.

## Чем просматривать локально файлы в формате markdown ?
- в IDEA, плагин **Markdown Navigator**
- в Chrome, плагин <a href="https://chrome.google.com/webstore/detail/markdown-preview/jmchmkecamhbiokiopfpnfgbidieafmd">Markdown Preview</a> (в опциях надо разрешить открывать файлы по ссылкам)
- можно вчекинить уроки себе с github репозиторий и смотреть через github

## Если все поломалось:
- откатываете ревизии до "хорошего" патча [Как откатить patch](#Как-откатить-patch) с выбором `Hard` (все локальные изменения также пропадут). Затем накатываете патчи заново по порядку.
- Сделайте fork, либо `clone` с нашего репозиторий c уже примененными патчами (см ниже).

## Клонирование проекта
- Создайте локальную копию проекта: `git clone https://github.com/..../project`
- Перейдите в каталог проекта: `cd project`
- Настройте git в локальном проекте на свой проект в GitHub:
  - `git remote -v`
  - `git remote set-url origin url_на_твой_репозиторий.git` - настройка pull
  - `git remote set-url --push origin url_на_твой_репозиторий.git` - настройка push
  - `git push -u origin master` - первый push с свой репозиторий

## Манипуляции с коммитами до push:
Клик на ревизии в `Local Changes` и -> `Interactively Rebase from Here...`
- `action -> squash` - Склеить 
- другие действия