| Issue |  #10 |
| ----- | --- |
| author       | Michael Stöger @11778261 |
| released by  | Nicolas Griebenow @01617265 |
| release date | 2020-10-19 |

# Architecture
Most of this software's architecture can be described as client-server three tier architecture.
The frontend part connects over a network connection to a backend server, serving and collecting data.
The backend server will be implemented as a REST-server collecting data from the frontends and serving application data to them.
Separately there will be a webserver that serves the web based frontend.
These two servers will not have to run on the same machine, but can be running e.g. in different datacenters.
To access the web frontend a modern webbrowser like Firefox or Chromium will be required. 
Additionally, there will be an Android App, only using the backend REST server for data.

#### REST-Backend:
The REST backend will be built using [Spring](https://spring.io/projects/spring-framework).
Spring is a Java framework that can be used to build REST backends.
Because of its long development history it can be considered stable, and it is not expected that development will stall anytime soon.
Spring has many active users, so it is mostly easy to find solutions if problems occur during development of our application.

##### Storage:
Application data will be stored in a [H2 database](http://www.h2database.com) running within the Spring backend.
By using H2 it will be easier to set up the system, since it does not need to be installed.
All configuration will be managed by our application, users will have no influence on it.
To aid with development Hibernate will be used.
This allows for simple and clear communication with our persistence layer and helps to produce clean and maintainable code.
Still one exception exists to this storage concept.
The 3D-models, used for the Android AR feature, will be stored on a web server, because the file size and type are not suitable for a relational database.
Needed models can be quickly downloaded on demand, when a user starts the AR feature.

#### Web-based frontend
For the web-based frontend [Angular](http://www.angular.io) will be used.
In combination with [Bootstrap](https://getbootstrap.com) it is quick and easy to develop good-looking modern frontends which are compatible with our target platforms.
As it is developed by Google and used by many projects today, it can be considered stable and well documented. 

#### Android App
The Android App should act as another frontend besides the web frontend, but it will have a different feature set.
Not all features implemented on the web application will be available on Android too, but therefore the Android App will support augmented reality.
Using Google's [ARCore](https://developers.google.com/ar/discover) library 3D-models of animals should be projected into the customer's homes.
With this feature our target platforms are modern powerful phones that can handle the 3d load.
Because of that only phones running Android 9 and newer will be supported.
Google services are required for the AR features to run.

#### General notes
For all used software and libraries the current stable and non development version will be used.
That way the most modern features can be used without any major risk of security incidents or bugs that may appear in bleeding edge releases.
Also features marked as deprecated must not be used to avoid conflicts and problems when dependencies get updated.

![ComponentDiagram](uploads/6e419116f91b44612e9a195a9c342b5c/ComponentDiagram.png)