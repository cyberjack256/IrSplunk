# Splunk Docker Deployment for Academic Exploration of Digital Forensics

This repository facilitates a straightforward setup to deploy a Splunk instance within a Docker container, tailored for incident response and forensic analysis. It incorporates a setup script for secure handling of the Splunk admin password and automatic configuration of indexes for various forensic artifacts.

## Features

- One-command deployment for ease of use.
- Secure password handling through Docker secrets.
- Pre-configured indexes suitable for forensic analysis.
- Customizable setup to cater to specific use cases.

## Prerequisites

- Docker and Docker Compose installed on the host machine.

## Quick Start

1. **Run the Setup Script:**
    Use this one-liner to fetch and run the setup script directly:
    ```bash
    bash <(curl -s https://raw.githubusercontent.com/cyberjack256/IrSplunk/master/setup.sh)
    ```

    The script will prompt you to enter and confirm the Splunk admin password, then deploy Splunk in a Docker container.

2. **Access Splunk:**
   - Once the deployment is complete, access the Splunk web interface at `http://<your-host>:8000`.
   - Log in with the username `admin` and the password you specified during setup.

3. **Customize Setup (Optional):**
   - Modify the `docker-compose.yml`, `custom_entry.sh`, and `setup_indexes.sh` files as needed to fit your use case.
   - Redeploy the app using `docker-compose up -d`.

## Files

- `setup.sh`: Script to prompt the user for Splunk admin password, create Docker secret, and deploy the app.
- `docker-compose.yml`: Docker Compose configuration to define the Splunk service, volumes, and custom entry script.
- `custom_entry.sh`: Custom entry script to read the Docker secret and start Splunk.
- `setup_indexes.sh`: Script to set up indexes in Splunk for various forensic artifacts.

## Support

For any issues, feature requests, or general inquiries, feel free to open an issue in this GitHub repository.
