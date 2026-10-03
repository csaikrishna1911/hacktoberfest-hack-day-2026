# Project Name

## Team / attendee

- Team name (if applicable):Tech_worriors
- Members and GitHub usernames:C.sai krishna(csaikrishna1911)
-                              Lade Kavya (LadeKavya)
- Profile links (optional):

## Challenge

Select the challenge you are entering:

- [ ] Best Open-Source AI Project
- [X] Best Use of Gemma 4
- [ ] Build on elah

If listing multiple categories, confirm eligibility with the organizers and complete evidence for each.

## Project links

- Public GitHub repository:https://github.com/csaikrishna1911/fixlens
- Open-source license (link to the license file):MIT License

## Problem and solution

FixLens is designed for developers, students, and technical users who encounter confusing coding, software, application, or system errors.

The problem is that error messages and screenshots often contain technical information that is difficult to understand, especially for beginners. Users may know that something is wrong but not understand the cause or the steps required to fix it.

FixLens turns a technical screenshot into an actionable troubleshooting plan.

Main workflow:

Screenshot/image of a technical problem
→ Gemma 4 multimodal visual analysis
→ Problem identification
→ Root-cause explanation
→ Quick fix
→ Step-by-step fix instructions
→ Prevention tips

The output is structured so users can understand what went wrong and what they can do next.

## Approach and technologies

FixLens is a React + Vite web application focused on multimodal technical troubleshooting.

The application sends the uploaded screenshot together with a troubleshooting instruction prompt to Gemma 4 through the Google Generative Language API. The model analyzes visible terminal output, error messages, dialogs, UI states, and other visual clues.

The primary model configured in the application is:

`gemma-4-26b-a4b-it`

The implementation also supports other Gemma 4 model identifiers and dynamically checks the available Gemma 4 models through the API. The response is requested as structured JSON containing the detected problem, explanation/root cause, quick fix, step-by-step solution, and prevention tips. The React interface then renders this structured result into separate UI sections. 

Technologies used:
- React
- Vite
- JavaScript
- CSS
- Gemma 4
- Google Generative Language API
- Browser File/Clipboard APIs

Gemma 4 was chosen because the core problem requires understanding screenshots rather than relying only on manually entered text. The multimodal input allows FixLens to extract visible error messages and contextual visual information directly from the screenshot.

AI-assisted development was used during implementation for code generation, debugging, refactoring, and UI development. The final application logic, integration, testing, and project decisions were reviewed and validated during development.

## Challenge evidence

### Best Open-Source AI Project

- Open-source/open-weight AI component and its role:
  Gemma 4 is the open/open-weight AI model used as the multimodal reasoning component for visual technical troubleshooting.

- Code link showing the integration:
  https://github.com/csaikrishna1911/fixlens/blob/main/src/services/aiService.js

- Agent Skill Open Standard compliance (if applicable):
  Not applicable.

- Original harness implementation or meaningful changes (if applicable):
  FixLens provides an original application harness around Gemma 4 for technical screenshot troubleshooting, including screenshot ingestion, multimodal API requests, structured diagnostic output, response parsing, error handling, and React-based result rendering.

### Best Use of Gemma 4

- Gemma 4 model identifier and Gemini API integration:
  `gemma-4-26b-a4b-it`

  FixLens calls the Google Generative Language API using the Gemma 4 model's `generateContent` endpoint. The request contains both a troubleshooting prompt and the uploaded screenshot as multimodal input.

- Code link showing the integration:
  https://github.com/csaikrishna1911/fixlens/blob/main/src/services/aiService.js

- Input and useful output; multimodal value where applicable:
  Input: A screenshot/image containing a technical problem such as a terminal error, coding error, application error, or system error.

  Gemma 4 visually analyzes the screenshot and produces structured diagnostic information including:
  - Problem detected
  - Error snippet
  - Environment/technology detected
  - Explanation and root cause
  - Quick fix
  - Step-by-step fix
  - Prevention tips

  The multimodal capability is important because the user does not need to manually copy or explain the error. FixLens can use the screenshot itself as the primary diagnostic evidence.

### Build on elah

Not applicable.

## Current status

- What works:
  - Screenshot upload and drag-and-drop
  - Clipboard image paste
  - Example/preset scenarios
  - Multimodal Gemma 4 analysis
  - Technical problem detection
  - Root-cause explanation
  - Quick fixes
  - Step-by-step troubleshooting instructions
  - Prevention tips
  - Structured response parsing
  - Error handling and analysis states
  - Copy/export and voice briefing features
  - Live API analysis and demonstration/offline fallback

- Known limitations / incomplete features:
  - The current prototype is primarily focused on screenshot-based technical troubleshooting.
  - The frontend currently communicates with the Google API directly, which is suitable for the hackathon prototype but would need a backend proxy for production API-key protection.
  - AI-generated troubleshooting commands should be reviewed by the user before execution.

- What you would improve next:
  - Add a secure backend API layer for production deployment.
  - Expand supported technical problem categories.
  - Add conversation/history so users can ask follow-up questions about an analyzed error.
  - Add automated evaluation datasets for measuring diagnostic accuracy.
  - Improve deployment and production security.

## Submission checklist

- [x] Project repository is public and links work.
- [x] Required challenge evidence is included.
- [x] Project uses an open-source license where required by the challenge.
- [x] Work and reused materials are represented honestly.
- [x] No API keys, tokens, passwords, or private data are included.
- [x] I followed the organizers' build window and submission instructions.
- [ ] Project repository is public and links work.
- [ ] Required challenge evidence is included.
- [ ] Project uses an open-source license where required by the challenge.
- [ ] Work and reused materials are represented honestly.
- [ ] No API keys, tokens, passwords, or private data are included.
- [ ] I followed the organizers' build window and submission instructions.
