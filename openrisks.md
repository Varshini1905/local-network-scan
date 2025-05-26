#  Risks Associated with Open Ports (Nmap Scan)

##  Common Services – Risks

| **Port**  | **Service**       | **Risks** |
|-----------|-------------------|-----------|
| **135/tcp** | msrpc | Can be abused for remote code execution or lateral movement via DCOM or RPC-based attacks (e.g., **EternalBlue**). Often targeted in Windows environments. |
| **139/tcp** | netbios-ssn | Can expose file shares, leak sensitive system info, or be used for **Man-in-the-Middle (MitM)** attacks like SMB Relay. |
| **445/tcp** | microsoft-ds | High-risk port; vulnerable to SMB-based exploits like **EternalBlue**, **WannaCry**, **NotPetya**, and credential theft. |
| **1521/tcp** | oracle | If Oracle DB is exposed and not properly secured, it can lead to **unauthorized database access**, **data leakage**, or **SQL injection**. |
| **5432/tcp** | postgresql | Similar to Oracle; if improperly configured, may allow attackers to access or manipulate the database remotely. |
| **7070/tcp** | realserver | May expose streaming media servers; older RealServers are known for **buffer overflow** and **directory traversal** vulnerabilities. |
| **8081/tcp** | blackice-icecap | Often used for development or admin panels; may be **unauthenticated** or misconfigured, exposing internal tools or debug interfaces. |
| **902/tcp** | iss-realsecure / VMware | Could allow **remote management of virtual machines**. Vulnerabilities here might expose guest VMs or hypervisor details. |
| **912/tcp** | apex-mesh | Unknown service – **high risk** if unmonitored, could be custom or legacy software with unpatched vulnerabilities. |
| **6646/tcp** | unknown | Unknown – potentially dangerous if it’s a backdoor, debug port, or undocumented service. |
| **55555/tcp** | unknown | High-numbered port – often used by custom or test services, and commonly targeted by malware/botnets as a backchannel or C2. |

---

