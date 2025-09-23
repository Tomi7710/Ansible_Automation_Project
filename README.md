## Ansible Project – Web Application Automation

This repository contains a collection of Ansible playbooks and roles to automate the setup of different components of a web application stack.

It includes roles for Apache, PHP, HTML, Angular and supporting playbooks to demonstrate single plays, multi-plays, dynamic/static configuration and app deployments.

## Highlights

Frontend: HTML + Angular, **deployed via automation**.

Backend: PHP, **standardized and repeatable deployment**.

Web Server: Apache, **managed consistently across servers**.

Assets: Static files and templates, **allowing configuration as code**.

Deployment: **Ansible playbooks and inventory provide fully automated, idempotent deployments suitable for CI/CD pipelines**.

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
- Web Server: Handles HTTP requests and serves web content.
  - Apache HTTP Server (apache role, 03-httpd.yml).

- Application Server / Backend: Runs server-side code, handles business logic, processes requests.
  - PHP (php role, 13-phpapp.yml)

- Frontend / Client Layer: User interface that runs in the browser.
  - HTML (html role, 12-htmlapp.yml)
  - Angular (angular role, 14-angularapp.yml)

- Static Files / Assets: Templates, configuration files.
  - files/ folder in roles
  - templates/ folder for Jinja2 templates
  - static.html, Maintenance.html

- Configuration & Inventory: Define which servers to deploy to and how to configure them.
  - hosts.ini (static inventory)
  - dynamic.j2 (template for dynamic inventory)
  - Variables in vars/main.yml

### Notes

- 09-static.yml and 10-dynamic.yml demonstrate static vs dynamic inventory usage.

- dynamic.j2 is a Jinja2 template to help generate inventory dynamically.

- Maintenance.html and static.html are sample app pages deployed via playbooks.

### Getting Started

```bash
git clone <repo-url>
cd ansible-work-6
ansible-playbook -i hosts.ini 02-multi-play.yml
