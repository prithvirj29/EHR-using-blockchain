# EHR Management using Blockchain

This project is a blockchain-based Electronic Health Record (EHR) system that allows patients, doctors, and administrators to manage medical data with a secure and transparent workflow. The application combines a Django REST API, an Angular frontend, blockchain smart contracts, and IPFS for file storage.

## Overview

The platform is designed to:

- manage patient records securely on the blockchain
- allow doctors to view and update patient information
- enable patients to book appointments and access their records
- give administrators control over the overall workflow
- store medical documents and files in IPFS to reduce central storage dependency

## Tech Stack

- Frontend: Angular
- Backend: Django + Django REST Framework
- Blockchain: Truffle + Solidity + Ganache
- Storage: IPFS
- Database: SQLite (for Django local development)

## Project Workflow

### 1. Clone the repository

```bash
git clone https://github.com/prithvirj29/EHR-using-blockchain.git
cd EHR-using-blockchain
```

### 2. Install prerequisites

Make sure the following are installed:

- Node.js: https://nodejs.org/en/download/
- Python: https://www.python.org/downloads/
- Git: https://git-scm.com/downloads
- IPFS: https://dist.ipfs.tech/#go-ipfs
- Angular CLI:

```bash
npm install -g @angular/cli
```

- Truffle:

```bash
npm install -g truffle
```

If Truffle fails, use:

```bash
npm install -g truffle@5.4.29
```

### 3. Set up the Django backend

Open a terminal in the Server folder:

```bash
cd Server
python -m pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

This starts the Django REST API on the local development server.

### 4. Start Ganache and configure blockchain

- Launch Ganache
- Create or import a workspace for the project
- Ensure the blockchain network is running locally
- Deploy the smart contracts using Truffle

### 5. Install frontend dependencies

Open a terminal in the Client folder:

```bash
cd Client
npm install --force
truffle migrate
npm start
```

This will build and run the Angular application.

### 6. Access the app

Once the frontend is running, open:

```text
http://localhost:4200/
```

Before using the application, make sure MetaMask is configured for the local blockchain network.

## Important Notes

### IPFS configuration

The project depends on IPFS for storing uploaded medical files. Ensure your IPFS node is running and configured correctly.

### Resetting the project

If you need to reset the local database:

```bash
cd Server
python manage.py flush
```

If you need to redeploy smart contracts:

```bash
cd Client
truffle migrate
```

## Repository Structure

```text
EHR-using-blockchain/
├── Client/
│   ├── src/
│   ├── contracts/
│   ├── migrations/
│   └── package.json
├── Server/
│   ├── api/
│   ├── ehr/
│   ├── requirements.txt
│   └── manage.py
├── Pictures/
├── README.md
├── README.txt
├── package.json
└── db.sqlite3
```

## Screenshots

These images already exist in the repository and showcase the application workflow:

![Main Page](Pictures/Main%20Page.png)

![Admin Dashboard](Pictures/Admin%20Dashboard.png)

![Doctor Dashboard](Pictures/Doctor%20Dashboard.png)

![Patient Dashboard](Pictures/Patient%20Dashboard.png)

![Booking appointment by patient](Pictures/Booking%20appointment%20by%20patient.png)

![Patient record](Pictures/Patient%20record.png)

## Image Descriptions

### Image 1: Voice-Driven AI Patient Report Interface

![Doctor Assistant GUI](Pictures/Doctor%20Assistant%20GUI.png)

This screen shows a voice-driven AI-based patient reporting interface used for generating clinical notes. The system allows a doctor to record patient details through speech or manual input and organize them into a structured report. The interface is designed for a lightweight desktop environment and simplifies the process of creating patient records from spoken interactions.

It is especially useful for capturing patient history, prescriptions, and general notes without requiring repetitive manual typing during consultation.

### Image 2: Attached PDF in the Patient Record

![Generated PDF Report](Pictures/Generated%20PDF%20Report.png)

This image shows the generated PDF report attached within the patient record workflow. After the voice-driven AI captures and organizes the consultation details, the system creates a downloadable PDF that can be linked to the patient record as an official report or attachment.

This demonstrates how the patient report is generated, stored, and attached to the medical record so that it can be reviewed, shared, or printed when needed.

## Useful Links

- Project setup playlist: https://youtube.com/playlist?list=PL54V-i7zW55d1VKxEkp9DCPt5k_zE6m3X
- GitHub repository: https://github.com/prithvirj29/EHR-using-blockchain.git

## Support

If you run into setup issues, double-check the prerequisites, blockchain network, and IPFS connection before retrying the workflow.
