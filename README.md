# n8n Automation Workflows

This repository contains n8n workflows that I have designed and built for practical AI automation and business use cases. Each project combines n8n with external platforms and APIs to create a complete, reusable automation system.

The repository currently includes the following two workflows:

## 1. AI Restaurant Voice Assistant

An automation backend for an ElevenLabs Conversational AI restaurant agent. It handles table availability, new reservations, reservation modifications and cancellations, pickup or delivery orders, and human callback requests.

The workflow uses Google Sheets to store operational records and Gmail to notify restaurant staff. Five n8n webhook endpoints allow the ElevenLabs agent to perform these actions during live customer calls and return natural-language results to the caller.

**Technologies:** n8n, ElevenLabs Conversational AI, Google Sheets, Gmail, webhooks, and JavaScript.

[View the workflow](./restaurant-voice-assistant/)

## 2. Website RAG Customer Support Chatbot

A retrieval-augmented customer support system that converts website content into a searchable AI knowledge base. Firecrawl discovers pages, n8n cleans and chunks the extracted content, Google Gemini generates embeddings, and Pinecone stores the vectors for semantic retrieval.

A Gemini-powered support agent searches the Pinecone knowledge base before answering questions about services, pricing, policies, FAQs, contact details, and other indexed website information.

**Technologies:** n8n, Firecrawl, Google Gemini, Pinecone, RAG, vector embeddings, and JavaScript.

[View the workflow](./website-rag-customer-support/)

## Repository structure

Each workflow has its own folder containing:

- An importable n8n `workflow.json` file.
- A dedicated README with architecture, requirements, configuration, and setup instructions.
- Sanitized placeholders instead of private credentials or account-specific values.

## Using the workflows

1. Open the folder for the workflow you want to use.
2. Read its setup guide and prepare the required external services.
3. Import `workflow.json` into n8n.
4. Connect your own credentials and replace the configuration placeholders.
5. Test the workflow with non-production data before activating it.

## Security

No API keys, OAuth credentials, personal email addresses, private spreadsheet IDs, n8n instance IDs, or production webhook IDs are included in this repository. Users must provide their own credentials and secure all public endpoints before production use.

## Disclaimer

These workflows are provided as reusable examples and starting points. Review the logic, permissions, privacy requirements, API usage, and service costs before using them in a production environment.
