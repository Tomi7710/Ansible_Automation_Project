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

### Tech Stack
- Web Server: Apache HTTP Server (apache role, 03-httpd.yml).

    Purpose: Handles HTTP requests and serves web content.

- Application Server / Backend: PHP (php role, 13-phpapp.yml)

    Purpose: Runs server-side code, handles business logic, processes requests.

- Frontend / Client Layer: HTML (html role, 12-htmlapp.yml); Angular (angular role, 14-angularapp.yml)

    Purpose: User interface (HTML, CSS, JavaScript) that runs in the browser.

- Static Files / Assets: files/ folder in roles; templates/ folder for Jinja2 templates; static.html, Maintenance.html

    Purpose: Images, CSS, JS files, templates, configuration files.

Configuration & Inventory: hosts.ini (static inventory); dynamic.j2 (template for dynamic inventory); Variables in tasks/main.yml or vars/main.yml

Purpose: Define which servers to deploy to and how to configure them.

### Notes

- 09-static.yml and 10-dynamic.yml demonstrate static vs dynamic inventory usage.

- dynamic.j2 is a Jinja2 template to help generate inventory dynamically.

- Maintenance.html and static.html are sample app pages deployed via playbooks.
