# Calculate Client Security Hash – UiPath Project

## Overview
This project automates the process of retrieving client data from an Orchestrator queue, generating a security hash, and submitting the result to a web form. It is built using UiPath's REFramework to ensure scalability, reliability, and proper error handling.

## Objective
- Retrieve transaction data (Client ID, Name, Country) from the Orchestrator queue
- Generate a SHA1 hash from the combined client data
- Submit the hash into a specified field on a web application
- Follow robust exception handling and logging practices

## Technologies Used
- UiPath Studio
- REFramework
- Orchestrator Queues
- SHA1 Hashing using Invoke Code
- Web Automation with dynamic selectors
- Secure credential handling via Orchestrator Assets

## Features
- REFramework-based structure (Init, Get Transaction, Process, End)
- Uses Config file for dynamic values and settings
- Retrieves credentials securely from Orchestrator
- Implements detailed logging and retry mechanisms
- Uses dynamic selectors for stable UI automation
- Processes multiple transactions from the queue

## How It Works
1. **Init**: Reads configuration, initializes applications and credentials.
2. **Get Transaction**: Retrieves one transaction item (client data) at a time.
3. **Process**: Concatenates Client ID, Name, and Country, computes SHA1 hash, and submits it.
4. **End**: Closes applications and performs cleanup.

## Prerequisites
- UiPath Studio and Orchestrator
- Configured Queue with client data (Client ID, Name, Country)
- SHA1 hash function implemented via Invoke Code or .NET method
- Access to the target web application
- Assets in Orchestrator for credentials

## Output
- SHA1 hash submitted for each transaction on the web form
- Execution logs stored in output/logs
- Status of each queue item updated (Success/Failed)

## How to Use
1. Import the project into UiPath Studio.
2. Configure `Config.xlsx` with required settings and asset names.
3. Ensure Orchestrator has the correct Queue and Assets.
4. Run the process from Studio or Orchestrator.

## Author
This project was developed as part of an RPA training program to demonstrate the use of REFramework and queue-driven automation in UiPath.

---

You can enhance this project by adding screenshot capture, improved exception logging, or dashboard integration.
