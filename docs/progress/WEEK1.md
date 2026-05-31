Career Agent OS — Week 1 MVP
Overview

This project is a personal AI-powered career operating system designed to automate and enhance the internship and job search process. The long-term vision is a multi-agent platform capable of monitoring job opportunities, managing networking relationships, tailoring resumes, tracking applications, identifying skill gaps, and providing career strategy recommendations.

Week 1 focused on building the foundational infrastructure and proving that the core AI workflow pipeline works end-to-end.

Week 1 Goals

The primary objective for Week 1 was to create a functioning MVP workflow that could:

Generate or ingest job data
Send the data to an LLM for analysis
Store the results in a database
Send automated notifications through Discord

This established the foundation for all future automation and agentic workflows.

Current Workflow
Manual Trigger
    ↓
Mock Job Data
    ↓
OpenAI Job Scoring
    ↓
Supabase Database Insert
    ↓
Discord Notification
Tech Stack
Infrastructure
Dedicated always-on MacBook
Docker Desktop
n8n (self-hosted)
AI
OpenAI API
GPT-4.1-mini
Database
Supabase (PostgreSQL)
Notifications
Discord Bot API
Development Tools
VS Code
Git
Homebrew
Node.js
Features Implemented
n8n Local Automation Server
Installed and configured Docker
Deployed n8n locally using Docker Compose
Verified local workflow execution
OpenAI Integration
Connected OpenAI API to n8n
Built first AI scoring workflow
Generated structured job evaluations
Supabase Integration
Created PostgreSQL jobs table
Connected Supabase credentials to n8n
Inserted AI-generated workflow data into database
Discord Bot Integration
Created Discord developer application
Configured bot permissions
Connected Discord API to n8n
Successfully sent automated AI-generated job notifications
Database Schema
create table jobs (
  id bigint generated always as identity primary key,
  title text,
  company text,
  location text,
  description text,
  ai_score integer,
  ai_reason text,
  created_at timestamp default now()
);
Example AI Output
{
  "score": 90,
  "reason": "Strong alignment with embedded systems and AI interests, reputable defense company, excellent for career growth with immediate income potential."
}
Key Concepts Learned
Workflow Orchestration

Understanding how automation systems pass data between services and APIs.

JSON Data Structures

Learning how AI APIs structure responses and how nested data is accessed programmatically.

API Authentication

Configuring credentials and securely handling API keys and tokens.

Database Permissions

Debugging PostgreSQL/Supabase access control and service role permissions.

AI System Architecture

Understanding that modern AI systems are largely orchestration, infrastructure, and integrations rather than just prompting.

Challenges Encountered
Docker and local environment setup
Supabase permissions and RLS configuration
Nested JSON parsing from OpenAI outputs
n8n expression syntax
Discord bot authentication and permissions
Mapping workflow data into database fields
Current Status

The system can now:

generate job analysis using AI
store structured data in a cloud database
automatically notify through Discord
orchestrate multiple services together in a functioning pipeline

Week 1 successfully established the technical foundation for the larger multi-agent career operating system.

Planned Next Steps
Week 2
Replace mock job data with real job feeds/APIs
Implement scheduled workflows
Improve AI scoring logic
Add application tracking
Future Features
Resume tailoring
Networking CRM
Recruiter tracking
LinkedIn/browser automation
Skill gap analysis
Multi-agent workflows
Personalized career strategy recommendations
Dashboard/frontend interface
Long-Term Vision

The long-term goal is to create an autonomous AI career operating system that acts as:

a networking assistant
a job discovery engine
an application manager
a personalized career strategist
a productivity automation platform

The system is intended to continuously monitor opportunities, recommend actions, automate repetitive tasks, and help maximize long-term career growth.