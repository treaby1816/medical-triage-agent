# 🏥 Medical Triage AI Agent

![Status](https://img.shields.io/badge/Status-Prototype-orange?style=for-the-badge)
![Role](https://img.shields.io/badge/Role-Automation_Engineer-red?style=for-the-badge)
![Tech](https://img.shields.io/badge/Tech-n8n_|_Conditional_Logic_|_Healthcare-red?style=for-the-badge)

## 📋 Executive Summary
Architected by **Adewole Felix Bamidele**, this system automates the patient intake process by acting as a "Digital Triage Nurse." It uses conditional logic to analyze patient symptoms in real-time and route them to the correct medical department, reducing wait times for critical cases.

## 🛠️ Technical Know-How
1. Conditional Logic (If-This-Then-That)
Implemented complex Switch Nodes in n8n that parse keywords like "chest pain," "bleeding," or "unconscious" to trigger immediate high-priority alerts.

2. Privacy & Compliance
Designed with data minimization in mind. The system strips PII (Personally Identifiable Information) before sending analytics to the dashboard, ensuring patient confidentiality is maintained.

3. Real-Time Alerting
Connected to Twilio API to deliver SMS alerts to doctors within 3 seconds of a high-risk submission.

## 🧠 Triage Logic Architecture

```mermaid
graph TD
    A[Patient Form Input] -->|Webhook| B(n8n Triage Engine)
    B -->|Analyze Symptoms| C{Severity Check}
    C -->|High Fever + Chest Pain| D[🚨 EMERGENCY ROUTE]
    C -->|Moderate Symptoms| E[⚠️ Urgent Care Route]
    C -->|Checkup/Refill| F[General Practice Route]
    
    D -->|Action| G[SMS Alert to On-Call Doctor]
    E -->|Action| H[Schedule Next Available Slot]
    F -->|Action| I[Send Calendar Booking Link]


    


Architected by: Adewole Felix Bamidele Solutions Architect & Automation Engineer
