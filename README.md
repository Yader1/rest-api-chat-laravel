<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## Project settings
To configure this project in your local service follow the following steps:

- [Install composer](https://getcomposer.org/).
- [Install Laravel with php](https://laravel.com/).
- Create an account or if you have one, a project in [PUSHER](https://dashboard.pusher.com/), specifically create a channel.
- Run the `php artisan migrate` command to create the database tables. It is worth mentioning that you must have your env, credentials and the database where the tables will be created.
## Requests that can be consulted to the rest api.
```
GET|HEAD   /
  POST       api/auth/login ........ auth.login › AuthController@login
  POST       api/auth/login_with_token auth.login_with_token › AuthCo…
  GET|HEAD   api/auth/logout ..... auth.logout › AuthController@logout
  POST       api/auth/register auth.register › AuthController@register
  GET|HEAD   api/chat .............. chat.index › ChatController@index
  POST       api/chat .............. chat.store › ChatController@store
  GET|HEAD   api/chat/{chat} ......... chat.show › ChatController@show
  GET|HEAD   api/chat_message chat_message.index › ChatMessageControl…
  POST       api/chat_message chat_message.store › ChatMessageControl…
  GET|HEAD   api/user .............. user.index › UserController@index
```
## Examples:
${\textsf{\color{orange}POST -> Resgister}}$
```
    {{base_url_api}}/auth/register
    BODY -> Form-data
    email = ''
    password = ''
    password_confirmation = ''
```
${\textsf{\color{orange}POST -> Login}}$
```
    {{base_url_api}}/auth/login
    BODY -> Form-data
    email = ''
    password = ''
```
${\textsf{\color{orange}POST -> Login with token}}$
```
    {{base_url_api}}/auth/login_with_token
    Authorization -> Token
    {{token}}
```
${\textsf{\color{lightgreen}GET -> Logout}}$
```
    {{base_url_api}}/auth/logout
    Authorization -> Token
    {{token}}
```
${\textsf{\color{orange}POST -> Create Chat}}$
```
    {{base_url_api}}/chat?user_id=
    Authorization -> Token
    {{token}}
```
${\textsf{\color{lightgreen}GET -> Many Chats}}$
```
    {{base_url_api}}/chat
    Authorization -> Token
    {{token}}
```
${\textsf{\color{lightgreen}GET -> Single Chat}}$
```
    {{base_url_api}}/chat/?chat_id=1
    Authorization -> Token
    {{token}}
```
${\textsf{\color{lightgreen}GET -> Chat Message}}$
```
    {{base_url_api}}/chat_message?chat_id=1&page=1
    Authorization -> Token
    {{token}}
```
${\textsf{\color{orange}POST -> Create Chat Message}}$
```
    {{base_url_api}}/chat_message
    BODY -> Form-data
    chat_id = 
    message = ''
    Authorization -> Token
    {{token}}
```
${\textsf{\color{lightgreen}GET -> Users}}$
```
    {{base_url_api}}/user
    Authorization -> Token
    {{token}}
```
