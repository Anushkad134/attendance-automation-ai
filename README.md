# 📋 Attendance Automation Using AI

> *"What's my attendance?"* — answered in seconds, not office hours.

A Telegram-based attendance assistant that turns a raw spreadsheet row into a friendly, formatted report — no app to install, no portal to log into, just a message and a reply.

Built entirely as a visual, no-code workflow in **n8n**, powered by **Google Sheets** as the data store and **OpenAI GPT-4o-mini** as the report writer.

---

## ✨ Features

| | |
|---|---|
| 🤖 | **Telegram chatbot** — query attendance with a simple `/attendance <roll_no>` command |
| 📊 | **Google Sheets integration** — live lookup against a spreadsheet acting as the attendance database |
| 🧠 | **AI-generated reports** — GPT-4o-mini converts raw rows into clean, emoji-formatted messages |
| ✅ | **Two-stage validation** — confirms the record is dated *today* and that a status has actually been recorded |
| ⚠️ | **Automatic "Do not Bunk" warning** — flagged whenever attended sessions fall short of total sessions |
| ⚡ | **Real-time delivery** — response lands back in the same Telegram chat within seconds |

---

## 🧱 Tech Stack

- **n8n** — workflow orchestration
- **Telegram Bot API** — chat interface
- **Google Sheets** — attendance database
- **OpenAI GPT-4o-mini** — natural-language report generation

---

## 🔄 Workflow

```
📩 Telegram Trigger
        │
        ▼
🔢 Extract Roll Number
        │
        ▼
📑 Google Sheets Lookup
        │
        ▼
📅 Date Check  ──►  ❓ Status Check
        │
        ▼
🧠 OpenAI: Generate Report
        │
        ▼
📤 Telegram: Send Reply
```

A student sends `/attendance 101` → the bot looks up roll number `101` for *today's* date → checks a status exists → hands the record to GPT-4o-mini → sends back a clean report with attendance %, and a bunking warning if it's low.

---

## 🖼️ Screenshots

> *Add screenshots here after uploading them.*

| Telegram Report | Google Sheet Source |
|---|---|
| _add image_ | _add image_ |

---

## 🚀 Why This Approach

| Instead of... | This does... |
|---|---|
| Manual email/in-person lookups | Instant self-service, 24/7 |
| A heavyweight LMS portal | A chat message on an app students already have |
| A custom mobile app | A visual, no-code workflow anyone can inspect and modify |

---

## 🔮 Future Scope

- 🔐 Link Telegram users to their own roll number (real auth)
- 🗄️ Swap Google Sheets for a proper database at scale
- 📈 Weekly/monthly summaries & subject-wise breakdowns
- 🔔 Proactive low-attendance alerts, not just on-demand queries
- 🎯 End-to-end integration with biometric/facial attendance capture

---

## 📚 References

- [n8n Documentation](https://docs.n8n.io)
- [Telegram Bot API](https://core.telegram.org/bots/api)
- [Google Sheets API](https://developers.google.com/sheets/api)
- [OpenAI API](https://platform.openai.com/docs)

---

<p align="center">Built with 🤖 + 📊 + 💬 — because nobody should have to email a professor to ask "sir, attendance?"</p>
