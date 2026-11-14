# Hi, I'm Ibnu 👋

DevOps learner building a production-style homelab on Kubernetes — GitOps all the way down. Currently working in F&B while transitioning into DevOps.

## 🏠 Homelab GitOps — the main thing

My Kubernetes homelab, managed entirely through GitOps. No `kubectl apply` from my laptop — ArgoCD syncs everything from git.

**Repo:** [WanXSky/homelab-gitops](https://github.com/WanXSky/homelab-gitops)

**Live:** [ArgoCD](https://argocd.kzt.biz.id) · [api.kzt.biz.id](https://api.kzt.biz.id)

**What's running:**
- **K3s** (v1.37.2) — 1 server + 2 agents
- **ArgoCD** (v3.6.1) — app-of-apps pattern, 8 applications, all Healthy + Synced
- **ingress-nginx** (4.13.1) + **cert-manager** (v1.18.2) — TLS everywhere
- **PostgreSQL** (Bitnami 18.7.13) + **SealedSecrets** — no plain secrets in git, ever
- **Cloudflare Tunnel** — origin IP hidden, no public IP exposed
- **base-api** (TypeScript + Express) — my own API, live on the cluster

**What I learned building it:** ArgoCD `ignoreDifferences` for API-server normalisation drift, and how `kubectl apply`'s 3-way merge can no-op a sync for 852 rounds while reporting success. Wrote it up as a playbook in the repo.

## 🛠️ Other projects

- **[base-api-ts](https://github.com/WanXSky/base-api-ts)** — TypeScript + Express API, deployed to the homelab via GitOps
- **Pondok Sakpore SaaS** — full-stack restaurant system (TypeScript/Express + PostgreSQL, Docker + Helm for K3s, CI with CodeQL + Trivy) — menu management, stock per item, orders via WhatsApp, admin dashboard with visitor tracking

## 🧭 Now building / next

- **HPA** (Horizontal Pod Autoscaler) for base-api — scale on CPU/memory
- **Observability as code** — Prometheus + Grafana managed in GitOps (Grafana already runs on the cluster; now making it declarative)
- **Trivy** image scanning in CI — fail the build on critical vulnerabilities

## 💻 Tech Stack

![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=flat&logo=kubernetes&logoColor=white)
![ArgoCD](https://img.shields.io/badge/ArgoCD-EF7B4D?style=flat&logo=argo&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=flat&logo=docker&logoColor=white)
![Helm](https://img.shields.io/badge/Helm-0F1689?style=flat&logo=helm&logoColor=white)
![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=flat&logo=typescript&logoColor=white)
![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=flat&logo=express&logoColor=%2361DAFB)
![PostgreSQL](https://img.shields.io/badge/postgres-%23316192.svg?style=flat&logo=postgresql&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat&logo=Cloudflare&logoColor=white)
![Nginx](https://img.shields.io/badge/nginx-%23009639.svg?style=flat&logo=nginx&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=flat&logo=githubactions&logoColor=white)
![Grafana](https://img.shields.io/badge/grafana-%23F46800.svg?style=flat&logo=grafana&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)

## 🌐 Socials

[![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?logo=Instagram&logoColor=white)](https://instagram.com/ibnu.alwan.m_)

## 📊 GitHub Stats

![](https://github-readme-stats.shion.dev/api?username=WanXSky&theme=calm&hide_border=false&include_all_commits=true&count_private=false)
![](https://streak-stats.demolab.com/?user=WanXSky&theme=calm&hide_border=false)
![](https://github-readme-stats.shion.dev/api/top-langs/?username=WanXSky&theme=calm&hide_border=false&include_all_commits=true&count_private=false&layout=compact)
