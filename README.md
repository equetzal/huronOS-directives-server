## huronOS Directives Server

The huronOS Directives Server is intend to be the platform to control instances of huronOS. Currently this server still not developed as the main system (the distribution) still needing to reach maturity.

## Current work

Because this server will require a bigger engineering effort, huronOS project opted for a simple synchronization method. This is, a directives file which will be polled every 1 minute by all the instances of huronOS.

When huronOS installer asks for a URL of a directives server, it will start polling that file every 1 min. This file needs to be available over HTTP or HTTPS to be downloaded and checked. It is not necessary to use the [directives.huronos.org](https://directives.huronos.org), but if you need to, we can provide you with an SSH access to a directory inside our webserver to host your directives files.

## Target work

Ideally, huronOS directives server will have 2 parts, a _Manager Front-End_ and the _Directives API_. On the frontend you'll be able to create a new _Room_, which will generate a unique code for that room, which will be configurable on huronOS at installation (with possibility of change it later), so that the huronOs installation instance get linked with that room. With this front end the manager will be able to edit, and personalize all the behavior of the room without needing to touch the directives file.

On the _Directives API_, all the communication between huronOS and the server will be performed
