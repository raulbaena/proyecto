# Project
## Explanation
Dockerfile: File with the necessary parameters for the creation of the web server image
´´´
# Version: 1.0
# Linkia FP 2019-2020
# Raul Baena Nocea
# Servidor web proyecto
# -------------------------------------
FROM fedora:27
LABEL author="Raul Baena Nocea"
LABEL description="Servidor web detach"
RUN dnf -y install httpd
COPY index.html /var/www/html/
CMD ["/usr/sbin/httpd", "-D", "FOREGROUND"]
EXPOSE 80
´´´
index.html: Main web server file.

´´´
<html>

<head></head>

<body>
	<h1> Soy el servidor web de linkia </h1>

</body>

</html>
´´´
## Execute
´´´
docker run --rm --name http -h http -p 4000:80 -d raulbaena/http:server20
´´´
