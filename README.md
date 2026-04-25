# Twitch Real-Time Lead Generation Engine ⚡

## The "Speed to Lead" Problem

In 2026, business agility is the ultimate competitive advantage. When a business identifies high-potential leads, serving them an offer at the exact moment of need is critical. Waiting hours or days results in lost opportunities.

## Project Overview

This automation engine scans live Twitch streams to identify creators that fit specific business criteria. It goes beyond basic API data by scraping profile HTML to find direct contact information and social presence indicators.

## Key Features

Real-Time Discovery: Automated hourly triggers to find live streamers based on language and engagement.

Advanced Data Enrichment: Uses Regex-based HTML scraping to extract:

Business Emails

Social Links (YouTube, Discord, Instagram, TikTok)

Streamer Bios

Intelligent Lead Scoring: A custom JavaScript logic-based system that ranks leads (e.g., +5 for direct email, +3 for high viewer count, +2 for established tiers).

Production-Ready Resilience: * Node-Level Retries: Built-in 3x retry logic for network stability.

Human-Like Interaction: Dynamic "Wait" nodes with randomized intervals (3–10s) to avoid rate limits.

Global Error Handling: Dedicated error-trap workflows for high availability.

Centralized Dashboard: Clean data delivery to Google Sheets using "Upsert" logic (Match on Login) to prevent duplicate entries.

## Technical Stack

Orchestration: n8n

Languages: JavaScript (Node.js), Regex

API: Twitch Helix API

Storage: Google Sheets API

Security: Environment Variables and encrypted n8n Credentials

## Workflow Architecture

The workflow utilizes a parallel-branching strategy:

Top Branch: Fetches raw HTML profile data.

Bottom Branch: Preserves core API metadata.

Merge Node: Synchronizes both branches by index to create a unified lead profile.

## How to Use

Import: Download and import the **Twitch Leads Generation V2.json** file into your n8n instance.

Setup Credentials: Create and link your Twitch API and Google Sheets credentials.

Configure Variables: Set your sheetId and twitchClientId in the "Edit Fields" (Setup) node.

Activate: Turn on the workflow to begin real-time lead ingestion.

## Project Artifacts

- **Twitch Leads Generation V2.json**: The complete n8n workflow export
- **WorkFlow.jpg**: Visual diagram of the workflow architecture
- **Output.jpeg**: Sample output from the Google Sheets dashboard

Special thanks to Eng. Kareem for the foundational automation insights and guidance throughout this project.

#DataEngineering #Automation #n8n #LeadGeneration #AI #BusinessIntelligence
