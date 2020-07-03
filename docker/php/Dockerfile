FROM php:7.3-alpine
WORKDIR /usr/src/toggly

# Update certificates.
RUN apk update && apk add ca-certificates && rm -rf /var/cache/apk/*

# Install composer
RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" \
	&& php composer-setup.php --install-dir=/usr/bin --filename=composer \
	&& php -r "unlink('composer-setup.php');"
