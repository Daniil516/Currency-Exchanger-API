# Currency-Exchanger-API

"Currency-Exchange-API" is a rails API that receives the currencies exchange rates to US dollar from the Central Bank of the Russian Federation and gives it to you in JSON. Application is secured with bearer authentication. AUTH token you can find in app directory in file `auth_token.txt`. APP has pagination.

### Usage
You launch the application. Then you should send possible(check below) *get* request with BEARER token(In Postman you can easily send request with bearer token by entering it in `authorization` tab, photo below)
![image](https://user-images.githubusercontent.com/83035520/194614201-ee9199b6-3641-4f40-add2-d53cc0b2f1a3.png)


#### Possible requests:
`http://localhost:3000/api/v1/currencies?page=<page number>` - to list currencies and its exchange rate to US dollar.
![image](https://user-images.githubusercontent.com/83035520/194611539-da7b28c9-01f9-42ab-8877-eaa03e77702c.png)

`http://localhost:3000/api/v1/currencies/<currency_iso>` - to get particular currency rate
![image](https://user-images.githubusercontent.com/83035520/194611649-ab4e0287-31f9-4f53-969c-38dcd1fd4f64.png)


### To start

- **WARNING**: This app uses secret api keys for getting exchange rates from external services. So you should have `master.key` in config folder. Ask [owner](https://t.me/Grishchenko1) for this file
- You should have installed ruby(3.0.2) on your pc(how to do this - [here](https://www.ruby-lang.org/en/documentation/installation/)

1. Download all files to single folder
2. Open CMD
3. Open program directory in CMD
4. Install all the gems (libraries) required by the application by entering these commands in CMD:
```
gem install bundler
bundle install
```
5. Insert master.key(check above) in config folder
6. Run migrations
```
bundle exec rails db:migrate
```
7. Launch app by entering this(you are in program directory already)
```
bundle exec rails s
```
9. That's all. Now you can use it as I described in `Usage` section

### P.s
This is my RoR study project that I created during  [good programmer course](https://goodprogrammer-ru.translate.goog/rails?_x_tr_sl=auto&_x_tr_tl=en&_x_tr_hl=en&_x_tr_pto=wapp)

#### What have I learned during developing this app?
- Rails API
- Bearer authentication
- Rails Service Objects
- Pagination, gem kaminari

## RUS

# Обменник валют API

"Обменник валют API" - это rails API, который получает курсы валют к доллару США от Центрального банка Российской Федерации и предоставляет их вам в формате JSON. Приложение защищено с помощью bearer аутентификации. Токен аутентификации вы можете найти в директории приложения в файле `auth_token.txt `. Приложение имеет разбивку на страницы.

### Использование
Вы запускаете приложение. Затем вы должны отправить допустимый(смотрите внизу) *get* запрос с bearer токеном(В Postman вы можете легко отправить запрос с bearer токеном, введя его во вкладке "Авторизация", фото ниже)
![image](https://userimages.githubusercontent.com/83035520/194614201-ee9199b6-3641-4f40-add2-d53cc0b2f1a3.png)


#### Возможные запросы:
`http://localhost:3000/api/v1/currencies?page=<номер страницы>` - Чтобы отобразить список валют с нужной страницы.
![image](https://user-images.githubusercontent.com/83035520/194611539-da7b28c9-01f9-42ab-8877-eaa03e77702c.png)

`http://localhost:3000/api/v1/currencies/<код валюты()>` - чтобы получить необходимый курс валюты
![image](https://user-images.githubusercontent.com/83035520/194611649-ab4e0287-31f9-4f53-969c-38dcd1fd4f64.png)


### Чтобы запустить

- **ВНИМАНИЕ**: Это приложение использует ключи api для получения обменных курсов от внешних сервисов. У вас должен быть `master.key` в папке config. Попросите этот файл у [владельца](https://t.me/Grishchenko1) 
- Вы должны иметь установленный ruby(3.0.2) на свой компьютер(как это сделать - [здесь](https://www.ruby-lang.org/en/documentation/installation/)

1. Скачайте все файлы в отдельную папку
2. Откройте командную строку
3. Откройте директорию программы в командной строке
4. Установите все гемы(библиотеки) требуемые этим приложением, введя в командной строке следующее:
```
gem install bundler
bundle install
```
5. Вставьте `master.key` в папку `config`
6. Прогоните миграции
```
bundle exec rails db:migrate
```
7. Запустите приложение введя это
```
bundle exec rails s
```
9. Это все. Теперь вы можете использовать его так, как я описал в разделе `Использование`

### P.s
Это мой учебный RoR проект, который я сделал во время [курса хорошего программиста](https://goodprogrammer-ru.translate.goog/rails?_x_tr_sl=auto&_x_tr_tl=en&_x_tr_hl=en&_x_tr_pto=wapp)

#### Чему я научился во время разработки этого приложения?
- Rails API
- Bearer авторизация
- Rails Service Objects
- PПагинация, gem kaminari
