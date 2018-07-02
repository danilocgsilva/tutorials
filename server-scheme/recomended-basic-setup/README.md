
# Recomended Basic Setup

There are two different servers: the application server and the database server.
The application communicates with the database through a TCP connection from another server. This way, we have a *realiability layer*. You specialize a server setup just for application, and another server setup just for database. Putting the same server to deal both with application and the database can open security issues, let the server maintenance harder, have less flexibility and exposes the data in case of server attack.

## Offline Backuping

You may have a script in the application server to pack all application and also the database. Put them in different directories and them fetches from development machine or throw to some backup drive.