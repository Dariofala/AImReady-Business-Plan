# AImReady
> **Turning exam-day panic into practiced confidence.**

AImReady is an AI-powered virtual exam panel designed to help university students overcome oral-exam anxiety through immersive, objective, and repeatable practice sessions. 

This repository contains the foundational Business Plan and architectural design developed for the **Business and Project Management** course (Master's Degree in Artificial Intelligence and Data Engineering) at the **University of Pisa**.

---

## The Problem
Oral-exam anxiety is the norm, not the exception. Studies show that a vast majority of students experience moderate-to-high pre-exam stress, which directly hurts their academic performance and future job chances. Current practice methods (like mirror practice or being quizzed by family) fail because they lack two crucial elements: **real exam pressure** and **objective, measurable feedback**.

## Our Solution
AImReady simulates a real university exam panel using a sophisticated Multi-Agent AI system. It provides students with a safe space to fail, get accustomed to the pressure of an interrogation, and receive actionable feedback strictly on their communicative behavior (e.g., pacing, fillers, vocal steadiness, gaze), explicitly avoiding emotion labeling or official grading.

---

## System Architecture
The core of AImReady relies on a localized, privacy-first data architecture. The system operates in two main phases:

### 1. Live Exam Phase
* **Student Input:** Users upload their own course material. The browser captures audio and video via webcam/mic.
* **Multimodal Processing:** Utilizes **Whisper** for accurate speech-to-text recognition and edge-based vision frameworks (like MediaPipe/TensorFlow.js) to process facial expressions client-side, ensuring raw biometric data never leaves the device.
* **Multi-Agent Engine (Live):**
  * **Lead Examiner (GPT-4o-mini):** Asks the main subject-matter questions in a structured way.
  * **Assistant Examiner (Llama 3.1 8B):** Fast-paced agent that jumps in with direct follow-up questions to simulate pressure.
  * **Silent Coordinator (Claude Haiku):** Reads transcripts and delivery metrics to apply pacing rules and coordinate the two speaking agents without ever addressing the student directly.

### 2. Post-Exam Phase
* **Evaluation Panel (Async):** The LLMs reread the transcript to evaluate content accuracy and clarity.
* **Final Report:** Generates a comprehensive breakdown of the student's communicative performance, offering actionable suggestions to improve delivery and non-verbal signals.

---

## Defensibility & Compliance
AImReady is designed with strict adherence to the **EU AI Act**. By keeping all video processing on the edge and limiting the output to behavioral feedback (without inferring emotional states or providing certifying grades), the system operates safely within the role-play and training simulation exemptions.
Our FTO (Freedom to Operate) analysis confirms that the European market is unobstructed by current 3D-simulation patents, allowing us to build a strong data moat through strategic B2B institutional licenses.

---

## The Team
This project was collaboratively designed and developed by:
* **Dario Falaschi**
* **Leonardo Lentini**
* **Chiara Nasoni**
* **Vittoria Vellutini**

*Università di Pisa - 2025/2026*
