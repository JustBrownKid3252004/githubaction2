# 💋 Telegram Automated Alert System

This project is a GitHub Actions-based automation designed to send scheduled voice messages and text alerts to Telegram. It is currently configured to send a daily "Kiss & Voice" greeting to my girlfriend, Nway.

## 🚀 Features

*   **Scheduled Automation**: Runs twice daily (9:30 AM and 9:30 PM Myanmar Standard Time).
*   **Voice Message Support**: Automatically uploads and sends `voice.m4a` using the Telegram Bot API.
*   **Secure Implementation**: All sensitive credentials (Bot Token and Chat IDs) are managed via GitHub Secrets to ensure privacy.
*   **Dual Notification**: Capable of sending alerts to multiple chat IDs simultaneously.

## 🛠️ Technical Stack

*   **GitHub Actions**: Workflow orchestration and scheduling.
*   **Telegram Bot API**: Messaging interface.
*   **Shell/Curl**: For file upload and API interaction.

## 🔒 Security Setup

To keep this project secure, the following secrets must be configured in the GitHub Repository Settings:

| Secret Name | Description |
| :--- | :--- |
| `TELEGRAM_BOT_TOKEN` | Your unique Telegram Bot API token. |
| `NWAY_ID` | The Telegram Chat ID for the primary recipient. |
| `MY_CHAT_ID` | Your personal Chat ID for delivery notifications. |

## 📂 Project Structure
```text
githubaction2/
├── .github/workflows/
│   └── send_kiss.yml       # The core automation logics
├── voice.m4a          # The voice file to be sent
└── README.md          # Project documentation
