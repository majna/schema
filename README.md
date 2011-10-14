# CakePHP app schema for Sample Blog Application

Useful when learning CakePHP, for benchmarks, tests, debugging and more.

All you need is to copy schema.php to APP/Config/Schema and run cake console task.

Following tables (and number of inserted rows) will be created (can be configured in schema file):

	blogs: 6, 
	categories: 50, 
	comments: 2000, 
	languages: 1,
	posts : 1000,
	posts_tags : 2000,
	tags : 1000, 
	users : 1000

It tries to match data values for name, date, email address, title, post etc.

## Usage

1. Install fresh copy of CakePHP (1.3.x or 2.x)
2. Configure database in "APP/Config/database.php".
3. Browse to home page and confirm Cake setup checks.
4. Copy provided schema.php to "APP/Config/Schema" folder.
5. Configure and run CakePHP console: 

    `cake schema create app` Wait for a minute until all records are inserted.
    `cake bake all` Repeat for all available models.

All done, now browse to "/posts".

If benchmarking, disable debug mode: edit `app/Config/core.php` and change `Configure::write('debug', 0);`


## Example of few  records created in table 'users':

	id: 1
	name: Eleifend Vivamus
	email: proin@example.com
	password: db6ff2ffe2df7b8cfc0d9542bdce27dc
	phone: 4624-8435
	mobile_phone: 2078-8235
	address: Sit orci amet
	city: Sociis
	postcode: 8561
	web: http:/www.fermentum.com
	created: 2011-05-15 22:01:01
	modified: 2011-07-13 20:31:06

	id: 2
	name: Risus Proin
	email: fringilla@example.com
	password: c3d32ae7ad6a5d450756a7d96b2a2a21
	phone: 4624-8435
	mobile_phone: 2078-8235
	address: Sit orci amet
	city: Morbi
	postcode: 8561
	web: http:/www.fermentum.com
	created: 011-08-15 23:30:16
	modified: 2011-09-05 09:31:26

## Example of created records in table 'posts':

It will assign few tags and comments to each Post and pick a random category and blog.

	id: 1
	category_id: 48
	title: Quam nisl lacinia
	description: Tincidunt nisi nascetur mollis vitae vel mus quam mperdiet dis Vivamus libero.
	body: Urna tortor dapibus consectetur sit nisl interdum placerat ipsum pellentesque dictum tortor orci pulvinar 
		qegestas varius fringilla at adipiscing parturient congue risus Donec aliquet velit mus consectetur consequat
		imperdiet eleifend mauris sed blandit lacus eleifend est Proin quis nisi mollis Cum sociis Donec vestibulum 
		posuere sodales quam vitae ante magnis Maecenas tincidunt consectetur Phasellus sagittis sed Lorem tincidunt 
		lacinia turpis elit Quisque congue congue libero amet congue sed urna vitae nisi ipsum tristique Integer montes leo.
	created: 2011-07-15 02:12:36
	modified: 2011-09-15 23:30:19
	featured: 0
	published: 1
	blog_id: 4


	id: 2
	category_id: 36
	title: Tristique Aenean erat
	description: Aenean ipsum leo nibh posuere nascetur venenatis at malesuada vestibulum ligula euismod.
	body: Dictum imperdiet nisi Quisque Donec tristique sit malesuada diam Proin ligula sodales magnis sagittis
		pulvinar at ante consectetur consequat venenatis ullamcorper quam orci sit amet congue blandit dignissim 
		posuere vestibulum congue amet tortor penatibus Aenean congue placerat sollicitudin velit lacinia Morbi.
	created: 2011-07-15 21:34:46
	modified: 2011-09-05 10:11:06
	featured: 1
	published: 1
	blog_id: 5


### Requirements

    PHP version: PHP 5.2+
    CakePHP version: 1.3, 2.x
