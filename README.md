# CakePHP app schema with sample data ready for baking

This app can be used for benchmarking, testing, debugging etc. on CakePHP 1.3.x and CakePHP 2.x

Quickly bake sample application with following tables and number of inserted rows:

    'blogs'=>6, 'categories' =>50, 'comments'=>2000, 'languages'=>1,'posts'=>1000,
    'posts_tags'=>2000, 'profiles'=>1000, 'tags'=>1000, 'users'=>1000


## Usage

1. Install fresh copy of CakePHP.
2. Configure database in "app/config/database.php".
3. Browse to homepage and confirm Cake install check (all green). Make sure "app/tmp" folder is writable (and subfolders).
4. Copy provided schema.php to "app/config/schema" folder.
5. Configure CakePHP console.
6. Run in console "cake schema create app". Wait for a minute until all records are inserted.
7. Run in console "cake bake all". Repeat for all available models.
8. All done, now browse to "/posts".

For benchmarking, edit "app/config/core.php" and change "Configure::write('debug', 0);" to enable cache.

## Requirements

    PHP version: PHP 5.2+
    CakePHP version: 1.3, 2.x
