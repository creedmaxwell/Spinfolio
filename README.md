# Spinfolio

Track and manage your vinyl records, CDs, and cassette collections with Spinfolio — a modern, full-stack media cataloging app.

<img width="1919" height="905" alt="image" src="https://github.com/user-attachments/assets/fdc0d826-1f21-4c08-98c1-babb291d6f4a" />

## 🧠 About

Spinfolio is a web application to help music lovers catalog their physical media (vinyl, CDs, cassettes). It provides:

- Easy addition of items with metadata (artist, title, format, etc.)
- Browsable collection views
- Search and filters
- User authentication and personalized collections
- AI chatbot to answer questions about a user's collection and make recommendations

Built with a **Python backend** and a **JavaScript frontend**, Spinfolio aims to be simple, extensible, and fun to use. 

---

## 🚀 Features

- 📀 Store your favorite albums across formats
- 🔍 Search and filter your collection
- 🧑‍💻 Full CRUD on media items
- 📡 RESTful API for backend services
- 📱 Responsive UI
- 🤖 AI chatbot

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| Backend | Python |
| Frontend | JavaScript |
| Styles | CSS |
| Data | SQLite (configurable) |

---

## 🤖 AI Agent Overview

Spinfolio includes an AI agent designed to enhance how users search, explore, and understand their physical media collections.

The agent works by embedding collection records into a vector space, allowing it to reason semantically about albums, artists, genres, and other metadata rather than relying only on exact keyword matches. This enables more intelligent interactions such as similarity search, contextual recommendations, and flexible querying.

### How it works

 - Hybrid storage approach

    - A relational database (e.g., SQLite/PostgreSQL) stores authoritative, structured data such as albums, artists, formats, and ownership details.

    - A vector store maintains embeddings of collection items for semantic retrieval.

 - Semantic retrieval

    - When a user queries their collection, the agent performs similarity search in the vector store to find contextually relevant items.

    - Results can then be filtered, ranked, or enriched using structured data from the relational database.

 - Incremental ingestion

    - New records can be embedded and added individually without rebuilding the entire vector space, allowing the system to scale efficiently as collections grow.

### Capabilities

 - Semantic search over user collections

 - Context-aware recommendations

 - Flexible querying across structured and unstructured metadata

 - Extensible foundation for future features (summaries, trends, insights)

This design allows Spinfolio to combine the reliability of traditional databases with the expressiveness of modern embedding-based AI systems, keeping the platform both practical and intelligent.

## 🔧 Getting Started

### Prerequisites

Make sure you have the following installed:

- Python 3.10+
- Git

---

### Backend Setup

```bash
# Clone the repo
git clone https://github.com/creedmaxwell/Spinfolio.git
cd Spinfolio/server

# Create and activate virtual env
python -m venv venv
source venv/bin/activate  # macOS/Linux
venv\Scripts\activate     # Windows PowerShell

# Install Python dependencies
pip install -r requirements.txt

# Start server
python app.py

# Your API backend will be live at:

http://localhost:8000/
