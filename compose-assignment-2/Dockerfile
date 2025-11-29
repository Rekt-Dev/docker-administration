# create your custom drupal image here, based of official drupal



# Fix apt-get for old Debian Jessi
FROM drupal:8.2

# Use archived Jessie repos and disable signature checks
RUN sed -i 's|http://deb.debian.org/debian|http://archive.debian.org/debian|g' /etc/apt/sources.list && \
    sed -i 's|http://security.debian.org|http://archive.debian.org|g' /etc/apt/sources.list && \
    apt-get -o Acquire::Check-Valid-Until=false -o Acquire::AllowInsecureRepositories=true update && \
    rm -rf /var/lib/apt/lists/*

RUN apt-get update \
	&& rm -rf /var/lib/apt/lists/*

WORKDIR /var/www/html/themes

RUN git clone --branch 8.x-3.x --single-branch --depth 1 https://git.drupal.org/project/bootstrap.git && chown -R www-data:www-data botstrap

WORKDIR /var/www/html
