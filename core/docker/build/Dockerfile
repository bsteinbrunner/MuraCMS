FROM blueriver/lucee:5.2.7.23-SNAPSHOT.3

# Provide app
RUN mkdir -p /var/www
RUN mkdir -p /var/www/etc
RUN mkdir -p /var/www/plugins

# Rewrite rules
COPY core/docker/build/urlrewrite.xml /var/www/etc/urlrewrite.xml

# Logs
RUN ln -sf /dev/stdout /opt/lucee/web/logs/application.log \
	&& ln -sf /dev/stdout /opt/lucee/web/logs/exception.log

# Copy Mura files
COPY . /var/www
