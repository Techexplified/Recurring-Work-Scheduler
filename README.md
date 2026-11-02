# Recurring Work Scheduler for Jira Cloud

[![Atlassian Forge](https://img.shields.io/badge/Atlassian-Forge-0052CC?logo=atlassian&logoColor=white)](https://developer.atlassian.com/platform/forge/)
[![Jira Cloud](https://img.shields.io/badge/Jira-Cloud-0052CC?logo=jira&logoColor=white)](https://www.atlassian.com/software/jira)

**Recurring Work Scheduler** is a cloud-native Atlassian Forge application for Jira Cloud that automates the creation of repetitive issues, periodic maintenance tasks, review routines, and recurring checklists.

---

## 🚀 Key Features

- **Automated Recurring Cadences**: Schedule Jira issues to generate hourly, daily, weekly, or monthly at custom times and timezones.
- **One-Click Issue Creation**: Convert any existing Jira issue into a recurring schedule directly from the Jira Issue Action menu (`...` > *Create recurring issue*).
- **Dual Dashboards**:
  - **Global Dashboard**: Manage recurring tasks sitewide across all projects via Jira's top `Apps` navigation.
  - **Project Dashboard**: Scoped view within individual Jira project sidebars.
- **On-Demand Execution**: Trigger an issue instantly with **"Create Issue Now"** without waiting for the next timer cycle.
- **Full Lifecycle Controls**: Pause, resume, edit, or delete active schedules with live tracking of issues generated.
- **Enterprise Security**: 100% hosted on Atlassian Cloud (Forge). Zero external database hosting, zero external servers, and zero data egress.

---

## 📖 Documentation & User Guide

For the full user manual, step-by-step guides, and FAQ, please see [DOCUMENTATION.md](DOCUMENTATION.md).

---

## 🔒 Security & Permissions

This application runs within Atlassian's secure Forge runtime and adheres to least-privilege permission scopes:

| Scope | Purpose |
| :--- | :--- |
| `read:jira-work` | Reads project keys, issue types, and issue metadata for task configuration. |
| `write:jira-work` | Creates scheduled Jira issues via Jira REST API v3. |
| `storage:app` | Securely persists schedule definitions in Atlassian Forge Custom Entity Storage. |

No user or project data is ever transmitted outside of your Atlassian site.

---

## 🛠️ Local Development & Deployment

### Prerequisites
- Node.js (v18+)
- [Atlassian Forge CLI](https://developer.atlassian.com/platform/forge/getting-started/) (`npm install -g @forge/cli`)

### Quick Setup

```bash
# 1. Install root dependencies
npm install

# 2. Build the frontend UI
cd static/scheduler-ui
npm install
npm run build
cd ../..

# 3. Deploy to your Forge development environment
forge deploy

# 4. Install into your Jira Cloud site
forge install
```

---

## 📄 License & Support

- **Provider**: Explified
- **Website**: [https://explified.com](https://explified.com)
- **License**: Commercial - No Charge
- **Community**: [Atlassian Community](https://community.atlassian.com)
