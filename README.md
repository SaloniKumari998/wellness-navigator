# 🌿 Wellness Navigator AI

### AI-Driven Personalized Guidance for Physical, Nutritional & Mental Well-Being

> **Wellness Navigator AI** is an AI-powered wellness assistant designed to provide personalized, empathetic, adaptive, and privacy-first guidance across **fitness, nutrition, and mental resilience**.

---

## 📌 Overview

Modern lifestyles have increased the challenges associated with maintaining overall well-being.

People commonly struggle with:

- 🏃 Obesity and physical inactivity
- 🥗 Poor nutrition and hydration
- 🧠 Stress, anxiety, and mental fatigue
- 😴 Poor sleep patterns
- 📉 Inconsistent wellness routines
- 🔄 Lack of continuous and personalized guidance
- 🔐 Privacy concerns surrounding AI-powered health applications

Traditional wellness applications often address these areas separately, resulting in fragmented tracking and limited personalization.

**Wellness Navigator AI** aims to address this gap by providing a unified, adaptive wellness experience that continuously guides users according to their goals, activity levels, and selected health metrics.

---

# 🎯 Vision

> **To build an AI-powered Wellness Navigator that continuously supports users with empathetic, personalized, adaptive, and privacy-first wellness guidance.**

The system combines:

**Empathy + Intelligence + Privacy**

to create a more accessible and holistic wellness experience.

---

# 🧩 Core Problem

### How can we design a secure, adaptive, and holistic AI system that supports wellness without overwhelming users?

Wellness data can involve multiple interconnected areas:

- Physical fitness
- Nutrition
- Mental resilience
- Daily habits
- Activity levels
- Personal goals
- Progress milestones

Instead of overwhelming users with lengthy surveys, Wellness Navigator AI follows an **iterative conversational approach**, collecting information progressively.

---

# 🎯 Primary Goals

### 1. 🧠 Personalized Guidance

Provide guidance based on individual:

- Wellness goals
- Activity level
- Primary health metric
- Fitness interests
- Nutrition goals
- Mental resilience needs

---

### 2. 🔄 Iterative Data Collection

The system follows a conversational approach:

> **One question at a time**

This reduces survey fatigue and allows the coaching experience to adapt dynamically.

---

### 3. 🔐 Secure Data Storage

User and milestone information is stored using **Supabase**, supporting a privacy-first architecture.

---

### 4. ⚡ Automated Health Sync

Validated wellness milestones can be synchronized through a dedicated webhook-based workflow.

The backend exposes:

