### <a href="http://jeeconf.com/archive/jeeconf-2013/materials/intellij-idea/">Эффективная работа с кодом в IntelliJ IDEA</a>

### <a href="https://www.youtube.com/watch?v=eq3KiAH4IBI">42 IntelliJ IDEA Tips and Tricks</a>

### <a href="https://blog.jetbrains.com/idea/2016/12/ide-features-trainer/">IDEA Features Trainer</a>

### <a href="http://info.javarush.ru/idea_help/2014/01/22/Руководство-пользователя-IntelliJ-IDEA-Отладчик-.html">Отладчик IntelliJ IDEA</a>

### <a href="https://www.mkyong.com/intellij/intellij-idea-run-debug-web-application-on-tomcat/">IntelliJ IDEA – Run / debug web application on Tomcat</a>

### [Advanced Breakpoint Settings in IDEA](https://nirlaor.wordpress.com/2011/02/10/advanced-breakpoint-settings-in-idea/)

### <a href="https://habrahabr.ru/post/279897/">Настройка Jetbrains IntelliJ Idea в Linux Ubuntu 14.04 LTS</a>

### [Intellij Jvm Options Explained](https://github.com/FoxxMD/intellij-jvm-options-explained)

### <a href="http://stackoverflow.com/questions/8942751/use-intellij-to-generate-class-diagram#26926334">Generate class diagram</a>

### <a href="http://stackoverflow.com/a/40556256/548473">Debug JSP</a>

### [Сравнение файлов и папок в IntelliJ IDEA](https://habr.com/ru/post/491496/)

### [Лучшие плагины IntelliJ IDEA](https://habr.com/ru/post/486578/)

Справочник (поиск) по использованию горячих клавиш: `Ctrl+Shift+A`

Если приложение работает, а IDEA отказывается и причина непонятна `File -> Invalidate Caches/Restart -> Invalidate and Restart`

### Выставить кодировку UTF-8 в консоли:

- `Help menu -> Edit Custom VM Options`: добавьте
```
 -Dfile.encoding=UTF-8
 -Dconsole.encoding=UTF-8`
