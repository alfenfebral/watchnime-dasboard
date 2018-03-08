# watchnime-dasboard
dashboard + api build with laravel 5.5 for watchnime

#init

cd watchnime-dasboard

composer install

sudo chmod 777 storage/ -R #chmod for storage

cp .env.example .env #open .env and configure database username and password

php artisan key:generate

php artisan migrate:refresh --seed

yarn install #install packet node js

npm run production #bundle to ready production


#auto migrate enable, to disable remove this. app/Console/Kernel.php

   protected function schedule(Schedule $schedule)
    {
        $schedule->command('migrate:refresh --seed')
                 ->everyThirtyMinutes();
    }
    
    
    
#dummy

Username: test@example.com
Password: 123456
