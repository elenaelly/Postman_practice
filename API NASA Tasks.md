## API NASA Task-1

**Данные:**

1. Тестовое задание выполняется на площадке open api NASA - [https://api.nasa.gov/](https://api.nasa.gov/)
2. Задание выполнять в Postman

**Задача:**

1. Необходимо найти запросы Mars Rover Photos
2. Выполнить запрос по Querying by Earth date на дату 21.01.2022
3. Передать в переменную окружения id второй фотографии, распарсив json
4. Ответ на задание прислать в следующем виде:
- URL получившегося запроса
- Код js для передачи переменной

- **Ответ**
    
    [https://api.nasa.gov/mars-photos/api/v1/rovers/curiosity/photos?earth_date=2022-01-21&api_key=DEMO_KEY](https://api.nasa.gov/mars-photos/api/v1/rovers/curiosity/photos?earth_date=2022-01-21&api_key=DEMO_KEY)
    
    ```jsx
    const jsonData = JSON.parse(responseBody);
    var responseJson = pm.response.json();
    var secondId = responseJson.photos[1].id;
    pm.environment.set("secondId", secondId);
    ```
