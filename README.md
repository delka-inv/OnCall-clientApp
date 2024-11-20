
# Назначение ПО

Основной целью данного ПО является упрощение работы с сервисом OnCall в базовых действиях сотрудника ГДМ, таких как: оповещение ответственных пользователей по тому или иному алерту, откладывание алерта до определённого времени помимо стандартных функций и другие функции, представляющие из себя автоматизацию некоторых рутинных действий.

# Условия работы ПО

- Последняя версия браузера Google Chrome
- Зарегистрированный аккаунт Grafana Invitro с доступом к плагину OnCall (редактирование)

# Инструкция по установке
1. Скачать [последнюю версию](https://github.com/delka-inv/OnCall-clientApp/releases/latest) ПО 
2. Распаковать в удобное место
3. Перейти на страницу расширений (chrome://extensions/)
4. Включить режим разработчика, если он не включен
5. Нажать кнопку "Загрузить распакованное расширение" и указать путь к папке с расширением
6. Расширение успешно установлено, если оно отобразилось в списке расширений

# Состав ПО
Приложение состоит из двух частей: меню настройки и дополнение интерфейса OnCall

1. Меню настройки активируется нажатием ЛКМ по иконке расширения. При нормальной работе расширения открывается панель, состоящую из панели взаимодействия и таблицы со сводной информацией. Для полноценной работы расширения рекомендуется установить json-конфигурацию, сгенерированную в [соответствующем приложении](https://github.com/delka-inv/OnCall-fileCreator).

2. Видоизменённый интерфейс доступен на странице алерта и представляет из себя две дополнительные кнопки: "Дополнительные действия" и "Передать ответственным".
 - "Дополнительные действия" - это небольшой набор функций, направленных на автоматизацию рутинных действий. На данный момент в список функций входит:
    + "Отложить до рабочего времени" - отложить алерт до ближайших 09:00 по Московскому времени
    + "Отложить до понедельника" - отложить алерт до ближайших 09:00 ближайшего понедельника по Московскому времени
    + "Отложить до ..." - отложить алерт до указанной даты и времени.
    + "Обработано, закрыть алерт" - добавить запись с текстом "Обработано" и закрыть текущий алерт на себе.

 - "Передать ответственным" - на основе обработанного конфигурационного файла собирается информация о текущем алерте, и если он описан, указывается список сотрудников для их дальнейшего привлечения к работе с алертом.

 Все функции работают на основе отправки клиентских запросов к API OnCall
