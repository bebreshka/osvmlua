# OSVMLua

**[Русский 🇷🇺](README_ru.md) | English 🇬🇧**

## Purpose & Idea

OSVMLua is a low-level execution platform designed to allow users to run Lua scripts in a safe, isolated environment using real host resources. The idea came from wanting a system similar to OpenComputers, but without being tied to a game like Minecraft. The goal is to provide real computation power, including GPU and CPU capabilities, directly to scripts while keeping execution sandboxed.

## Project Vision

OSVMLua enables multiple users to send Lua scripts through a frontend (VanJS + esbuild) to a backend written in Java. The backend executes the code safely and returns results (metrics, buffers, etc.) over WebSocket. The system uses the host machine’s resources for actual computation. Future plans include support for other programming languages if there is sufficient interest.

## Backend Operation & Hardware Requirements

- **Backend:** Java-based, leveraging low-level Linux operations for high performance.  

- **Execution Isolation:** Each Lua script runs in a separate sandbox, preventing malicious access to the host system.  

- **Resource Usage:** Scripts can utilize CPU and GPU resources for computations (e.g., frame calculations), with results sent back to clients.  

- **Hardware Requirements:** Linux host with modern CPU and GPU, standard RAM depending on load. No game dependencies.  

- **Configuration:** Resource limits (CPU, RAM, GPU, storage, etc.) are defined in backend config files.

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

## Use Cases & Audience

OSVMLua is useful for developers, researchers, and hobbyists who want to run and test scripts in real-time using actual machine resources. It can be used for:  

- Computational tasks  

- Learning Lua scripting  

- Experimenting with GPU acceleration  

- Creating interactive demos requiring high-performance calculations  

The platform provides a realistic execution environment while maintaining safety and manageability.

## 🛑 License and Usage Conditions

This project is **Source-Available**, and is **NOT Open Source**. The code is subject to strict limitations on commercial use and modification.

The code is licensed under the **Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0)**. The complete legal text of this license is provided in the **[LICENSE](LICENSE)** file.

### What You **CAN** Do (Non-Commercial Use Only)

* **View and Run:** You may view and execute the code for personal, research, or other non-commercial purposes.
* **Personal Modification:** You may create modifications (e.g., in a local clone or fork) solely for your private use.
* **Propose Changes:** You are welcome to submit suggestions or improvements via **Pull Requests (PRs)**.

### What You **CANNOT** Do (Prohibited Activities)

* **Commercial Use:** You may not use this code in any project or activity intended for commercial advantage or monetary compensation.
* **Distribution of Modifications:** You may **not** share, publish, or distribute any modified versions of the code (due to the **NoDerivatives** condition).

### Author's Control of Development

Due to the **NoDerivatives (ND)** condition, all improvements must be reviewed, accepted, and committed by the original authors (bebreshka and kotik9821) into the main repository before they can be considered part of the project.

***

## 📜 Copyright Notice

All rights to the source code and documentation are held by the authors.
