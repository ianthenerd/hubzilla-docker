# Hubzilla Docker image

This is the packaging of [hubzilla](https://framagit.org/hubzilla/core) as a [docker image](https://hub.docker.com/r/sebt3/hubzilla) based on php:8.1-fpm-alpine for amd64.

## Supported environnement variables:

| Variable            | Default                           | Description                                                                                                                          |
| ------------------- | --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| DB_TYPE             | postgres                          | Database type : postgres or mysql                                                                                                    |
| DB_HOST             | postgres                          | Host name of the database                                                                                                            |
| DB_PORT             | 5432                              | Database port number, set empty to use the default of your DB_TYPE (aka 3306 for mysql)                                              |
| DB_NAME             | hub                               | Database name                                                                                                                        |
| DB_USER             | hubzilla                          | Database user to connect to                                                                                                          |
| DB_PASSWORD         | hubzilla                          | Database user password                                                                                                               |
| SMTP_HOST           | smtp.domain.com                   | Mail server hostname                                                                                                                 |
| SMTP_PORT           | 587                               | Mail server port number                                                                                                              |
| SMTP_USER           | user                              | User name for the mail server                                                                                                        |
| SMTP_DOMAIN         | domain.com                        | Mail domain                                                                                                                          |
| SMTP_PASS           | password                          | Password for the user on the mail server, if set empty, then no authentication on the smtp server will be used                       |
| HUBZILLA_DOMAIN     | domain.com                        | Web domain name for hubzilla                                                                                                         |
| HUBZILLA_ADMIN      |                                   | email address of this hubzilla administrator (you)                                                                                           |
| REDIS_PATH          |                                   | If set (to something like " tcp://redis") then php sessions will be stored in this redis server (usefull for horizontal scalability) |
| LDAP_SERVER         |                                   | LDAP server name without ldap:// (dont forget to add "ldapauth" to the ADDON_LIST)                                                                  |
| LDAP_ROOT_DN        |                                   | LDAP username to connect to (e.g.: cn=admin,dc=domain,dc=com)                                                                          |
| LDAP_ADMIN_PASSWORD |                                   | Password for that LDAP user                                                                                                          |
| LDAP_BASE           |                                   | Path to look for users in the directory (e.g.: ou=people,,dc=domain,dc=com)                                                            |
| LDAP_ADMIN_PASSWORD |                                   | Password for that LDAP user                                                                                                          |
| LDAP_USERATTR |                                   | LDAP user attribute that user accounts will be based on (e.g: sAMAccountName)                                                                                                          |
| LDAP_GROUP |                                   | LDAP group distinguished name all users must be members of (e.g. CN=Hubzilla Users,CN=Users,DC=domain,DC=com)              |
| ADDON_LIST          | nsfw superblock diaspora pubcrawl | Addons to activate during initial configuration                                                                                      |

## Usage

Please see the [install directory](https://github.com/ianthenerd/hubzilla-docker/tree/master/install) for usage examples.
