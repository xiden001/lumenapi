Simple Lumen API with JWT AUthentication
Usage

git clone https://github.com/xiden001/lumenapi.git

cd lumenapi

create .env file 

composer install

Uncomment the following in bootstrap/app
****$app->withFacades();
****$app->withEloquent();

Also add in bootstrap/app,
$app->register(Tymon\JWTAuth\Providers\LumenServiceProvider::class);

php artisan jwt:secret (Generates JWT secret key)

php artisan migrate (run migration to populate database)

php -S localhost:8000 -t public (Launch using inbuilt php server)