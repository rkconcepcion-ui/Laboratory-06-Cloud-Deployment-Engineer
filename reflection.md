# Mission 6 Reflection

This mission helped me understand how Docker Compose can make cloud deployment easier and more organized. Writing a `docker-compose.yml` file allows a cloud engineer to define multiple containers and their settings in one configuration file. Instead of manually typing many commands for each container, the engineer can use one command such as `docker-compose up -d` to deploy the whole application. This makes the deployment process faster, more consistent, and easier to repeat.

I also learned that YAML is sensitive to indentation. An indentation error, such as using a Tab instead of spaces or placing a line at the wrong level, can cause the Compose file to fail. I experienced this while creating my own file because incorrect indentation resulted in a YAML parser error. After correcting the spacing, the configuration was accepted successfully. This showed me why careful formatting is important when working with Infrastructure as Code.

Environment variables such as `MYSQL_PASSWORD`, `MYSQL_DATABASE`, and `MYSQL_USER` were used to provide configuration information to the containers. They allow the Nextcloud application and MariaDB database to use the required settings without placing those values directly into application code. I also learned how `MYSQL_HOST=database` allows Nextcloud to find and communicate with the MariaDB container.

Deploying Nextcloud and MariaDB in just a few minutes was a useful experience because it showed me how quickly cloud technologies can create a working service. Seeing both containers running and accessing the Nextcloud setup page made the concepts more practical.

Since Mission 1, my understanding of Cloud Computing has developed from learning basic cloud concepts to actually deploying and managing cloud-based services. I now have a better understanding of containers, networking, storage, databases, Docker, and Infrastructure as Code. This mission showed me how these concepts can work together to create a multi-tier cloud application.

