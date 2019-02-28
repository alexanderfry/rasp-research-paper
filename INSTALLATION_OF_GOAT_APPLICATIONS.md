# Installation of Goat Applications

## NodeGoat

NodeGoat can be downloaded from *https://github.com/OWASP/NodeGoat*. The
options to run NodeGoat include: one click install on Heroku, install
from sources on local machine or using a Docker container. First,
Node.js v8.11.1 was installed from
[*https://nodejs.org*](https://nodejs.org). Next, the sources were
downloaded from GitHub with the command ```git clone
<https://github.com/OWASP/NodeGoat>```. After changing to the NodeGoat
directory, the node modules were installed with the command ```npm
install```. NodeGoat uses a MongoDB database. The options to install this
database include: local installation or install a sandbox version at
[*https://mlab.com*](https://mlab.com). After creating an account on
[*https://mlab.com*](https://mlab.com), a sandbox MongoDB database and
database user were created. The local db property in file
*config/env/development.js* was updated to reflect the database name and
user in the format:
*mongodb://\<username\>:\<password\>@\<databasename\>*. The
configuration for the NodeGoat database was
*mongodb://mongo:mongo1\@ds151382.mlab.com:51382/mongo\_nodegoat*. Then
the database was seeded by running the command ```npm run db:seed```. And
*npm* was started with the command ```npm start```, both run in the Mac OS X
Terminal application (Figure 1).

![](images/NG_Running_NodeGoat_on_the_Command_line_Figure_1.png)
Figure 1. Running NodeGoat on the Command Line

## WebGoat

WebGoat can be downloaded from *https://github.com/WebGoat/WebGoat*. The
options to run WebGoat include: standalone from a pre-compiled jar file,
using a Docker container or compiling a new jar from the sources.
WebGoat was compiled from the sources in order to introduce a new
vulnerable lesson. However, initially WebGoat was run from the
standalone release v8.0.0.M21 under Java version 1.8.0\_171\_b11 on Mac
OS X v10.13.6 with the following options in the Terminal application:
```java -jar webgoat-server-8.0.0.M21.jar --server.port=9080 --server.address=127.0.0.1``` (Figure 2).

![](images/WG_Running_WebGoat_Command_Line_Figure_2.png)
Figure 2. Running WebGoat on the Command Line
