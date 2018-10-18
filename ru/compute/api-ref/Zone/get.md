# Метод get
Возвращает информацию об указанной зоне доступности.
 
Чтобы получить список всех зон доступности, используйте
запрос [list](/docs/compute/api-ref/Zone/list).
 
## HTTP-запрос
`GET /compute/v1/zones/{zoneId}`
 
## Path-параметры {#path_params}
 
Name | Description
--- | ---
zoneId | Обязательное поле. Идентификатор зоны доступности, о которой запрашивается информация.  Максимальная длина — 50 символов.
 
## Ответ {#responses}
**HTTP Code: 200 - OK**

Зона доступности. Дополнительные сведения см. в разделе [Зоны
доступности](/docs/overview/concepts/geo-scope).
 
Поле | Описание
--- | ---
id | **string**<br><p>Идентификатор зоны доступности.</p> 
regionId | **string**<br><p>Идентификатор региона.</p> 
status | **string**<br><p>Статус зоны доступности.</p> <ul> <li>UP: Зона доступна. Вы можете обращаться к ресурсам в этой зоне.</li> <li>DOWN: Зона недоступна.</li> </ul> 