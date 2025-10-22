# 🤖 AI Support Triage — n8n Automation Workflow

> Automatically triages incoming support emails, classifies priority with an LLM, creates GitHub issues, and sends daily summaries via email.

---

## 🧩 Workflow Overview

This n8n workflow automates a full support pipeline:

1. **Trigger:** Gmail trigger on new support emails. 
2. **LLM Categorization:** Uses OpenAI to classify ticket priority (P1–P4). 
3. **GitHub Integration:** Creates issues in a linked repository. 
4. **Labeling:** Adds Gmail labels and marks processed mails as read. 
5. **Acknowledgment:** Sends auto-response emails. 
6. **Sheets Logging:** Logs data in Google Sheets. 
7. **Daily Digest:** Scheduled summary email with ticket stats.

---

## 📸 Visual Preview

![Workflow Overview](./screenshots/workflow-full.png)
![GitHub Issue](./screenshots/github-issue.png)

---

## ⚙️ Tech Stack

- **n8n Cloud**
- **Gmail API**
- **GitHub API**
- **Google Sheets**
- **OpenAI LLM**
- **JavaScript Code Nodes**
- **Scheduled Trigger + Digest**

---

## 🔒 Setup & Deployment

1. Import the workflow:
- Go to n8n → “Workflows” → “Import from file” → select `ai-support-triage.json`.
2. Reconnect the following credentials:
- Gmail OAuth2
- GitHub OAuth2
- Google Sheets
- OpenAI API Key
3. Update constants in the “Set Constants (Global)” node.
4. Run manually or activate the workflow to run automatically.

---

## 🧠 Example Output

**GitHub Issue Example:** 
`https://github.com/username/ai-support-triage/issues/1`

**Auto Acknowledge Email:** 
_Subject:_ “✅ Request received — P2 Support Ticket” 
_Body:_ Includes category, severity, and GitHub link.

**Daily Digest Email:**
| Priority | Count |
|-----------|--------|
| P1 | 1 |
| P2 | 4 |
| P3 | 2 |

---

## 🌟 Portfolio Highlights

- End-to-end automation integrating AI + DevOps tools. 
- Clean modular design with readable node names. 
- Tested for branching logic (critical alerts, non-critical digests). 
- Demonstrates practical workflow orchestration using n8n.

---

## 📤 Export

You can import the same workflow by using this JSON file: 
👉 [`ai-support-triage.json`](./ai-support-triage.json)
