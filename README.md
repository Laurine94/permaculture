# permaculture

installer symfony

cd <projet>
dans .env modifier : DATABASE_URL=pgsql://<user>:<password>@127.0.0.1:5432/Permaculure 
composer install
  Créer la bdd sur phpMyAdmin
php bin/console doctrine:database:create
  
  Lancer le server:
  symfony server:start
  
  mettre a jour ta bdd:
  php bin/console doctrine:migrations:migrate
  
  création de la fixture
  composer require orm-fixtures --dev
Installer la librairie Faker
composer require fzaninotto/faker

lancer les fixture
php bin/console doctrine:fixtures:load
