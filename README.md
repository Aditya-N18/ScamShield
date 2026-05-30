Hi this is a project for hack harvard- 
# ScamShield – Real-Time Call Scam Detection System
## lets get started
## Overview

ScamShield is a real-time scam detection system that analyzes live phone calls and assigns a risk score based on speech patterns and conversational signals. The system is designed to assist users during calls by identifying potential scams as they happen, rather than after the damage is done.

This project was built to explore low-latency audio processing, real-time AI inference, and distributed system design under streaming conditions.

---

## Key Features

* Real-time audio streaming and processing
* Live transcription using speech-to-text (Whisper)
* Scam risk scoring using NLP-based heuristics
* Low-latency backend with event-driven architecture
* Scalable pipeline using Redis queues
* Modular system for future AI model upgrades

---

## Tech Stack

* Backend: Node.js (Express)
* Streaming: WebSockets / Twilio Voice API
* AI / ML: OpenAI Whisper (speech-to-text), NLP scoring logic
* Queue System: Redis (Pub/Sub + event queues)
* Storage: MongoDB / PostgreSQL (optional logging)
* Deployment: Local / Cloud-ready architecture

---

## System Architecture

1. Incoming call audio is streamed via Twilio Voice API
2. Audio chunks are sent to backend through WebSockets
3. Backend processes audio stream in near real-time
4. Speech-to-text conversion using Whisper
5. Transcribed text is passed into scam detection logic
6. Risk score is calculated dynamically
7. Alerts or insights are generated for the user

Pipeline is designed to minimize latency while maintaining accuracy.

---

## Core Problem

Most scam detection systems operate post-call (e.g., spam flags, reports). This creates a delay between attack and prevention.

ScamShield focuses on **real-time intervention**, allowing users to detect and respond to threats during the call itself.

---

## Design Decisions

* Chose streaming over batch processing to enable real-time insights
* Used Redis queues to decouple audio ingestion and processing
* Designed modular scoring system to allow future ML model integration
* Prioritized low latency over heavy model complexity

---

## Challenges & Solutions

**1. Real-Time Processing Constraints**
Streaming audio while maintaining low latency required chunk-based processing and asynchronous pipelines.

**2. Noise & Speech Variability**
Handled by focusing on conversational patterns rather than exact phrasing.

**3. Scalability**
Redis queues were introduced to handle concurrent processing and avoid blocking.

---

## Example Flow

* User receives a suspicious call
* Audio is streamed into the system
* Transcript generated in near real-time
* System detects patterns like urgency, threats, financial requests
* Risk score increases dynamically
* User receives warning signal

---

## Future Improvements

* Train custom ML model for scam classification
* Add multilingual support
* Integrate real-time alert UI (mobile/web)
* Improve contextual understanding using LLMs
* Build dataset from labeled scam calls

---

## What This Project Demonstrates

* Real-time systems engineering
* Distributed architecture design
* AI integration in live pipelines
* Practical problem-solving in security domain

---

## GitHub

https://github.com/2006-sk

---

## Author

Shresthkumar Karnani
Computer Science @ San José State University

Aditya Nagpal
Computer Science @ San José State University

---
