Bitwarden
=========

Install [Bitwarden's](https://bitwarden.com/) entire infrastructure on Linux.

Requirements
------------

* Ports 80 (http) and 443 (https) should be open.
* When you want to access Bitwarden from the outside world, their must be pointing a DNS record to your machine.
* Bitwarden Installation ID and Installation key are required (can be obtained from [bitwarden.com/host](https://bitwarden.com/host))
* Hostname is required, example: bitwarden.example.com or a ip address

Role Variables
--------------

| Variable                         | Default value | Comments (type)                                              |
| :------------------------------- | :------------ | :----------------------------------------------------------- |
| `bitwarden_http_port`            | `80`          | Port to access bitwarden over HTTP                           |
| `bitwarden_https_port`           | `443`         | Port to access bitwarden over HTTPS                          |
| `bitwarden_installation_id`      | `[]`          | Unique bitwarden installation id (**required**)              |
| `bitwarden_installation_key`     | `[]`          | Bitwarden installation key (**required**)                    |
| `bitwarden_hostname`             | `[]`          | Hostname for the bitwarden server (**required**)             |
| `bitwarden_identitypassword`     | `[]`          | Random generated password for identity server (**required**) |
| `bitwarden_sql_connectionstring` | `[]`          | Random generated password for SQL server (**required**)      |
| `bitwarden_identityKey`          | `[]`          | Random generated bitwarden identitykey (**required**)        |
| `bitwarden_duo_akey`             | `[]`          | Random generated bitwarden duo akey (**required**)           |
| `bitwarden_mail`                 | `[]`          | Reply_to mail for bitwarden (**required**)                   |
| `bitwarden_smtp_host`            | `[]`          | Bitwarden smtp host (**required**)                           |
| `bitwarden_smtp_port`            | `[587]`       | Bitwarden smtp port                                          |
| `bitwarden_smtp_ssl`             | `[false]`     | Bitwarden snmp ssl                                           |
| `bitwarden_smtp_username`        | `[]`          | Bitwarden snmp username (**required**)                       |
| `bitwarden_smtp_password`        | `[]`          | Bitwarden snmp password (**required**)                       |
| `bitwarden_UID`                  | `[]`          | Desired user id for running bitwarden under (**required**)   |
| `bitwarden_GID`                  | `[]`          | Desired group id for running bitwarden under (**required**)  |

Dependencies
------------

The required dependencies (docker, docker-compose and unzip) are installed by the role.

Example Playbook
----------------

Minimal required playbook:

```yml
  - hosts: servers
    roles:
        - { role: username.rolename, x: 42 }
```
License
-------

BSD

Author Information
------------------

Maarten Beeckmans and Stijn Van De Moortele
