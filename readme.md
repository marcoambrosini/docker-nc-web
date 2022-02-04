# Spin this up

- [Install Docker](https://docs.docker.com/get-started/)

- [Install docker-compose](https://docs.docker.com/compose/install/)

- Clone this repository


```
git clone https://github.com/marcoambrosini/docker-nc-web.git
```

- Clone the nextcloud website repository

```
cd docker-nc-web
git clone https://github.com/nextcloud/nextcloud.com.git
``` 

- Build the stack

```
sudo docker-compose up -d
```

- Copy the config.php
​
```
docker-compose exec wordpress cp wp-content/themes/next/config.php.sample wp-content/themes/next/config.php
```

- Access the site at [localhost:8084](http://localhost:8084)

- Activate the "next" theme in Appearance -> Themes

- Import the website content.xml file
  * First install the Wordpress Import Plugin (via Tools -> Import -> Wordpress Import -> Install Plugin)
  * Select the content.xml file from the repository and click upload
  * Select Import

- Useful commands:
	Open a shell in the wordpress container
	```
	docker-compose exec wordpress sh
	```