```
- Restart IntelliJ

### Советы по настройка остальных опций:
- [Slow startup time on Windows](https://youtrack.jetbrains.com/issue/IDEA-211178#focus=streamItem-27-3412218.0-0)
- [Customize IntelliJ IDEA Memory](http://tomaszdziurko.com/2015/11/1-and-the-only-one-to-customize-intellij-idea-memory-settings)
- [Increase IDE memory limit in IntelliJ IDEA](https://stackoverflow.com/questions/13578062)

## Показывать строчки в IDEA:
![image](https://cloud.githubusercontent.com/assets/13649199/18053369/b39438d6-6e07-11e6-8a74-dbf796ecb5d5.png)

## Обновить зависимости в maven проекте:
![image](https://cloud.githubusercontent.com/assets/13649199/18507767/6b20f57e-7a7a-11e6-9f0c-8b175c152ff5.png)

## Деплой war в Tomcat (`Application Context` должен быть тот же, что и url приложения, деплоить надо `war exploded`)
![tomcat](https://cloud.githubusercontent.com/assets/975870/11599106/057932c4-9ad6-11e5-9e9e-fe9fd389532e.png)

## Remote debug в новой IDEA:
Порт remote debug по умолчаниню у Tomcat: 8000
![Remote debug](https://user-images.githubusercontent.com/13649199/59295289-fc22e980-8c8b-11e9-8720-967e1684185e.png)

##   Ошибки Spring: There is more than one bean / Coudln't autowire:
![spring_ctx](https://cloud.githubusercontent.com/assets/13649199/10559681/96b8bcca-74ff-11e5-8203-8d0d4cf1bd19.png)

### Проверьте, что правильно выставлены профили Spring.

![image](https://cloud.githubusercontent.com/assets/13649199/25596554/58158758-2ed2-11e7-9d42-71501a700deb.png)

### Для тестовых контекстов поставьте чекбокс Check test files в Inspections.

![image](https://cloud.githubusercontent.com/assets/13649199/18831817/8a858f22-83f0-11e6-837e-bf5317b33b3a.png)

### Проверьте - нет ли лишних бинов (или наоборот их не хватает) в Project Structure->Modules->Spring (если не работает редактирование- удалить и создать заново):

![image](https://cloud.githubusercontent.com/assets/13649199/22221277/52c03cb4-e1c3-11e6-9039-08787e31a505.png)

-------------------------

## Поставить кодировку UTF-8

Выставьте в `Settings->File Encoding` везде UTF-8.

По умолчанию: `File-> Other Settings-> Default Settings..->File Encoding`

Также можно сконвертировать файл в нужную кодировку внизу в строке статуса (View -> Status Bar поднят).
![utf-8](https://cloud.githubusercontent.com/assets/13649199/10559841/e1b65654-7501-11e5-8913-d2b5b4e25087.png)

---------------

## Поменять фонт по умолчанию (DejaVu) или **[новый JetBrains Mono](https://habr.com/ru/company/jugru/news/t/484134/)**:

- Скачиваете [DejaVu](https://sourceforge.net/projects/dejavu) или [JetBrainsMono](https://www.jetbrains.com/lp/mono) и устанавливаете в операционную систему (<a href="http://netler.ru/ikt/windows7-font.htm">установка в Windows</a>)
- Перегружаете IDEA
- В IDEA Settings нужно сделать схеме Save As с именем, отличным от Default:
![idea_fonts](https://cloud.githubusercontent.com/assets/11200258/11875035/b09d058c-a4f3-11e5-9d35-88e1b607c310.png)

<hr>

## Добавить поддержку DB в JDBC
- сконфигурить DataSource
- проверить включенный плагин `Database Tools and SQL` и `IntelliLang`
- `Alt+Enter` на SQL и кликнуть на: 
   - выбрать `Language Injection Settings`
![image](https://user-images.githubusercontent.com/13649199/75113155-3f778980-565c-11ea-8094-1bd9a28d05c3.png)
   - выбрать `PostgreSQL`
![image](https://user-images.githubusercontent.com/13649199/75113178-70f05500-565c-11ea-8e84-9b524e41f29c.png)

## Добавить JPA:

![image](https://cloud.githubusercontent.com/assets/13649199/16520055/134bfb42-3f96-11e6-8653-2b75cf3b0f52.png)

![image](https://cloud.githubusercontent.com/assets/13649199/16520135/b87ba914-3f96-11e6-8758-4ebd45443165.png)

## Для динамической перегрузки ресурсов кнопка нажмите кнопку `Update Resource on Frame Deactivation`

![image](https://cloud.githubusercontent.com/assets/13649199/22221467/4819a2f4-e1c4-11e6-9d03-4fe7fcdaafb9.png)

## В spring-db.xml неактивные профили не становаться серыми

Проверьте
![image](https://cloud.githubusercontent.com/assets/13649199/22104238/562485bc-de4f-11e6-9efb-dc2f5e4132c6.png)

## Если непонятно, что за класс или метод перед вами:
Посмотреть javadoc: `Ctrl+N`:`имя_класса`
Если нет исходников - попробовать загрузить через Maven (если не получается- можно попробовать вручную с [Maven Central](http://search.maven.org/#browse))

![image](https://user-images.githubusercontent.com/13649199/37712797-0975ddf2-2d26-11e8-9ef0-4e7132b84d8f.png)

Читать javadoc можно напрямую, либо через `Ctrl+Q`

## Внимание! Лизензия выдается JetBrains только один раз. 

Если она закончилась, можно 
- купить (скидка 25% на месячное продление после окончания лицензии)
- получить на 3 месяца, [порешав задачи на Stepik](https://stepik.org/course/2262). Можно решать не выходя из IDEA через [EduTools плагин](http://javaops.ru/view/story/story21#edutools)
- купить или попросить у знакомых [студенческую почту](https://www.jetbrains.com/student)