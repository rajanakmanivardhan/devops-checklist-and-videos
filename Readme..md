# DevOps & Cloud Sequential Learning Studio

An interactive, single-file sequential learning portal and curriculum tracker for mastering **DevOps & Cloud Engineering** from fundamentals to real-world projects. Built with a hybrid **Apple Human Interface** and **Google Material 3 Expressive** design system, per-user authentication, step-by-step lesson unlocking, and downloadable progress reports.

---

## Key Features

* **Sequential Step-by-Step Unlocking (158 Lessons · 15 Modules):** Starts at **Module 1, Lesson 1** and unlocks subsequent videos and modules in strict fundamentals-to-mastery order as you complete each lesson.
* **Hidden-by-Default Topic Explorer:** All 15 topic modules remain collapsed until selected, paired with custom gradient vector artwork cards so you can focus on one module at a time.
* **Direct YouTube Playback & Search:** Opens mapped lessons directly on YouTube (`youtube.com/watch?v=<ID>`) and provides clean YouTube search links (`youtube.com/results?search_query=...`) for remaining lessons without broken playlist-index redirects.
* **Multi-User Login & Profiles:** Register and sign in with individual user profiles (passwords hashed locally in the browser via Web Crypto SHA-256), keeping sequential progress, starred lessons, and completion timestamps isolated per user.
* **User Progress Reports (CSV, PDF & Multi-User Summary):** Generate an individual module-by-module progress report, export a full **CSV** spreadsheet, print/save as **PDF**, or compare progress across all local user profiles.
* **Apple HIG + Material 3 Expressive UI:** Features a frosted-glass sticky navigation bar, circular completion progress ring, tonal metric cards, pointer-ripple interactions, floating action dock, and **Auto / Dark / Light** theme support.

---

## Curriculum Structure (15 Modules · 158 Videos)

1. **DevOps fundamentals and SDLC** — Prerequisites, DevOps fundamentals, SDLC improvements, and DevOps project management.
2. **Linux administration** — Linux fundamentals, directory hierarchy, users/files/Vi editor, permissions, process/disk/network management, virtual machines, and WSL 2.
3. **Shell scripting** — Complete shell scripting foundations, zero-to-hero parts 1 & 2, and a live AWS shell scripting project.
4. **Networking** — Core networking concepts and the OSI model.
5. **Git and GitHub** — Version control basics, branching strategies, and Git commands/interview Q&A.
6. **Python for DevOps** — Syllabus through core Python, Boto3 automation, GitHub–Jira Flask projects, and interview Q&A.
7. **AWS** — Course overview, IAM, EC2, VPC, Security Groups/NACLs, Route53, S3, CLI, CloudFormation, CodeCommit/CodePipeline CI/CD, CloudWatch, Lambda, cost optimization, CloudFront, ECR/ECS, Secrets, Terraform on AWS, Config, Load Balancers, and live deployment projects.
8. **Azure** — Azure fundamentals, Resource Groups, VMs, VNets, Storage, Azure CLI, ARM/Bicep, IAM/Entra, Azure DevOps, AKS, Key Vault, Serverless Functions, Terraform on Azure, and cost optimization.
9. **Docker and containers** — Container basics, Docker zero-to-hero, Django containerization, multi-stage/distroless builds, volumes/bind mounts, container networking, and interview Q&A.
10. **Kubernetes** — Kubernetes introduction, architecture, KOPS, Pods, Deployments/ReplicaSets, Services, Kubeshark traffic inspection, Ingress, RBAC, Custom Resources/Controllers, and ConfigMaps/Secrets project.
11. **Terraform and Infrastructure as Code** — IaC fundamentals, syllabus, providers/variables, modules, remote state & locking, real-time tasks, workspaces, Vault integration, interview scenarios, and end-to-end Terraform project.
12. **Ansible** — Configuration management concepts (Puppet vs. Ansible) and Ansible zero-to-hero.
13. **CI/CD and Jenkins** — CI/CD concepts, Jenkins zero-to-hero with live projects, GitHub Actions & custom runners, and CI/CD interview Q&A.
14. **Monitoring and observability** — Observability fundamentals, Prometheus, custom instrumentation & alerts, EFK logging stack, Jaeger distributed tracing, end-to-end/multi-cloud monitoring, and Kubernetes Prometheus & Grafana live demo.
15. **AI-assisted DevOps** — Syllabus, AI-assisted DevOps fundamentals, prompt engineering, Gen-AI project, local DeepSeek setup, AI shell scripting, AIOps & log analysis, AI agents (Crew AI, local LLMs, Retool), and full-stack AI deployment test.

---

## How to Run & Host on GitHub

1. Place `index.html` in the root of your GitHub repository.
2. Open `index.html` directly in any modern web browser, **or** enable **GitHub Pages**:
   * Go to **Settings → Pages** in your GitHub repository.
   * Under **Build and deployment**, select **Deploy from a branch**, choose your main branch and `/ (root)`, and save.
3. Create a user account on the sign-in screen to begin tracking progress and exporting reports.

---

## Data & Privacy Note

* All user accounts, hashed passwords, lesson completion states, starred items, and timestamps are stored locally in your browser's `localStorage` (`devops-portal-users-v1` and `devops-portal-session-v1`).
* Use **Export User JSON** or **Download CSV Report** periodically to back up your progress across browsers or devices.
