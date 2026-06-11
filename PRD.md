# Product Requirements Document (PRD)

# Product Name

CuspidAI

AI-Powered WhatsApp Receptionist for Dental Clinics

---

# 1. Executive Summary

DentalFlow AI is a WhatsApp-based AI receptionist designed specifically for dental clinics. It automates patient communication, appointment management, reminders, and lead capture while minimizing operational costs for clinics.

The platform aims to reduce receptionist workload by automating routine interactions and improving patient experience through instant responses.

The product is designed with a lean infrastructure approach, allowing profitability from the first few customers.

---

# 2. Problem Statement

Dental clinics heavily rely on WhatsApp for patient communication.

Common problems include:

* Receptionists spending excessive time answering repetitive questions
* Missed inquiries outside business hours
* Manual appointment scheduling errors
* High appointment no-show rates
* Lack of patient follow-up processes
* Limited visibility into patient interaction trends

Existing solutions are often expensive, generic, and designed for larger healthcare organizations.

Dental clinics need a simple, affordable solution tailored specifically to their workflows.

---

# 3. Product Vision

To become the default AI-powered WhatsApp receptionist for independent dental clinics by automating routine administrative tasks while preserving the option for human intervention when necessary.

---

# 4. Objectives

## Business Objectives

### First 3 Months

* Acquire 5 paying dental clinics
* Achieve ₹15,000 Monthly Recurring Revenue (MRR)
* Validate product-market fit

### First 12 Months

* Acquire 50 dental clinics
* Reach ₹1,50,000 MRR
* Maintain customer churn below 5%

---

# 5. Target Users

## Primary Users

### Dental Clinic Owners

Goals:

* Reduce administrative workload
* Improve appointment attendance
* Increase patient satisfaction
* Reduce staffing costs

Pain Points:

* Missed patient inquiries
* Inefficient appointment handling
* Time-consuming manual processes

---

### Receptionists

Goals:

* Focus on high-value patient interactions
* Minimize repetitive tasks

Pain Points:

* Repeated FAQ responses
* Scheduling conflicts
* Managing reminders manually

---

### Patients

Goals:

* Receive immediate responses
* Easily book appointments
* Obtain treatment information quickly

Pain Points:

* Long wait times for replies
* Difficulty scheduling appointments

---

# 6. Scope

## MVP Features

### 6.1 AI WhatsApp Assistant

Description:

Provide instant responses to patient inquiries using clinic-specific information.

Supported Queries:

* Clinic timings
* Consultation fees
* Available treatments
* Address and directions
* Insurance acceptance
* Emergency contact information

Requirements:

* Understand natural language queries
* Use clinic knowledge base for responses
* Support fallback to human staff

Priority:

Critical (P0)

Success Metric:

80% FAQ automation rate

---

### 6.2 Appointment Booking

Description:

Allow patients to schedule appointments directly through WhatsApp.

Workflow:

1. Patient requests appointment
2. Available slots are retrieved
3. Patient selects preferred slot
4. Appointment is confirmed

Requirements:

* Display available slots
* Prevent double booking
* Store appointment information

Priority:

Critical (P0)

Success Metric:

90% successful booking completion rate

---

### 6.3 Appointment Rescheduling

Description:

Allow patients to modify existing appointments.

Requirements:

* Retrieve current appointment
* Show alternative slots
* Update appointment records

Priority:

Critical (P0)

Success Metric:

95% successful rescheduling rate

---

### 6.4 Appointment Cancellation

Description:

Allow patients to cancel appointments.

Requirements:

* Verify appointment ownership
* Update appointment status
* Offer rescheduling option

Priority:

Critical (P0)

Success Metric:

95% cancellation accuracy

---

### 6.5 Automated Appointment Reminders

Description:

Automatically remind patients about upcoming appointments.

Reminder Schedule:

* 24 hours before appointment
* 2 hours before appointment

Requirements:

* Schedule messages automatically
* Track delivery status

Priority:

Critical (P0)

Success Metric:

Reduce no-show rate by 25%

---

### 6.6 Knowledge Base Management

Description:

Allow clinics to maintain information used by the AI assistant.

Information Types:

* Clinic timings
* Services offered
* Treatment pricing
* Address
* Dentist information
* Frequently asked questions

Requirements:

* Add new FAQs
* Edit existing information
* Generate embeddings for search

Priority:

High (P1)

Success Metric:

85% answer accuracy

---

### 6.7 Human Handoff

Description:

Transfer conversations to clinic staff when AI confidence is low.

Requirements:

* Confidence threshold detection
* Staff notification
* Resume automation after handoff

Priority:

High (P1)

Success Metric:

95% successful escalation rate

---

### 6.8 Lead Capture

Description:

Collect patient information for follow-up purposes.

Captured Information:

* Patient name
* Phone number
* Treatment interest
* Preferred appointment date

Requirements:

* Automatically identify potential leads
* Store lead information securely

Priority:

Medium (P2)

Success Metric:

90% lead data completeness

---

### 6.9 Analytics Dashboard

Description:

Provide insights into clinic operations.

Metrics:

* Total conversations
* Appointments booked
* Appointments cancelled
* No-show rates
* Frequently asked questions
* AI automation rate

Priority:

Medium (P2)

Success Metric:

Weekly dashboard engagement >60%

---

# 7. User Flows

## Appointment Booking Flow

Patient initiates booking request

↓

AI checks appointment availability

↓

Available slots presented

↓

Patient selects preferred slot

↓

Appointment confirmed

↓

Reminder schedule created

---

## FAQ Resolution Flow

Patient asks question

↓

Knowledge base searched

↓

AI generates response

↓

Response sent

↓

