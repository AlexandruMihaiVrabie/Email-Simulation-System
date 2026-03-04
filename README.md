# Email-Simulation-System

A clean, interactive Python simulation of a basic email client. This project utilizes core **Object-Oriented Programming (OOP)** principles to model how users, inboxes, and individual emails interact with one another in a software ecosystem.

## 🚀 Features

* **OOP Architecture:** The system is cleanly divided into three distinct, interacting classes: `User`, `Inbox`, and `Email`, making the codebase modular and easy to expand.
* **Timestamping:** Automatically tracks and formats the exact date and time an email was created using Python's built-in `datetime` module.
* **State Tracking:** Emails maintain their own state, automatically switching from `[Unread]` to `[Read]` the moment a user opens them.
* **Full Inbox Management:** Users can send messages to other users, list all emails in their inbox, read full message contents, and delete emails by their index number.
* **Zero Dependencies:** Built entirely with standard Python libraries.

## 🧠 System Architecture

The simulation relies on the relationship between three main objects:

1. **`Email` Class:** The fundamental data container. It holds the sender, receiver, subject, body, timestamp, and a boolean flag for the read/unread status.
2. **`Inbox` Class:** Acts as the storage manager. It contains a dynamic list of `Email` objects and handles the logic for listing, fetching, and deleting them based on user input.
3. **`User` Class:** The top-level entity. Every user has a `name` and their own dedicated `Inbox` instance. Users interact with each other by generating `Email` objects and passing them directly into another user's `Inbox`.

## 🛠️ Requirements & Running

This project requires **Python 3.x**.

1. Clone the repository or download the `email_simulator.py` file.
2. Open your terminal or command prompt.
3. Run the script using:

```bash
python email_simulator.py
```

## 💻 Code Example & Usage

The script includes a `main()` function that demonstrates the core functionality. Here is how you can use the classes to build your own interactions:

```python
# Create two users
alice = User('Alice')
bob = User('Bob')

# Alice sends an email to Bob
alice.send_email(receiver=bob, subject='Meeting Update', body='Hey Bob, the meeting is moved to 3 PM.')

# Bob checks his inbox to see the unread message
bob.check_inbox()

# Bob reads the first email (which changes its state to Read)
bob.read_email(1)

# Bob deletes the email
bob.delete_email(1)
```

**Expected Output Example:**
```text
Email sent from Alice to Bob!

Bob's Inbox:
Your Emails:
1. [Unread] From: Alice | Subject: Meeting Update | Time: 2023-10-27 14:30

--- Email ---
From: Alice
To: Bob
Subject: Meeting Update
Received: 2023-10-27 14:30
Body: Hey Bob, the meeting is moved to 3 PM.
------------

Email deleted.
```

## 🤝 Contributing

Contributions are highly encouraged! This is a great foundational
