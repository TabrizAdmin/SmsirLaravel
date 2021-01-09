<p align="center"><img src="https://www.sms.ir/wp-content/themes/sms.ir/assets/img/final-sms-logo.png"></p>

<p align="center">Official Laravel Package for sms.ir</p>

[![Latest Stable Version](https://poser.pugx.org/tabrizadmin/smsirlaravel/v/stable)](https://packagist.org/packages/tabrizadmin/smsirlaravel)
[![Total Downloads](https://poser.pugx.org/tabrizadmin/smsirlaravel/downloads)](https://packagist.org/packages/tabrizadmin/smsirlaravel)
[![Monthly Downloads](https://poser.pugx.org/tabrizadmin/smsirlaravel/d/monthly)](https://packagist.org/packages/tabrizadmin/smsirlaravel)
[![License](https://poser.pugx.org/tabrizadmin/smsirlaravel/license)](https://packagist.org/packages/tabrizadmin/smsirlaravel)



<a align="center" href="https://www.sms.ir/%D8%AE%D8%AF%D9%85%D8%A7%D8%AA/%D9%88%D8%A8-%D8%B3%D8%B1%D9%88%DB%8C%D8%B3/%D8%A7%D8%B1%D8%B3%D8%A7%D9%84-%D9%BE%DB%8C%D8%A7%D9%85%DA%A9-laravel/">آموزش فارسی نصب و استفاده از پکیج ارسال پیامک لاراول</a>



Hi, if you have an account in sms.ir, you can use this package for laravel

----------


How to install:
-------------

    composer require tabrizadmin/smsirlaravel:dev-master
    php artisan vendor:publish
    php artisan migrate

> **Setup:**

add this line to your app.php providers:
tabrizadmin\smsirlaravel\SmsirlaravelServiceProvider::class,

and add this line to your app.php aliases:
'Smsirlaravel' => tabrizadmin\smsirlaravel\SmsirlaravelFacade::class,


> After publish the package files you must open smsirlaravel.php in config folder and set the api-key, secret-key and your sms line number.
>

> **Like this:**

	'webservice-url' => env('SMSIR-WEBSERVICE-URL','https://ws.sms.ir/'),
	'api-key' => env('SMSIR-API-KEY','Your sms.ir api key'),
	'secret-key' => env('SMSIR-SECRET-KEY','Your sms.ir secret key'),
	'line-number' => env('SMSIR-LINE-NUMBER','Your sms.ir line number'
>
> Note:

you can set the keys and line number in your .env file

> **like this:**

> SMSIR-WEBSERVICE-URL=https://ws.sms.ir/

> SMSIR-API-KEY=your api-key

> SMSIR-SECRET-KEY=your secret-key

> SMSIR-LINE-NUMBER=1000465******



Methods:
-------------

> Smsirlaravel::send()

> Smsirlaravel::credit()

> Smsirlaravel::getLines()

> Smsirlaravel::addToCustomerClub()

> Smsirlaravel::deleteContact();

> Smsirlaravel::sendToCustomerClub();

> Smsirlaravel::addContactAndSend();

> Smsirlaravel::sendVerification();

> Smsirlaravel::ultraFastSend();

> Smsirlaravel::getSentMessages();

> Smsirlaravel::getReceivedMessages();
