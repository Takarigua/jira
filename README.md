# Домашнее задание к занятию 7 «Жизненный цикл ПО»

## Подготовка к выполнению

1. Получить бесплатную версию Jira - https://www.atlassian.com/ru/software/jira/work-management/free (скопируйте ссылку в адресную строку). Вы можете воспользоваться любым(в том числе бесплатным vpn сервисом) если сайт у вас недоступен. Кроме того вы можете скачать [docker образ](https://hub.docker.com/r/atlassian/jira-software/#) и запустить на своем хосте self-managed версию jira.
2. Настроить её для своей команды разработки.
3. Создать доски Kanban и Scrum.
4. [Дополнительные инструкции от разработчика Jira](https://support.atlassian.com/jira-cloud-administration/docs/import-and-export-issue-workflows/).

## Основная часть

Необходимо создать собственные workflow для двух типов задач: bug и остальные типы задач. Задачи типа bug должны проходить жизненный цикл:

1. Open -> On reproduce.
2. On reproduce -> Open, Done reproduce.
3. Done reproduce -> On fix.
4. On fix -> On reproduce, Done fix.
5. Done fix -> On test.
6. On test -> On fix, Done.
7. Done -> Closed, Open.

Остальные задачи должны проходить по упрощённому workflow:

1. Open -> On develop.
2. On develop -> Open, Done develop.
3. Done develop -> On test.
4. On test -> On develop, Done.
5. Done -> Closed, Open.

**Что нужно сделать**

1. Создайте задачу с типом bug, попытайтесь провести его по всему workflow до Done. 
1. Создайте задачу с типом epic, к ней привяжите несколько задач с типом task, проведите их по всему workflow до Done. 
1. При проведении обеих задач по статусам используйте kanban. 
1. Верните задачи в статус Open.
1. Перейдите в Scrum, запланируйте новый спринт, состоящий из задач эпика и одного бага, стартуйте спринт, проведите задачи до состояния Closed. Закройте спринт.
2. Если всё отработалось в рамках ожидания — выгрузите схемы workflow для импорта в XML. Файлы с workflow и скриншоты workflow приложите к решению задания.

---

### Как оформить решение задания

Выполненное домашнее задание пришлите в виде ссылки на .md-файл в вашем репозитории.

---

### Ответ

Я сделал немного больше тасок/тестов, чтобы просто лучше понять процесс, поэтому в scrume и в workflow у меня их больше чем надо. Прогнал их туда сюда оставляя их в разных статусах. Как возобновлял, так и полностью закрывал.

----

Начну со схем Bug Workflow Fina - https://github.com/Takarigua/jira/blob/9cc2188306b20f82f90f7afe39c56bb10b0e8764/Bug%20Workflow%20Final.xml и Simple Workflow Final - https://github.com/Takarigua/jira/blob/9cc2188306b20f82f90f7afe39c56bb10b0e8764/Simple%20Workflow%20Final.xml

----

2.![BugWorkflow](https://github.com/Takarigua/jira/blob/56043223e82d41e70e3fc75558fdd98ca8927f93/screen/BugWorkflow.png) 

---

3.![Simple Workflow](https://github.com/Takarigua/jira/blob/56043223e82d41e70e3fc75558fdd98ca8927f93/screen/Simple%20Workflow.png)

---

4.[Тесты Workflow](https://github.com/Takarigua/jira/blob/56043223e82d41e70e3fc75558fdd98ca8927f93/screen/%D0%A2%D0%B5%D1%81%D1%82%D1%8B%20Workflow.png)

---

5.[Scrum](https://github.com/Takarigua/jira/blob/56043223e82d41e70e3fc75558fdd98ca8927f93/screen/Scrum.png)
