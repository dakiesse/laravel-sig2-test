#Laravel SIG2 Test

Требования
----------------------------------

PHP >= 5.5.9
OpenSSL PHP Extension
PDO PHP Extension
Mbstring PHP Extension
Tokenizer PHP Extension
PostgreSQL >= 9.4
PostGIS >= 2.0

Установка
----------------------------------

Зайти в папку проекта и выполнить из терминала

<pre>
composer install
</pre>


Скопировать .env.example в .env и заменить данные секции для PostgreSQL

<pre>
DB_HOST=localhost
DB_DATABASE=homestead
DB_USERNAME=homestead
DB_PASSWORD=secret
</pre>

Количество сида можно изменять с помощью SEED_COMPANY_AMOUNT в .env
По умолчанию 10000 компаний создаст.

Выполнить миграции с сидингом (команда так же позволяет сделать rollback и накатать по новой с сидингом).
Миграции сами производят подключение postgis модуля.
<pre>
php artisan migrate:refresh --seed
</pre>