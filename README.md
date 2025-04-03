Ниже приведён пример минимальной (index.html) - HTML-страницы, которая:
1.	Позволяет ввести idInstance и apiTokenInstance.
2.	Показывает четыре кнопки для вызова методов:
o	getSettings
o	getStateInstance
o	sendMessage
o	sendFileByUrl
3.	Выводит результат (JSON-ответ от сервера) в поле «только для чтения».
4.	Имеет простой макет (вы можете доработать верстку на свой вкус).
Важно: Формат и названия методов (с прописными или строчными буквами) зависят от официальной документации GREEN-API. В примере ниже названия совпадают с эндпоинтами, указанными в документации.
Пояснения к коду
1.	idInstance, apiToken: Введите значения, которые вы получите при создании инстанса (см. личный кабинет GREEN-API).
2.	Номер получателя:
o	GREEN-API в большинстве случаев требует указывать телефон в формате 71234567890@c.us (для РФ это 7 + номер без «+»).
o	В коде я автоматически добавляю @c.us в конце.
3.	Методы:
o	getSettings → GET /waInstance{ID}/GetSettings/{token}
o	getStateInstance → GET /waInstance{ID}/getStateInstance/{token}
o	sendMessage → POST /waInstance{ID}/sendMessage/{token}
o	sendFileByUrl → POST /waInstance{ID}/sendFileByUrl/{token}
4.	Вывод: Результат от API (JSON) отображается в textarea с атрибутом readonly.
