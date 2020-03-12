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

