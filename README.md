# 🚚 AI-Powered Waybill (TTN) Document Processing Bot

An automated self-hosted pipeline designed to ingest, parse, and structure Waybill / Consignment Note (ТТН) documents received via Telegram. Built using **n8n**, **Google Gemini Multimodal API**, and **Telegram Bot API**.

---

## 📌 Project Overview
Logistics and consignment documents (Waybills/TTN) often come in unstructured visual formats (photos, scans, PDFs). Manually extracting route details, cargo parameters, and signatures is slow and error-prone. 

This project automates the entire processing lifecycle: receiving documents, running multimodal layout extraction, validating logistics parameters, and storing structured outputs.

## 🚀 Key Features
- **Telegram Interface:** Drivers or dispatchers submit photos or PDF scans of Waybills directly in Telegram.
- **Multimodal AI Extraction:** Leverages Google Gemini 1.5 to dynamically parse unstructured photo/PDF table layouts.
- **Data Extracted:**
  - TTN Number & Document Date
  - Sender / Consignor & Recipient / Consignee details
  - Departure and delivery addresses
  - Cargo description, weight, volume, and quantity of places
  - Transport & Driver registration details
- **Self-Hosted Infrastructure:** Orchestrated fully on a personal VPS instance with Docker and n8n.

---

## 🛠 Tech Stack
- **Orchestration:** n8n (Docker on Ubuntu VPS)
- **AI Processing:** Google Gemini API (Multimodal Vision Prompting)
- **Messaging API:** Telegram Bot API
- **Data Transfer:** JSON Schema

---

## 📈 Real-World Impact
- Eliminates manual data entry for logistics and consignment tracking.
- Reduces waybill processing time from **3–5 minutes down to <20 seconds**.
- Formats structured payloads ready for CRM/ERP integration.
