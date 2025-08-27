# 📧 MailMind – Automate your email replies via n8n

# 📧 Automatic Gmail Replies with n8n + Gemma AI

This project is an **AI-powered email assistant** built with [n8n](https://n8n.io/). It automates Gmail responses using **Gemma/Gemini AI** and logs interactions into **Google Sheets**.

---

## 🔹 Features

* Fetches **unread / starred / important Gmail messages**
* Only replies to **Starred or Important emails** (user can manually mark these) → prevents replying to every mail
* Reads the **email body**
* Uses **Gemma/Gemini AI** to generate a professional reply
* Logs email details + AI draft into **Google Sheets**
* Sends the reply back to the sender automatically
* Marks the original email as **Read**

---

## 🔹 Workflow Overview

```
[Schedule Trigger] 
   → [Get All Gmail Messages] 
   → [Get a Message] 
   → [AI Agent (Gemma/Gemini)] 
   → [Append Row in Google Sheets] 
   → [Reply to Message] 
   → [Mark as Read]
```

---

## 🔹 Skills Demonstrated

* Workflow automation with **n8n**
* Integration with **Gmail API**
* **Prompt engineering** for LLMs (Gemma/Gemini)
* Data logging with **Google Sheets**
* Building an **end-to-end automation pipeline**

---

## 🔹 Setup Instructions

1. **Clone or Download** this repository.
2. **Import the workflow** into your n8n instance:

   * Go to *n8n → Workflows → Import from File*
3. **Configure credentials** in n8n:

   * Gmail (OAuth2)
   * Google Sheets (OAuth2)
   * Gemini/Gemma API
4. Update the **Google Sheet ID** in the `Append row in sheet` node.
5. Activate the workflow.

✅ Now your Gmail will automatically reply to starred/important emails (which you mark manually) and log them in Google Sheets.

---

## 🔹 Example Google Sheet

| Sender Name | From Email                                    | Email Body                   | Draft Reply                   | Thread ID |
| ----------- | --------------------------------------------- | ---------------------------- | ----------------------------- | --------- |
| Alice       | [alice@example.com](mailto:alice@example.com) | "Can we reschedule meeting?" | "Sure Alice, 5pm works fine." | 123456789 |

---

## 🔹 Notes

* AI-generated replies are **polite, concise, and professional**.
* Replies always close with:

  ```
  Best regards,
  Rohaz Bhalla
  ```
* Emails are marked as **Read** only after reply is successfully sent.
* Bot replies **only to messages marked Important or Starred**, so you can control which emails are handled automatically.

---

## 📌 Tech Stack

* [n8n](https://n8n.io)
* Gmail API
* Google Sheets API
* Gemma / Google Gemini AI

---

## 📌 Author

👨‍💻 Built by **Rohaz Bhalla**
