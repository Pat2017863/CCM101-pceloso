# Mission 6 Reflection

## 1. How Does Docker Compose Make a Cloud Engineer's Job Easier?

Docker Compose makes a cloud engineer's job easier because it allows multiple containers to be configured in one YAML file. Instead of typing many commands to start the application and database separately, I can use one command to deploy them together. It also makes the setup easier to repeat when the same application needs to be deployed again.

## 2. What Happens If There Is an Indentation Error in YAML?

Indentation is important in YAML because spaces determine how settings are grouped. If I use a tab instead of spaces or put a setting at the wrong level, Docker Compose may show an error or interpret the configuration incorrectly. I learned that checking the indentation before deploying can save time and prevent problems.

## 3. Why Did We Use Environment Variables?

Environment variables allow the containers to receive important configuration information, such as the database name, username, password, and database host. They help the application connect to the database without putting these values directly into the application code. However, real projects must protect sensitive credentials and avoid exposing them in public repositories.

## 4. How Did It Feel to Deploy Nextcloud in a Few Minutes?

Deploying Nextcloud with MariaDB helped me understand how powerful containerization can be. It was interesting to see how two separate services could work together as one application. I also learned that successful deployment requires checking container status, reading logs, and confirming that the website is accessible.

## 5. How Has My Understanding of Cloud Computing Changed Since Mission 1?

Since Mission 1, I have learned that cloud computing involves more than just using online storage or virtual machines. It also includes managing infrastructure, connecting services, automating deployments, and documenting configurations. This activity helped me understand Infrastructure as Code and how Docker Compose can make deployment more organized, consistent, and easier to maintain.
