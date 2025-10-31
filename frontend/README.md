# OSVMLua

## Frontend & Interactivity

The frontend provides an interactive simulation of a virtual machine environment, including:  

- EEPROM chip  

- Storage devices

- RAM modules  

- CPU, APU, GPU  

- Real-time characteristics and usage metrics  

This interface allows users to visualize resource allocation and monitor metrics from scripts running on the backend.

## Data Storage

- JSON is used as the database to store user data and resource states.  

- Since the project is not designed for massive concurrent users, JSON allows direct modification of individual user limits after shutting down the backend or through backend console commands.

## Authorization & User Management

- No frontend registration system.  

- Host executes a command like `create user <username>` on the backend.  

- A 256-character hash password is generated automatically and used for login.  

- This ensures secure, host-controlled user creation and authentication.

## 📜 Copyright Notice

All rights to the source code and documentation are held by the authors.
