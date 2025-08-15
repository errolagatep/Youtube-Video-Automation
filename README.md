YouTube Video Automation Workflow

This repository contains an automated YouTube content creation pipeline built using n8n. The workflow handles idea generation, content planning, prompt creation, video assembly, and publishing — all with minimal manual intervention.

📌 Overview

This workflow is designed to:

1. Generate content ideas automatically on a schedule.

2. Plan and store ideas in a Google Sheet for tracking.

3. Format prompts for media generation.

4. Create and assemble video clips with sounds.

5. Upload the final video to YouTube and log it back to the sheet.


The process is fully automated using:

1. OpenAI Chat Models for idea generation and planning.

2. Wavespeed API for video clip creation.

3. FAL API for sound generation and video sequencing.

4. Google Sheets for logging ideas and outputs.

5. YouTube Upload API for publishing.


⚙️ Workflow Steps

1. Schedule Trigger - Initiates the workflow at defined intervals.

2. Idea Generator - Uses OpenAI to generate video content ideas.

3. Planning Agent - Refines ideas and prepares structured prompts. Logs ideas into Google Sheets.

4. Prompting Agent - Formats prompts for downstream APIs.

5. Media Creation

    - Create Wavespeed Clips → Wait until ready.

    - Generate Sounds with FAL API → Wait until ready.

    - Sequence Video by merging clips and sounds.

6. Publishing - Uploads final video to YouTube. Updates Google Sheets with the published link.


🗂️ Tech Stack

n8n – Workflow automation engine

OpenAI API – Idea and script generation

Google Sheets API – Idea logging and tracking

Wavespeed API – Video clip creation

FAL API – Sound generation and video sequencing

YouTube Data API – Video publishing


📋 Requirements

n8n instance

API keys for:

OpenAI

Google Sheets

Wavespeed

FAL

YouTube Data API