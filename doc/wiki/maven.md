## Настройки

    Путь к мавен репозиторию можно поменять тут: MAVEN_HOME\conf\settings.xml
    Например  <localRepository>c:/mvn_repo</localRepository>
    В IDEA в настройках Maven надо проверить 
    (и переопределить, если неверно) путь к конфигурации и maven

- <a href="https://maven.apache.org/settings.html">Настройки</a>

## Не подтягивается зависимость (pom.xml в окошке Maven показывается красной). Причины: 
  - не подтянулась зависимость. Обновляем в окошке Maven
![image](https://cloud.githubusercontent.com/assets/13649199/18507767/6b20f57e-7a7a-11e6-9f0c-8b175c152ff5.png)
  - **неверно закачалась. Чистим зависимость в локальном Maven репозитории. По умолчанию в `~/.m2` (для Windows это `c:\Users\[login]\.m2`) удаляем каталог зависимости, например `\org\slf4j\slf4j-api\1.7.28` и делаем Reimport All (первая кнопка окошка Maven)**
  - Maven в режиме offline и не подключен к инету. Кнопка `Toggle Offline Mode` в IDEA окошке Maven 
  - отсутствует в центральном maven репозитории. Проверяем тут [https://search.maven.org/#browse](https://search.maven.org/#browse)

## Ресурсы
- <a href="http://maven.apache.org/">Home Page</a>
- <a href="http://www.apache-maven.ru/">Maven по русски</a>.
- <a href="http://search.maven.org/#browse">The Central Repository</a>
- <a href="http://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html">Build Lifecycle</a>.
- <a href="http://maven.apache.org/guides/introduction/introduction-to-dependency-mechanism.html">Dependency Mechanism</a>
- <a href="http://www.ibm.com/developerworks/ru/library/j-5things13/">Зависимости, профили</a>
- <a href="http://maven.apache.org/guides/mini/guide-multiple-modules.html">The Reactor</a>.
- <a href="http://books.sonatype.com/mvnref-book/reference/index.html">Maven: The Complete Reference</a>
