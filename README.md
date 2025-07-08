deepak_sin@LP1-AP-52217668:/mnt/c/Users/deepak_sin/ansible-grafana-zipkin-poc/ansible$ cat README.md
cat << 'EOF' > README.md
# 🛠️ Ansible + Grafana + Prometheus Observability Setup

This project automates the setup of **Grafana** with a Prometheus data source and a pre-configured dashboard using **Ansible**. It runs smoothly in a **WSL + Docker Compose** environment.

---

## 📁 Directory Structure

\`\`\`
.
├── grafana.yml                   # Main Ansible playbook
├── files/
│   └── dashboard.json            # Grafana dashboard definition
├── roles/
│   └── grafana/
│       ├── defaults/
│       │   └── main.yml          # Default variables
│       └── tasks/
│           └── main.yml          # Main tasks to run
└── .gitignore
\`\`\`

---

## ⚙️ Prerequisites

- WSL or Linux Shell
- Docker & Docker Compose
- Python + Ansible installed in WSL
- Grafana running at \`http://localhost:3001\`
- Prometheus accessible at \`http://prometheus:9090\`

---

## 🚀 Run the Automation

\`\`\`bash
ansible-playbook grafana.yml
\`\`\`

This will:

- ✅ Wait for Grafana to be healthy
- ✅ Check/create Prometheus data source
- ✅ Import the dashboard defined in \`files/dashboard.json\`

---

## 📊 Customize the Dashboard

1. Open Grafana UI
2. Create or edit a dashboard
3. Click "Share" → Export → Save to JSON
4. Replace \`files/dashboard.json\` with your version
5. Rerun the playbook

---

## 🧪 Tested With

- Ansible 2.14+
- Grafana 10+ (running on port 3001)
- Prometheus (running inside Docker at port 9090)

---

## 📌 Author

Made by **Deepak Singh**
🔗 GitHub: [https://github.com/DeepakSRR](https://github.com/DeepakSRR)

---

## 📄 License

MIT License
EOF

git add README.md
git commit -m "📝 Final clean README with Bash-safe formatting"
