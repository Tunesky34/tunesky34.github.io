# Kareem Sodiq Babatunde

**DevOps, Cloud & Platform Engineer** · Terraform · Ansible · Docker/Podman · Nomad · CI/CD · AWS

I build the infrastructure and automation that let teams ship software quickly and safely: repeatable environments defined as code, pipelines that test and deploy on every commit, and containerised services that run the same everywhere.

📍 Lagos, Nigeria · ✉️ [tunesky34@gmail.com](mailto:tunesky34@gmail.com) · 💼 [LinkedIn](https://www.linkedin.com/in/kareem-sodiq-460973245/)

---

## What I do

- **Automate delivery.** CI/CD with GitHub Actions, GitLab CI and Jenkins, from commit to tested image to deployment.
- **Codify infrastructure.** Environments provisioned with Terraform and configured with Ansible, so they can be reviewed, versioned and rebuilt on demand.
- **Run containers securely.** Docker and rootless Podman workloads, self-hosted runners, and orchestration on Nomad and Kubernetes.
- **Make systems observable.** Logging and monitoring with Loki, Promtail, Grafana and CloudWatch.

## Skills & tools

| Area | Tools |
|---|---|
| Cloud | AWS (EC2, VPC, ALB, CloudWatch) |
| CI/CD | GitHub Actions, GitLab CI, Jenkins |
| Infrastructure as code | Terraform (including libvirt and Terraform Cloud) |
| Configuration management | Ansible, ansible-freeipa |
| Containers & orchestration | Docker, Docker Compose, rootless Podman, Nomad, Consul, Kubernetes |
| Identity & access | FreeIPA (LDAP, Kerberos, HBAC/RBAC, SSH key management) |
| Observability | Grafana, Loki, Promtail, CloudWatch |
| Languages & tooling | Bash, Node.js/TypeScript, Git |
| Systems | Linux administration (Ubuntu, Rocky Linux) |

---

## Featured projects

### 1. Identity and access management platform: FreeIPA proof of concept
*Platform engineering spike, The Community Revolution*

Evaluated FreeIPA as a central directory and access-control platform, then built the proof of concept entirely as code so it can be rebuilt on demand.

- Provisioned the server VM with **Terraform (libvirt)** and configured FreeIPA and its access policy with **Ansible (ansible-freeipa)**; the full run completed with zero failed tasks.
- Verified SSH public key management, **Kerberos SSO**, host-based access control (HBAC), sudo rules and the full user lifecycle across a server and an enrolled Ubuntu client.
- Documented findings such as SSSD cache behaviour affecting key revocation and the differences between sudo implementations on the client.
- Delivered a VM-versus-container deployment assessment, an OIDC/SAML integration path (identity broker with LDAP federation) and a go/no-go decision document.

**Stack:** FreeIPA · Terraform · Ansible · KVM/libvirt · Rocky Linux · Ubuntu · Kerberos · SSSD

### 2. Event relay: Plane to Google Chat notifications
*Internal tooling, The Community Revolution*

Plane only offers mobile push notifications, so I built a webhook relay that receives project events, filters them and posts clear messages to the right Google Chat spaces.

- Built with **Node.js, Express and TypeScript**, test-first with Jest and Supertest against fixtures based on Plane's webhook specification.
- Maps Plane projects to Chat spaces through configuration, verifies webhook signatures, and formats messages with the object, the people involved and the action taken.
- Packaged with a Dockerfile and Compose file and deployed on a VPS under **rootless Podman**.
- Live Plane events now reach a real Google Chat space end to end.

**Stack:** Node.js · TypeScript · Express · Jest · Podman · Google Chat webhooks

### 3. Rootless Podman GitLab Runner and container CI
*Platform engineering, The Community Revolution*

Designed a CI runner setup that avoids a root-owned Docker daemon, plus the pipelines that use it.

- Deployed a **rootless Podman GitLab Runner** and compared executor options, with a deployment plan and comparison written up for the team.
- Built an end-to-end libvirt custom-executor VM runner and resolved disk, DNS, QEMU and first-boot issues along the way.
- Fixed a GitLab CI pipeline for a BookStack and MariaDB Podman deployment, including a hanging health-check dependency and a Podman-in-Docker networking failure (switched the firewall driver to iptables).
- Documented gotchas such as Podman short-name resolution so others could reproduce the setup.

**Stack:** GitLab CI · Podman · libvirt · BookStack · MariaDB

### 4. Nomad and Consul deployment pipeline with centralised logging
*DevOps engineering internship, Springer Capital*

A containerised service built and tested in GitHub Actions, published to GHCR and deployed to a Nomad and Consul cluster, with logs shipped through Promtail and Loki into Grafana.

**Stack:** GitHub Actions · GHCR · Nomad · Consul · Loki · Promtail · Grafana
🔗 [devops-intern-final](https://github.com/Tunesky34/devops-intern-final)

---

## More projects

| Project | What it shows |
|---|---|
| [Jenkins-image](https://github.com/Tunesky34/Jenkins-image) | Jenkins CI/CD for a Node.js app, Dockerised with automated tests and AWS deployment |
| [TERRAFORM-PROJECT-USING-ALB-WITH-AWS](https://github.com/Tunesky34/TERRAFORM-PROJECT-USING-ALB-WITH-AWS) | VPC, subnets, EC2 and security groups behind an ALB, provisioned with Terraform Cloud |
| [DOCKERIZED-WORDPRESS-SITE](https://github.com/Tunesky34/DOCKERIZED-WORDPRESS-SITE) · [DOCKERIZED-CONTAINER](https://github.com/Tunesky34/DOCKERIZED-CONTAINER) | Multi-stage Dockerfiles, non-root users, Compose stacks |
| [Kubernetes-RealApp-Deployment](https://github.com/Tunesky34/Kubernetes-RealApp-Deployment) | Deployment, Service and Ingress manifests for a real app |
| [ansible-nginx-deployment](https://github.com/Tunesky34/ansible-nginx-deployment) | Ansible playbooks installing Docker and running Nginx |

---

## Certifications

- AWS Certified Cloud Practitioner
- Docker & Kubernetes Associate

## Get in touch

Open to DevOps, platform and cloud engineering roles and freelance work, including CI/CD setup, Terraform and Ansible infrastructure, container migration and monitoring.

✉️ [tunesky34@gmail.com](mailto:tunesky34@gmail.com) · 💼 [LinkedIn](https://www.linkedin.com/in/kareem-sodiq-460973245/)
