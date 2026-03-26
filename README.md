**Project Overview**

This project demonstrates an automated data extraction pipeline for collecting promotional offers from a telecom mobile application.

**Key objectives**

Extract structured data from a dynamic mobile UI.

Handle app instability and session interruptions.

Deduplicate and clean data for downstream analysis.

Showcase data engineering best practices like batch processing, error handling, and logging.

**Architecture**
<img width="1536" height="1024" alt="Architecture" src="https://github.com/user-attachments/assets/608feffb-48ef-407f-87ac-149ebd7cb586" />

**Key Components**

Batch Processing: Restart session after N numbers to ensure stability.
Deduplication: Hash-based keys prevent duplicate offer capture.
Resiliency: Recovery logic ensures pipeline continues even if the app crashes or UI changes.
Dynamic Scrolling: Automatically detects end of offer list.

**Features**

Handles dynamic mobile UI layouts

Deduplicates duplicate offers in real-time

Logs each step for traceability

Batch-based processing with session restart for stability

Generates structured CSV for analysis

**Tech Stack**

Python 3.x

Appium / Selenium WebDriver

Android Emulator

CSV for input/output

Standard Python libraries: os, time, csv, datetime

**Key Engineering Learnings**

Error Handling: Handled missing elements, timeouts, and app crashes gracefully.

Batch Processing: Restarted automation session after N numbers for reliability.

Deduplication: Hash-based approach ensures only unique offers are stored.

State Recovery: Ensures pipeline can recover if the app navigates to an unexpected screen.

Dynamic Data Handling: Can handle variable number of offers per number.

Note: Numbers are anonymized for privacy.
