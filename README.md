# OSVMLua

## Backend Operation & Hardware Requirements

- **Backend:** Java-based, leveraging low-level Linux operations for high performance.  

- **Execution Isolation:** Each Lua script runs in a separate sandbox, preventing malicious access to the host system.  

- **Resource Usage:** Scripts can utilize CPU and GPU resources for computations (e.g., frame calculations), with results sent back to clients.  

- **Hardware Requirements:** Linux host with modern CPU and GPU, standard RAM depending on load. No game dependencies.  

- **Configuration:** Resource limits (CPU, RAM, GPU, storage, etc.) are defined in backend config files.
## 📜 Copyright Notice

All rights to the source code and documentation are held by the authors.
