# 📅 Automated Scheduling System

A complete appointment scheduling system that processes messages from text files, manages clients, professionals, and appointments, and generates receipts — all powered by Python and SQLite.

---

## 🚀 What this project does

- Reads messages from `.txt` files in the `mensagens_recebidas/` folder
- Detects user intent: `book`, `list`, `cancel`, `confirm`, `help`
- Extracts professional, date, and time from natural language
- Manages appointment flow: booking, confirmation, cancellation
- Generates receipts and stores data in SQLite database
- Saves responses in the `mensagens_enviadas/` folder

---

## 🧠 How it works

1. Place a `.txt` file with messages in `mensagens_recebidas/`
2. The system reads the file and processes each message
3. It detects the user's intent and manages the conversation state
4. Appointments are saved in a local SQLite database (`agendamentos.db`)
5. Receipts are generated in the `agendamentos/` folder
6. Responses are saved in `mensagens_enviadas/`

---

## 📁 Project Structure

```
automated_scheduling/
├── mensagens_recebidas/      # Input: message files (.txt)
├── mensagens_enviadas/       # Output: response files (.txt)
├── agendamentos/             # Output: generated receipts
├── agendamentos.db           # SQLite database
├── estados_conversas.json    # Conversation state cache
└── sistema_agendamento.py    # Main script
```

---

## 🛠️ How to Run

1.  **Place your message files** in the `mensagens_recebidas/` folder.

2.  **Run the script:**
    ```bash
    python sistema_agendamento.py
    ```

3.  **Check the results** in `mensagens_enviadas/` and `agendamentos/`.

---

## 📌 Message Format

Each message file must follow this structure:

```
FROM: 5511999999999
NAME: Client Name
DATE: 15/12/2024 10:00:00
==================================================
Book with Dr. Carlos Silva for tomorrow
```

---

## 🧩 Technologies Used

- Python 3.10+ (standard library only)
- SQLite3
- Regular Expressions (`re`)
- JSON for state management

---

## 🙏 Credits & Original Work

This project was developed by [alictech7-oss](https://github.com/alictech7-oss).

---

## 📄 License

MIT — use, modify, and share freely.
