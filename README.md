# Ansible Role: Apache 2.x

[![CI](https://github.com/BenLee83/RHEL_post_patch_validation/workflows/CI/badge.svg?event=push)](https://github.com/BenLee83/RHEL_post_patch_validation/actions?query=workflow%3ACI)

An Ansible Role that checks Server Stack (following patch maintenance).

## Requirements

If you are using SSL/TLS, you will need to provide your own certificate and key files. You can generate a self-signed certificate with a command like `openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout example.key -out example.crt`.

## Dependencies

None.

## Example Playbook

    - hosts: webservers
      vars_files:
        - vars/main.yml
      roles:
        - { role: geerlingguy.apache }

*Inside `vars/main.yml`*:

    apache_listen_port: 8080
    apache_vhosts:
      - {servername: "example.com", documentroot: "/var/www/vhosts/example_com"}

## License

MIT / BSD

## Author Information

This role was created in 2020 by [Ben Lee]
