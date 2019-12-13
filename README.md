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

| Variable                     | Default value | Comments (type)                                  |
| :--------------------------- | :------------ | :----------------------------------------------- |
| `bitwarden_http_port`        | `80`          | Port to access bitwarden over HTTP               |
| `bitwarden_https_port`       | `443`         | Port to access bitwarden over HTTPS              |
| `bitwarden_installation_id`  | `[]`          | Unique bitwarden installation id (**required**)  |
| `bitwarden_installation_key` | `[]`          | Bitwarden installation key (**required**)        |
| `bitwarden_hostname`         | `[]`          | Hostname for the bitwarden server (**required**) |
| `identitypassword`           | `[]`          | Password for identity server (**required**)      |

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

Maarten Beeckmans and Stijn Van De Moortele
