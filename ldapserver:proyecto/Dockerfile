#Version 1.0
# Servidor Ldap
# Raul Baena Nocea ASIX 2019-2020
# LINKIAFP
#---------------------------------
FROM fedora:27
LABEL author="Raul Baena Nocea"
LABEL description="Servidor LDAP"
RUN dnf -y install procps openldap-clients openldap-servers
RUN mkdir /opt/docker
COPY * /opt/docker/
RUN chmod +x /opt/docker/install.sh /opt/docker/startup.sh
WORKDIR /opt/docker
EXPOSE 389
CMD ["/opt/docker/startup.sh"]
