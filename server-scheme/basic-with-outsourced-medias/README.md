# Basic with outsourced medias

This is also a very basic setup, but the medias have an exclusive server for them. This can be a strategy for efficiency of money saving.
Medias should be seem as a different kind of content. Medias are special, because:

1. The media content generally is much more large in terms of space than any other kind of content.
1. The media content is a static resource. There is no need for processing the media content.
1. Server may not make any decision based on presence or absence of medias. Server may even not know if the medias are there or not. The application may work seamlessly, with or without medias, although for user experience this may have negative impact.

The space reserved for application may be very expensive. So, having an separated webserver just to serve medias always is a very solid strategy for money saving. The processing power may not be a concern in the media webserver. Amazon S3 makes any concern about processing power for its instance, just the space, that is much more cheap. A large site may have tens or even hundreds of gigabytes of medias, if some social activity is taken. Otherwise, the application server leads an important concern about processing power and RAM amount, and less than 10 gigabytes would serve very well the application server, even for large projects.

## Offline Backuping

Your backup may be done in three steps:

### Step 1: Backups application code and database in the server

Packs together both files from the application and the database in single file in the server, them download them to the development machine or to any kind of backup drive.

### Step 2: Backups the media

You may needs to download the medias files directly from the media webserver to the development machine. Media webserver may have a more simple and restricted setup, so running a script inside the machine is not a reasonable way. The meida files may downloaded directly from the webserver to the development machine through TCP protocol.

### Step 3: Packs the application code and the medias together

In the development machine you will have both the application code backup and the medias backups. Pack them together and close your backup file.