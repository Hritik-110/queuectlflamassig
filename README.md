#  🚀 queuectl — CLI-Based Background Job Queue

A lightweight Node.js-based background job queue supporting persistent storage, multiple workers, retries with exponential backoff, DLQ (Dead Letter Queue), and priority scheduling — all powered by SQLite and a clean CLI.


#  🧰 Tech Stack

Node.js

Commander.js (CLI)

Better-SQLite3 (database)

UUID (unique job IDs)


#  🛠️ Commands
Start Monitoring Dashboard  :  node src/server.js
Start a Worker   : node src/worker.js
node src/worker.js  :: node bin/queuectl.js enqueue "echo 'Hello world!'"
List All Jobs : node bin/queuectl.js list
Reset Entire Queue Database : node bin/queuectl.js reset

# 🎥 Demo Video:
Drive Link: https:…

#  🧩 Features

✅ Persistent job storage (SQLite)

✅ Multiple worker processing

✅ Exponential backoff retry system

✅ Dead Letter Queue (DLQ)

✅ Priority-based scheduling (High → Low)

✅ Simple & powerful CLI

✅ Configurable poll intervals & retry rules

#  ⚡ How It Works (Short)

Enqueue → Job saved in SQLite with pending state.

Worker → Picks highest-priority job, executes, updates state.

Retry → On failure, job retries with exponential backoff.

DLQ → After max retries, job moves to Dead Letter Queue.

Manual Retry → Pick any failed job and requeue it.
