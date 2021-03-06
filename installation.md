# Installation

- [Installation](#installation)
    - [Server Requirements](#server-requirements)
    - [Installing Mage2 E cimmerce](#installing-mage2-ecommerce)

<a name="installation"></a>
## Installation
> 
<a name="server-requirements"></a>
### Server Requirements

The Mage2 E commerce framework has a few system requirements.

Below is the list which you will need to make sure your server meets the following requirements:


* PHP >= 7.1.3
* OpenSSL PHP Extension
* PDO PHP Extension
* GD Library (Image Processing)
* Mbstring PHP Extension
* Tokenizer PHP Extension
* XML PHP Extension
* Ctype PHP Extension
* JSON PHP Extension
* Curl PHP Extension


<a name="installing-mage2-ecommerce"></a>
### Installing Mage2 E commerce

Mage2 E commerce utilizes [Composer](https://getcomposer.org) to manage its dependencies. So, before using Mage2 E commerce, make sure you have Composer installed on your machine.

#### Via Composer Create-Project

Alternatively, you may also install Laravel by issuing the Composer `create-project` command in your terminal:

    composer create-project mage2/laravel-ecommerce --stability=dev

#### Set up your Envirionment(.env) file

    laravel-ecommerce/.env 
    
### Go to Url
    
    yoursite.com/install
    
That's it!

#### Directory Permissions

After installing Mage2 E commerce, you may need to configure some permissions. Directories within the `storage` and the `public/uploads` directories should be writable by your web server or Mage2 E commerce will not run. 

#### Application Key

The next thing you should do after installing Mage2 E commerce is set your application key to a random string. If you installed Mage2 E commerce via Composer, this key has already been set for you by the `php artisan key:generate` command.

Typically, this string should be 32 characters long. The key can be set in the `.env` environment file. If you have not renamed the `.env.example` file to `.env`, you should do that now. **If the application key is not set, your user sessions and other encrypted data will not be secure!**

