




![](/luv2code-ecom-angular-spring/assets/Screenshot-2025-06-13-160430.png)

![](/luv2code-ecom-angular-spring/assets/Screenshot-2025-06-13-160519.png)

![](/luv2code-ecom-angular-spring/assets/Screenshot-2025-06-13-160538.png)

![](/luv2code-ecom-angular-spring/assets/Screenshot-2025-06-13-160603.png)

![](/luv2code-ecom-angular-spring/assets/Screenshot-2025-06-13-160408.png)

![](/luv2code-ecom-angular-spring/assets/Screenshot-2025-06-13-160330.png)












```
344  sudo apt update
345  sudo apt search openjdk
346  sudo apt install openjdk-21-jdk
java --version
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
nvm --version
```

  
# mysql setup

* `sudo mysql -u root`







# start mysql
MySQL: localhost:3306
* `sudo service mysql start`

# start the backend
Backend: http://localhost:8080
* `cd 02-backend/spring-boot-ecommerce`
* `./mvnw spring-boot:run`

# start the frontend
http://localhost:4200
* `cd 03-frontend/angular-ecommerce`
* `ng serve`



# versions used
* `java --version`
    * ```
        openjdk 21.0.7 2025-04-15
        OpenJDK Runtime Environment (build 21.0.7+6-Ubuntu-0ubuntu124.04)
        OpenJDK 64-Bit Server VM (build 21.0.7+6-Ubuntu-0ubuntu124.04, mixed mode, sharing)
        ```
* `mvn --version`
    * ```
        openjdk 21.0.7 2025-04-15
        OpenJDK Runtime Environment (build 21.0.7+6-Ubuntu-0ubuntu124.04)
        OpenJDK 64-Bit Server VM (build 21.0.7+6-Ubuntu-0ubuntu124.04, mixed mode, sharing)
        ```
* `nvm --version`
    * `0.40.3`
* `npm --version`
    * `10.9.2`
* `node --version`
    * `v22.16.0`
* `mysql --version`
    * `mysql  Ver 8.0.42-0ubuntu0.24.04.1 for Linux on x86_64 ((Ubuntu))`