```text
POST /sync
SDG 3 — Good Health & Well-Being
Wellness Navigator AI aligns with:

United Nations Sustainable Development Goal 3: Good Health and Well-Being

The project focuses on supporting healthier habits, preventive wellness practices, and accessible personalized guidance.

Potential impact
Encourages healthier lifestyle habits

Supports continuous wellness monitoring

Promotes preventive approaches

Helps users identify areas requiring attention

Supports sustainable approaches to personal well-being

Note: Wellness Navigator AI is a wellness-support system and is not intended to replace qualified medical professionals or emergency services.

🤖 What Is Wellness Navigator AI?
Wellness Navigator AI is an AI-driven wellness assistant that:

Understands natural-language wellness goals

Guides users step-by-step

Collects information progressively

Adapts recommendations dynamically

Tracks wellness milestones

Stores validated information securely

Provides empathetic conversational guidance

Redirects users toward professional support when appropriate

🧠 Key Principle
Empathy + Intelligence + Privacy
The system is designed around three core principles:

❤️ Empathy
Interactions are designed to be:

Supportive

Respectful

Non-judgmental

User-centered

🧠 Intelligence
AI-driven coaching helps interpret user goals and dynamically determine the next conversational step.

🔐 Privacy
The architecture emphasizes secure data handling and avoids making assumptions about sensitive wellness information.

⚙️ System Capabilities
🎯 Intent-Based Coaching
The system identifies the user's wellness focus and routes the conversation accordingly.

Wellness domains
Fitness
   │
   ├── Exercise
   ├── Activity
   └── Physical goals

Nutrition
   │
   ├── Food habits
   ├── Protein
   ├── Hydration
   └── Nutrition goals

Mental Resilience
   │
   ├── Stress
   ├── Recovery
   ├── Sleep
   └── Emotional well-being

📊 Iterative Metric Collection
Instead of requesting a long form, the system progressively collects relevant information such as:

Name

Primary goal

Activity level

Primary health metric

Example:

Goal:
Eat more protein

Activity Level:
Weightlifting

Primary Metric:
Daily Protein (grams)

💬 Empathetic AI Coaching
The coaching interface enables users to communicate naturally with the AI.

Example interaction:

User:
I want to improve my fitness but I am struggling to stay consistent.

Coach:
Let's start with a manageable routine. We can identify
a realistic activity target and build from there.

The system aims to keep interactions concise and actionable rather than overwhelming users with large amounts of information at once.

🔄 Adaptive Recommendations
The system generates recommendations based on the user's collected information.

Examples include:

Plan moderate exercise sessions

Maintain a rest or mobility day

Track daily activity

Monitor relevant wellness metrics

Build sustainable habits

Example dashboard recommendations:

Plan 3–4 moderate sessions this week.

Keep one rest or mobility day.

Log steps daily to spot trends.

🚨 Safety-Oriented Design
Wellness Navigator AI is designed with safety considerations in mind.

If the conversation indicates potential medical or emotional distress, the system can redirect the user toward appropriate professional support instead of attempting to replace professional care.

Safety principle
AI Guidance
     │
     ├── General wellness → Continue coaching
     │
     ├── Unclear information → Ask clarification
     │
     └── Potential distress → Encourage professional help

🏗️ System Architecture
The application follows a modular architecture consisting of a React frontend, FastAPI backend, LangGraph-based coaching workflow, and Supabase data layer.

                    ┌──────────────────────┐
                    │      User            │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │   React Frontend     │
                    │  Wellness Dashboard  │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │    FastAPI Backend   │
                    │    REST Endpoints    │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │      LangGraph       │
                    │ Coaching State Flow  │
                    └──────────┬───────────┘
                               │
              ┌────────────────┼────────────────┐
              │                │                │
              ▼                ▼                ▼
        ┌──────────┐     ┌──────────┐    ┌─────────────┐
        │ Fitness  │     │Nutrition │    │  Resilience │
        │   Ward   │     │   Ward   │    │     Ward    │
        └──────────┘     └──────────┘    └─────────────┘
              │                │                │
              └────────────────┼────────────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │      Supabase        │
                    │ Secure Data Storage  │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │    /sync Webhook     │
                    │ Milestone Automation  │
                    └──────────────────────┘

🔁 Stateful Coaching Flow
The coaching system uses LangGraph to manage state and guide the conversation.

High-Level Flow
User submits wellness query
          │
          ▼
FastAPI receives request
          │
          ▼
LangGraph initializes state
          │
          ▼
Intent classification
          │
          ├───────────────┬────────────────┐
          ▼               ▼                ▼
       Fitness         Nutrition      Resilience
          │               │                │
          └───────────────┴────────────────┘
                          │
                          ▼
                 Collect missing metrics
                          │
                          ▼
                 Ask one question
                    at a time
                          │
                          ▼
                 Validate information
                          │
                          ▼
                  Store in Supabase
                          │
                          ▼
                  Trigger /sync
                          │
                          ▼
                  Update dashboard

🧩 LangGraph Nodes
The coaching state machine is organized around multiple nodes.

start_node
Initializes:

Session state

User state

Initial coaching context

intent_classifier_node
Determines the primary wellness area and routes the conversation.

Possible routes:

Fitness Ward
Nutrition Ward
Resilience Ward

Wellness Nodes
These nodes are responsible for:

Identifying missing information

Asking clarification questions

Updating state

Generating contextual guidance

Preparing validated milestone information

🔐 Data & Privacy
Privacy is a core design principle of the project.

Privacy-first principles
Avoid assumptions about user health data

Collect only information required for the current coaching flow

Validate information before synchronization

Store application data through Supabase

Keep milestone synchronization behind a dedicated endpoint

Provide professional-care redirection where appropriate

🔗 API
The FastAPI backend currently exposes the following endpoints:

Method	Endpoint	Purpose
GET	/health	Health check
POST	/coach	AI coaching interaction
POST	/sync	Synchronize validated milestone

GET /health
Used to verify that the backend service is available.

GET /health

POST /coach
Processes the user's wellness information and returns coaching guidance.

POST /coach

The endpoint supports the conversational coaching workflow.

POST /sync
Synchronizes a validated wellness milestone.

POST /sync

The synchronization workflow is designed to run only after the required information has been collected and validated.

📋 API Documentation
FastAPI automatically provides interactive API documentation.

After starting the backend, the Swagger UI can generally be accessed at:

/docs

and the OpenAPI specification at:

/openapi.json

🖥️ User Interface
The React dashboard provides a simple interface for interacting with the Wellness Navigator.

Profile & Metrics
Users can enter:

Name
Primary Goal
Activity Level
Primary Metric

Example:

Name:
Alex

Primary Goal:
Eat more protein

Activity Level:
Weightlifting

Primary Metric:
Daily Protein (grams)

💬 Coach Interaction
The dashboard provides a conversational interface where users can:

Ask the AI coach questions

Receive personalized guidance

Continue the coaching conversation

Synchronize validated milestones

📈 Suggested Actions
The dashboard displays actionable recommendations based on the user's current wellness context.

Example:

Plan 3–4 moderate sessions this week.

Keep one rest or mobility day.

Log steps daily to spot trends.

🛠️ Technology Stack
Technology	Role
⚛️ React	Frontend UI
⚡ FastAPI	Backend API
🧠 LangGraph	Stateful AI coaching workflow
🗄️ Supabase	Data storage
🔗 Webhooks	Milestone synchronization
📄 OpenAPI	API documentation

📁 Project Structure
A typical project structure is:

wellness-navigator/
│
├── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── ...
│
├── backend/
│   ├── main.py
│   ├── ...
│   └── requirements.txt
│
├── README.md
├── .env.example
└── ...

The exact structure may vary depending on the current repository organization.

🚀 Getting Started
1. Clone the Repository
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd <YOUR_REPOSITORY_NAME>

⚛️ Frontend Setup
Navigate to the frontend directory:

cd frontend

Install dependencies:

npm install

Start the development server:

npm run dev

The frontend will then be available at the local development URL shown by Vite.

⚡ Backend Setup
Navigate to the backend:

cd backend

Create a virtual environment:

Windows
python -m venv venv
venv\Scripts\activate

macOS / Linux
python3 -m venv venv
source venv/bin/activate

Install dependencies:

pip install -r requirements.txt

Start FastAPI:

uvicorn main:app --reload

The API will be available at:

http://localhost:8000

Swagger documentation:

http://localhost:8000/docs

🔑 Environment Variables
Create a .env file based on your project's environment configuration.

Example:

SUPABASE_URL=your_supabase_url
SUPABASE_KEY=your_supabase_key

# Add your AI provider/API configuration here
# according to the backend implementation.

Important
Never commit secrets such as:

API keys
Supabase service keys
Access tokens
Private credentials

to GitHub.

Add .env to .gitignore:

.env
.env.local
venv/
__pycache__/
node_modules/

🧪 Application Workflow
A typical user journey looks like this:

Step 1 — Define Profile
The user enters their basic wellness information.

Name
Goal
Activity Level
Primary Metric

Step 2 — Check-In
The user submits their current wellness state.

Step 3 — Intent Detection
LangGraph identifies the appropriate wellness domain.

Step 4 — Progressive Questions
The system asks for missing information one question at a time.

Step 5 — Personalized Guidance
The AI generates contextual recommendations.

Step 6 — Validation
Required milestone information is validated.

Step 7 — Secure Storage
Validated information is stored through Supabase.

Step 8 — Synchronization
The /sync endpoint can synchronize the milestone.

Step 9 — Dashboard Update
The user receives updated recommendations and wellness status.

🔄 Example Coaching Flow
User:
I want to improve my fitness.

        ↓

Intent Classifier

        ↓

Fitness Ward

        ↓

Coach:
What is your current activity level?

        ↓

User:
Weightlifting

        ↓

Coach:
What metric would you like to track?

        ↓

User:
Daily protein

        ↓

System validates required information

        ↓

Supabase

        ↓

Milestone Sync

        ↓

Personalized Suggestions

🎨 Design Principles
🔐 Privacy First
The system should not make unsupported assumptions about a user's health information.

🧠 Pacing
The system follows:

One question per response

This keeps the interaction manageable.

❤️ Empathy
Responses should remain:

Supportive

Respectful

Non-judgmental

Action-oriented

🚨 Safety
Potential medical or emotional distress should be handled with appropriate professional-care guidance rather than attempting to replace healthcare professionals.

✅ Data Integrity
Milestone synchronization occurs only after required information has been validated.

Collect
   ↓
Validate
   ↓
Store
   ↓
Sync

📊 Project Impact
Wellness Navigator AI is designed to:

👤 Empower Individuals
Help users understand and manage their wellness goals through accessible guidance.

🏃 Encourage Healthier Habits
Support consistent routines through actionable recommendations.

🧠 Support Mental Resilience
Include stress, recovery, and emotional well-being within a holistic wellness framework.

🌍 Support Sustainable Healthcare
Promote preventive wellness practices and healthier lifestyle behaviors.

🔮 Future Scope
The project can be extended with:

⌚ Wearable Integrations
Integration with:

Smart watches

Fitness trackers

Step counters

Sleep tracking devices

📊 Predictive Health Analytics
Future versions could analyze longitudinal wellness data to identify trends and provide earlier habit-oriented interventions.

🌐 Multilingual Support
Support for multiple languages would make the system more accessible to a broader range of users.

🧠 Long-Term Habit Intelligence
Future versions could build longer-term understanding of:

Habit consistency

Activity patterns

Nutrition trends

Recovery patterns

Goal progression

🏆 Project Outcome
Wellness Navigator AI demonstrates how AI, conversational workflows, and secure data infrastructure can be combined into a unified wellness platform.

The system brings together:

Physical Wellness
        +
Nutrition
        +
Mental Resilience
        +
AI Coaching
        +
Secure Data
        +
Adaptive Recommendations

into a single experience.

🌱 SDG 3 Connection
Good Health & Well-Being
Wellness Navigator AI contributes to the broader goal of improving access to personalized wellness support and encouraging healthier lifestyle practices.

Personalized Guidance
        ↓
Better Awareness
        ↓
Healthier Habits
        ↓
Preventive Wellness
        ↓
Improved Well-Being

📸 Screenshots
API Documentation
The project provides automatically generated FastAPI/OpenAPI documentation for the available backend endpoints.

Available endpoints
GET  /health
POST /coach
POST /sync

Wellness Dashboard
The dashboard provides:

Profile management

Wellness metrics

AI coach interaction

Milestone synchronization

Suggested actions

🔒 Disclaimer
Wellness Navigator AI is a wellness-support and educational project.

It is not a medical device, diagnostic system, emergency service, or substitute for a qualified healthcare professional.

Recommendations generated by the system should not be treated as medical diagnosis or treatment.

Users experiencing medical emergencies or serious mental-health concerns should contact an appropriate healthcare professional or emergency service.

👨‍💻 Development Philosophy
The project is built around the following philosophy:

Understand the user
        ↓
Ask only what is needed
        ↓
Adapt to their context
        ↓
Provide actionable guidance
        ↓
Protect their data
        ↓
Support long-term wellness

🤝 Contributing
Contributions are welcome.

To contribute:

Fork the repository

Create a feature branch

git checkout -b feature/your-feature

Commit your changes

git commit -m "Add your feature"

Push the branch

git push origin feature/your-feature

Open a Pull Request

📄 License
This project is available under the license specified in the repository.

If no license has been added yet, consider adding an appropriate open-source license before publishing the project for external contributions.

⭐ Acknowledgements
Built using:

React

FastAPI

LangGraph

Supabase

OpenAPI

with the goal of exploring how AI can provide more personalized, empathetic, and privacy-conscious wellness experiences.

🌿 Wellness Navigator AI
Empathy + Intelligence + Privacy
AI-driven personalized guidance for physical, nutritional, and mental well-being.

SDG 3 — Good Health & Well-Being 🌍
Built to help people stay informed, motivated, and on track with their wellness goals.

