# Multi-Tier Architecture

## Two-Tier Architecture

A two-tier architecture is a system divided into two separate layers: the Web/Application Tier and the Database Tier. In this laboratory, Nextcloud serves as the Web/Application Tier while MariaDB serves as the Database Tier. The two containers communicate with each other through Docker Compose.

## The Web/Application Tier

The Web/Application Tier is responsible for providing the user interface and handling HTTP requests from users. In this laboratory, the Nextcloud container provides the private cloud storage web application that users access through a web browser.

## The Database Tier

The Database Tier is responsible for storing persistent data required by the application. In this laboratory, MariaDB stores information such as user accounts and file metadata used by Nextcloud.

## Why Separate Them?

Separating the web application and database into two containers makes the system easier to manage and organize. Each container has a specific responsibility, allowing the application and database to be maintained separately while still communicating with each other.

