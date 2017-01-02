# docker-ubuntu16-nginx-php7
A docker image based on Ubuntu 16.04 with Nginx + PHP 7.0 (FPM) that uses supervisor as process manager.

## Building

For building the image from source, clone the repository and run docker build

```
git clone https://github.com/franCarmona/docker-ubuntu16-nginx-php7.git
docker build -t nginx-php7 .
```

## Running

After building the image, run the container.
```
docker run --name nginx-php7-fpm -v ~/path/to/code:/var/www/html -d -p [host-port]:80 nginx-php7
```
Browse to [http://localhost:[host-port]](http://localhost:[host-port]) to view your app.

## Using as a base image [TODO]

Overwrite nginx config files,....

## Exposed ports

80 (http). HTTPS is not enabled in this image.

## Exposed volumes

 - webroot: `/var/www/html`
 
## Out of the box

 * Ubuntu 16.04 LTS
 * Nginx
 * PHP7
 * Git
 * Composer