Conversation completed

---

## Human Escalation Flow

Patient inquiry received

↓

AI confidence below threshold

↓

Conversation assigned to receptionist

↓

Staff responds manually

↓

Conversation resolved

---

# 8. Functional Requirements

## Authentication

* Clinic admin login
* Staff role management
* Secure password storage

---

## WhatsApp Integration

* Receive incoming messages
* Send outgoing messages
* Delivery status tracking
* Template message support

---

## Appointment Management

* Create appointments
* Update appointments
* Cancel appointments
* Retrieve schedules

---

## AI Services

* FAQ retrieval
* Intent classification
* Response generation
* Escalation detection

---

## Notification System

* Appointment reminders
* Staff escalation alerts
* Booking confirmations

---

# 9. Non-Functional Requirements

## Performance

AI response latency:

< 5 seconds

Dashboard loading time:

< 3 seconds

Webhook processing:

< 2 seconds

---

## Reliability

Platform uptime:

99%

Reminder delivery success:

99%

---

## Security

Requirements:

* HTTPS encryption
* Secure credential storage
* Role-based access control
* Patient data isolation per clinic

---

## Scalability

Initial Capacity:

* 50 clinics
* 5,000 conversations/month

Future Capacity:

* 500 clinics
* 100,000 conversations/month

---

# 10. Technical Architecture

## Frontend

Framework:

React + Vite

Hosting:

Cloudflare Pages

Estimated Cost:

₹0/month

---

## Backend

Framework:

FastAPI

Hosting:

Railway (Free Tier)

Alternative:

Render

Estimated Cost:

₹0 to ₹400/month

---

## Database

Platform:

Supabase PostgreSQL

Features:

* Authentication
* Database
* Storage
* Row Level Security

Estimated Cost:

₹0/month

---

## Vector Search

Technology:

pgvector extension within Supabase

Purpose:

Knowledge base retrieval

Estimated Cost:

₹0/month

---

## AI Layer

Primary Model:

Gemini 2.5 Flash

Responsibilities:

* Response generation
* Intent classification
* FAQ answering

Alternative:

GPT-5 Nano

Estimated Cost:

₹0 to ₹200/month

---

## Messaging Platform

Technology:

Meta WhatsApp Cloud API

Responsibilities:

* Message delivery
* Incoming webhooks
* Template messages

Estimated Cost:

₹50 to ₹500/month depending on usage

---

## Scheduling Engine

Technology:

APScheduler

Responsibilities:

* Reminder scheduling
* Follow-up notifications

Estimated Cost:

₹0/month

---

## Monitoring

Technology:

Sentry Free Tier

Responsibilities:

* Error monitoring
* Exception tracking

Estimated Cost:

₹0/month

---

# 11. Database Entities

## Clinics

* Clinic ID
* Name
* Contact Information
* Address
* Operating Hours
* Consultation Fees

---

## Patients

* Patient ID
* Clinic ID
* Name
* Phone Number

---

## Appointments

* Appointment ID
* Patient ID
* Clinic ID
* Appointment Time
* Status

Statuses:

* BOOKED
* CANCELLED
* COMPLETED
* NO_SHOW

---

## Conversations

* Conversation ID
* Clinic ID
* Patient ID
* Message Content
* Sender Type
* Timestamp

---

## Knowledge Base

* FAQ ID
* Clinic ID
* Question
* Answer
* Vector Embedding

---

# 12. Success Metrics

## Business Metrics

* Monthly Recurring Revenue
* Customer Acquisition Cost
* Customer Lifetime Value
* Monthly Churn Rate

---

## Product Metrics

* FAQ Automation Rate >80%
* Booking Completion Rate >90%
* Reminder Delivery Success >99%
* Human Escalation Rate <20%

---

## Customer Metrics

* Customer Satisfaction Score >4.5/5
* Net Promoter Score >40

---

# 13. Pricing Strategy

## Starter Plan

₹2,999/month

Features:

* FAQ automation
* Appointment booking
* Appointment reminders
* Up to 500 monthly conversations

---

## Growth Plan

₹4,999/month

Features:

* Human handoff
* Lead capture
* Analytics dashboard
* Up to 1,500 monthly conversations

---

## Premium Plan

₹7,999/month

Features:

* Multiple staff accounts
* Advanced reporting
* Priority support

---

# 14. Development Roadmap

## Week 1

* WhatsApp webhook integration
* AI assistant setup
* Knowledge base functionality

---

## Week 2

* Appointment booking
* Rescheduling
* Cancellation workflows

---

## Week 3

* Reminder scheduling
* Human handoff implementation
* Lead capture

---

## Week 4

* Analytics dashboard
* Production deployment
* Pilot clinic onboarding

---

# 15. Estimated Operating Costs

Initial Monthly Infrastructure Cost:

₹130 to ₹200/month

Expected Cost at 10 Clinics:

₹1,500 to ₹2,000/month

Expected Revenue at 10 Clinics:

₹29,990/month

Estimated Gross Margin:

> 90%

---

# 16. Risks and Mitigation

## AI Hallucinations

Mitigation:

Restrict responses to knowledge base content.

---

## WhatsApp API Pricing Changes

Mitigation:

Monitor usage and adjust pricing plans.

---

## Low Customer Adoption

Mitigation:

Offer free trials and collect feedback from pilot clinics.

---

## Appointment Errors

Mitigation:

Implement validation checks and human handoff mechanisms.

---

# 17. Definition of Success

A dental clinic should be able to:

* Complete onboarding within 30 minutes
* Automate at least 70% of patient interactions
* Reduce receptionist workload by 40%
* Decrease appointment no-shows by at least 25% within the first month of adoption
