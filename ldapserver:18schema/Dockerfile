# Version: 0.0.1
# edt M06 2018-2019
# ldapserver base edt.org
#-------------------------------------------------
FROM fedora:27
LABEL author="Raul edt ASIX m06 Curs 2018-2019"
LABEL description="ldapserver edt.org cn dataDB"
RUN dnf -y install procps openldap-clients openldap-servers
RUN mkdir /opt/docker
COPY * /opt/docker/
RUN cp /opt/docker/ldap.conf /etc/openldap/ldap.conf
RUN chmod +x /opt/docker/install.sh /opt/docker/startup.sh
WORKDIR /opt/docker
EXPOSE 389
CMD ["/opt/docker/startup.sh"]
