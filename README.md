cat > README.md <<'EOF'
# 📊 Ansible + Grafana + Prometheus Automation

This repository automates the setup of a Grafana dashboard with Prometheus as a data source using **Ansible**.

---

## 📁 Directory Structure

\`\`\`
.
├── grafana.yml                      # Main Ansible playbook
├── files/
│   └── dashboard.json              # Grafana dashboard definition
├── roles/
│   └── grafana/
│       ├── defaults/
│       │   └── main.yml            # Default variables
│       └── tasks/
│           └── main.yml           # Main tasks to run
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

✅ Wait for Grafana to be healthy  
✅ Check/create Prometheus data source  
✅ Import the dashboard defined in \`files/dashboard.json\`

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
git commit -m "📝 Final README with Bash-safe formatting and directory tree"
git push origin main
