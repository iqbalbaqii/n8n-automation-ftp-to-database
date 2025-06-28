# n8n Automation: FTP to MySQL Database

This project automates the process of transferring Excel files from an FTP server to a MySQL database using [n8n](https://n8n.io/).

## Features

- Scheduled automation using a Cron trigger (runs every hour by default)
- Downloads Excel files from an FTP server
- Extracts and parses Excel data
- Inserts data into a MySQL database
- Easily configurable via Docker Compose

## Project Structure

- `docker-compose.yml` — Docker Compose setup for running n8n and related services
- `schema/ftp-excel-to-db.json` — n8n workflow JSON for FTP-to-MySQL automation

## Workflow Overview

The workflow consists of the following steps:
1. **Cron Trigger**: Starts the workflow on a schedule (every hour)
2. **Download FTP file**: Fetches the Excel file from the FTP server
3. **Extract Excel**: Parses the Excel file
4. **Insert into DB**: Inserts the parsed data into a MySQL database

## Getting Started

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/n8n-automation-ftp-to-database.git
   cd n8n-automation-ftp-to-database
   ```

2. **Configure environment variables:**
   - Edit the `docker-compose.yml` file to set your FTP and MySQL database credentials.

3. **Start the services:**
   ```bash
   docker-compose up -d
   ```

4. **Access n8n:**
   - Open your browser and go to [http://localhost:5678](http://localhost:5678).

5. **Import the workflow:**
   - In n8n, import the workflow from `schema/ftp-excel-to-db.json`.

## Customization

- Adjust the Cron schedule as needed in the workflow
- Modify the FTP path, Excel parsing, or MySQL table/columns to fit your requirements