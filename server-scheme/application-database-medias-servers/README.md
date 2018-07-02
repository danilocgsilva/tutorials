# Application Database Medias servers

Think a large WordPress, Drupal or any other PHP application that holds lots of medias and needs to have an optimal setup.
We can have three different and dedicated servers: one for application, another for the relational database and the last one for medias. Making different servers for application and database are a good practice to strength the database security and gain flexibility. And for media server, it may needs have a very large space, but does not requires huge processing power, beign a strategy for cost efficiency, once the space for serve static files is much more cheap than the space for a dynamic content. Usually, the media also requires a much larger space.

## Offline Backuping

Run a script in the application server to pack the database. Them from the development machine, fetches both the content of application and the database backup. Does not open a large time windown between the database backuping in the server and the files fetching. Finally, as the next step from the same backup proccess, downloads all contents from your media server. Packs everything toghether.