## Ansible Project – Web Application Automation

This repository contains a collection of Ansible playbooks and roles to automate the setup of different components of a web application stack.

It includes roles for Apache, PHP, HTML, Angular and supporting playbooks to demonstrate single plays, multi-plays, dynamic/static configuration and app deployments.

### Roles

- Apache – Installs and configures Apache web server.

- PHP – Installs PHP and dependencies.

- HTML – Deploys static HTML content.

- Angular – Deploys Angular application.

Each role contains:

- tasks/ → main tasks

- vars/ → variables

- files/ and templates/ → assets and configs

### Notes

- 09-static.yml and 10-dynamic.yml demonstrate static vs dynamic inventory usage.

- dynamic.j2 is a Jinja2 template to help generate inventory dynamically.

- Maintenance.html and static.html are sample app pages deployed via playbooks.
