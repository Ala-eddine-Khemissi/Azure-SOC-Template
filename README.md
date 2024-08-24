![architecture](https://github.com/user-attachments/assets/964b19fc-0de8-482e-9ec7-f48d4d56a156)

This draw represents an Azure architecture diagram designed to ensure security, monitoring, and role-based access control for a cloud-based environment. Here's a detailed description of the key components:
1. Identity and Access Management:
•	Microsoft Entra ID (formerly Azure AD): The architecture includes Microsoft Entra ID for identity management, enabling secure access to resources.
•	Conditional Access: This feature is used to enforce policies that determine the conditions under which users can access resources.
•	Privileged Identity Management (PIM): PIM is implemented to manage, control, and monitor access within Azure, ensuring that privileged roles are only accessible as needed.
2. User and Role Management:
•	Internet Access: Different user roles, such as DB Admin, DB Developer, VM Admin, and General User, access the system from the internet.
•	Firewall: Internet traffic is filtered through a firewall to ensure secure access to the virtual network.
3. Virtual Network and Subnets:
•	Azure Bastion Subnet: Provides secure RDP/SSH access to virtual machines without exposing them to the public internet.
•	Virtual Machine Subnet: Contains Windows VMs with Defender agents installed, ensuring endpoint security.
•	Database Subnet: Hosts the SQL Database, which is protected by Microsoft Defender for DB. Role-based access control (RBAC) is enforced to manage database access.
4. Security and Monitoring:
•	Network Security Groups (NSGs): NSGs are used in subnets to control inbound and outbound traffic, providing an additional layer of security.
•	Microsoft Defender for Cloud: This service is used to assess and protect the security posture of both virtual machines and databases.
•	Monitor and Log Analytics: These services are part of the monitoring and security subnet, allowing for comprehensive logging, monitoring, and alerting of activities within the environment.
•	Microsoft Sentinel: Acts as the Security Information and Event Management (SIEM) and Security Orchestration, Automation, and Response (SOAR) solution, offering advanced threat detection and response capabilities.
5. Data Protection and Encryption:
•	Key Vault: Used for managing encryption keys, ensuring that data is encrypted at rest via Customer Managed Keys (CMK).
•	DDoS Protection: The architecture is equipped with DDoS protection to defend against distributed denial-of-service attacks.
6. Integration and Connectivity:
•	Defender Agents: These are installed on virtual machines to ensure they are protected against threats.
•	Firewall and Security Layer: The firewall provides a robust security layer, ensuring that only authorized traffic is allowed within the environment.
•	Role-Based Access Control (RBAC): This is enforced at various points in the architecture to ensure that users only have access to the resources they need based on their role.

