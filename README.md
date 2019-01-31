## New Reports Team Coding Challenge

Below is a coding challenge for you to complete. You should be able to complete this challenge in couple of evenings of effort.

### Coding Spec:
Write an java microservice which collects current weather data for interested locations and provides ability to view weather history for them.
Weather data provider should be selected when city is added.

### Limitations:
* Java8
* Jooby with netty for webserver
* Retrofit for http
* Postgres for data storage
* Swagger for api documentation
* Data access via Jdbc, Sql2o, Flywaydb
* Dependencies loaded via gradle
* Docker for deploy

### Result:
docker deploy script for java microservice and its dependencies

Simple UI with:

* editable list of interested cities (locations) with current weather
* weather history for the selected city with 3 hour step


### Details:
* Weather data provider 1 [https://openweathermap.org/current](https://openweathermap.org/current), [list of cities](http://bulk.openweathermap.org/sample/city.list.json.gz)
* Weather data provider 2 [https://www.apixu.com/my/](https://www.apixu.com/my/)

### Samples with my auth keys:
```
curl "http://api.openweathermap.org/data/2.5/weather?q=Veshenskaya&units=metric&appid=080fa56b819976cbf04f1a71ff56c2e8" 2>/dev/null | jq .
curl "http://api.openweathermap.org/data/2.5/weather?lat=49.633806&lon=41.712661&units=metric&appid=080fa56b819976cbf04f1a71ff56c2e8" 2>/dev/null | jq .
curl "http://api.openweathermap.org/data/2.5/weather?id=473998&units=metric&appid=080fa56b819976cbf04f1a71ff56c2e8" 2>/dev/null | jq .

curl 'http://api.apixu.com/v1/search.json?key=1e1fe818cc6443a19dc95326193101&q=Veshenskaya' | jq .
curl 'https://api.apixu.com/v1/current.json?key=1e1fe818cc6443a19dc95326193101&q=Veshenskaya' | jq .
```
