# Spin this up
​
- [Install docker-compose](https://docs.docker.com/compose/install/)
​
- Clone this repository


```
git clone https://github.com/ma12-co/docker-nextcloud-website.git
```

- Clone the nextcloud website repository

```
cd docker-nc-web
git clone https://github.com/nextcloud/nextcloud.com.git
``` 

- Build the stack

```
docker-compose up -d
```

- Copy the config.php
​
```
docker exec -it docker-nextcloud-website_wordpress_1 cp wp-content/themes/next/config.php.sample wp-content/themes/next/config.php
```

- Access the site from [localhost:8084/wp-admin](http://localhost:8084/wp-admin)

- Activate the "next" theme in Appearance -> Themes

- Import the website content.xml file
  * First install the Wordpress Import Plugin (via Tools -> Import -> Wordpress Import -> Install Plugin)
  * Select the content.xml file from the repository and click upload
  * Select Import

