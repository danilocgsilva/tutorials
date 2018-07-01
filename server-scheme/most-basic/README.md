# Most basic

The most basic scheme shows the first ever and most simple server setup.
In this case, the same machine is responsible to serve the dynamic html, the frontend assets, like javascript and css, and also the media files. In this cenario, the resource are shared by three kinds of content. The machine uses the same resources, like processing power, memory and even network to serves all contents.
This setup may be the used for offline development machine, for simple shared hosting services or even for simple setup for clould machine. WordPress, Drupal, Symfony and Laravel may be examples of web applications the will uses this setup.

## Offline Backuping

### If your application server is not under a control version software in the production

The simplest setup also means the simplest way to backup the system. You can run in the machine a script that will pack at once all three kinds of contents. More simple web applications (or web applications with a simple schema, not meaning that the application itself is simple) also may have a *central folter* where everything are. No need for network content fetching. Everything can be packed in a file inside the machine itself and fetched to the development machine or to a more suitable place for offline backuping.

### If the application code in the server is controlled by a control version software

You may have to worry about what version is running in the server. Just needs to backup the database, and know which version of the code are running when making the backup. If your application have compiled code, also marks the webserver software setup, like version and modules running in the application, because it may impact with the final compiled running program.