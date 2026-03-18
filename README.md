# flask-azure-cloud-project

## Project Overview
This project demonstrates deploying a "Flask web application" on "Microsoft Azure" using two Virtual Machines (VM1 & VM2) with "high availability" and traffic distribution through an "Azure Load Balancer".

It is part of my journey in the **Cloud Computing track**, after learning:
- Linux & Docker
- Networking (MCSA & CCNA)
- Azure Fundamentals (AZ-900)
- Azure Administrator (AZ-104)

---

## Infrastructure Components
- Virtual Network (cloud-vnet) + Subnet** – Central network for project resources.
- Virtual Machines (VM1 & VM2) – Hosting the Flask application.
- Network Security Groups (NSG) – Controlling access (HTTP port 80) to VMs.
- Public IP (flask-lb-ip) – Entry point for users to access the app.
- Azure Load Balancer (Public, Basic) – Distributes traffic evenly between VM1 & VM2.
- Backend Pool – Collection of VMs receiving traffic.
- Health Probe (flask-probe) – Ensures only healthy VMs receive traffic.
- Load Balancing Rule (flask-lb-rule) – Connects Frontend IP to Backend Pool on TCP port 80.

---


## Steps Implemented
1. Created (VM1 & VM2) and configured "NSG".
2. Deployed Public Load Balancer (`flask-lb`).
3. Configured Frontend IP (`flask-lb-ip`).
4. Added VMs to Backend Pool.
5. Created Health Probe (`flask-probe`) for availability checks.
6. Configured Load Balancing Rule (`flask-lb-rule`).
7. Tested app via Public IP → `Hello from Flask! This is my DevOps assessment app.`

---

## Skills Demonstrated
- Azure Virtual Machines & Networking
- NSG Configuration & Security
- Load Balancer Setup & Traffic Distribution
- Cloud Infrastructure Design & Documentation

---

## Next Steps / Enhancements
- Add Autoscaling for dynamic traffic handling
- Integrate "DNS & SSL/TLS"
- Implement "Monitoring & Alerts"
- Introduce "CI/CD pipelines" or "Containers (Docker/Kubernetes)"

---

