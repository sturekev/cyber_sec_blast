---
name: Google Slides Research Poster Builder
description: Use when converting a PowerPoint/example poster into a reusable Google Slides-style academic research poster format.
---

# Google Slides Research Poster Builder

## Purpose

This skill helps an AI analyze an existing PowerPoint, poster, or poster-content document and generate a similar academic research poster layout for Google Slides. It focuses on preserving the structure, visual hierarchy, section balance, and presentation style while adapting the content to a new topic.

Use this skill when the user asks to:
- Create a research poster based on an existing PowerPoint or poster example.
- Convert technical content into a Google Slides poster format.
- Generate a poster layout guide, slide structure, or reusable template instructions.
- Match the formatting style of an attached poster while changing the subject matter.

## Core Responsibilities

When this skill is active, the AI should:

1. Read the provided PowerPoint, poster, notes, or content package.
2. Identify the poster’s layout structure, including columns, title area, footer, image placement, section order, and design patterns.
3. Extract formatting conventions such as heading style, color use, text density, visual balance, and academic tone.
4. Generate a clear Google Slides poster plan that a user or AI can recreate.
5. Adapt the format to the user’s new topic without copying irrelevant content from the original example.
6. Keep the final poster suitable for academic, class, conference, or BLAST-style presentation use.

## Poster Analysis Procedure

When analyzing an example poster or PowerPoint, inspect the following:

### 1. Page and Canvas Setup

Determine or recommend:
- Poster orientation: landscape or portrait.
- Suggested Google Slides page size.
- Number of columns.
- Header height.
- Footer height.
- Whether the poster uses a grid-based layout.

If the poster size is not stated, recommend a standard academic poster setup:
- Landscape widescreen-style poster.
- Four-column layout for dense technical topics.
- Large title banner at top.
- References and QR codes in footer.

### 2. Header Area

The header should usually include:
- Project title.
- Student name.
- Course or program name.
- Institution name.
- Faculty sponsor or instructor if required.
- Optional logo area on left or right.

The title should be the largest text element on the poster and should clearly communicate the main technical topic.

### 3. Content Columns

For a technical research poster, use this general structure unless the example poster suggests otherwise:

#### Column 1: Problem, Background, and Motivation
Include:
- Abstract or overview.
- Problem statement.
- Why the topic matters.
- Key definitions.
- Context for the technology or system.

#### Column 2: Core Concepts and Technical Foundation
Include:
- Main theories, algorithms, protocols, or data structures.
- Important terminology.
- Diagrams or conceptual visuals.
- Short explanations rather than long paragraphs.

#### Column 3: System Architecture, Implementation, or Method
Include:
- Main architecture diagram.
- Workflow or pipeline.
- Layer mapping if networking or computing systems are involved.
- Tables that connect concept to implementation.

For QKD/Post-QKD topics, place the major architecture diagram here and make it the visual anchor of the poster.

#### Column 4: Results, Evidence, Limitations, and Future Work
Include:
- Benefits.
- Limitations.
- Real-world evidence or status table.
- Future work.
- Conclusion.

Benefits and limitations should appear physically near each other to show balanced analysis.

### 4. Footer Area

The footer should include:
- References in small academic format.
- GitHub QR code placeholder if applicable.
- YouTube/demo QR code placeholder if applicable.
- Course hashtag, project tag, or event tag if required.

Example footer items:
- IEEE-style references.
- GitHub QR.
- YouTube QR.
- Class/project hashtag.

## Visual Design Rules

Follow these design principles:

1. Use a consistent grid.
2. Align section boxes cleanly.
3. Use no more than two or three main colors.
4. Use one accent color for the primary technical system and one for the secondary system if comparing two planes or layers.
5. Keep headings visually consistent.
6. Avoid large walls of paragraph text.
7. Use bullets, tables, and diagrams for readability.
8. Place the most important diagram near the center or in the widest visual area.
9. Keep benefits and limitations balanced.
10. Include status labels such as deployed, emerging, experimental, or speculative when discussing technologies.

For QKD/Post-QKD posters:
- Use one accent color for the quantum plane.
- Use another accent color for the classical/network plane.
- Keep the color mapping consistent in every figure.
- Make clear that QKD operates at the physical/quantum layer.
- Make clear that PQC works over classical IP networks.
- Clearly distinguish raw keys, key IDs, key management entities, and public network traffic.

## Recommended Google Slides Build Instructions

When generating instructions for Google Slides, provide steps like these:

1. Open Google Slides.
2. Go to File > Page setup.
3. Choose Custom size.
4. Set the poster to a large landscape format, such as 48 x 27 inches or another required class size.
5. Create a full-width title banner at the top.
6. Add four vertical content columns below the title.
7. Add section boxes inside each column.
8. Insert diagrams, screenshots, architecture figures, or QR placeholders.
9. Add a footer strip for references and links.
10. Use consistent fonts, colors, spacing, and alignment.

## Output Format When Asked to Generate a Poster Guide

Return the guide using this structure:

```markdown
# Google Slides Poster Generation Guide

## 1. Poster Setup
- Size:
- Orientation:
- Grid:
- Columns:

## 2. Visual Style
- Font style:
- Color palette:
- Heading style:
- Body text style:
- Diagram style:

## 3. Header Layout
- Title:
- Author block:
- Institution/course block:
- Logo placement:

## 4. Column-by-Column Layout
### Column 1: [Name]
- Section:
- Section:
- Visual:

### Column 2: [Name]
- Section:
- Section:
- Visual:

### Column 3: [Name]
- Section:
- Section:
- Visual:

### Column 4: [Name]
- Section:
- Section:
- Visual:

## 5. Footer Layout
- References:
- QR codes:
- Tags:

## 6. Content Adaptation Rules
- What to preserve from the example:
- What to replace for the new topic:
- What to avoid:

## 7. Google Slides Construction Steps
1. ...
2. ...
3. ...
```

## Output Format When Asked to Generate Actual Poster Content

Return content in a slide-ready structure:

```markdown
# Poster Title

## Header
Author:
Course:
Institution:
Sponsor:

## Column 1: Background and Problem
### Abstract
...

### Problem Statement
...

### Motivation
...

## Column 2: Technical Foundation
### Key Concepts
...

### Core Mechanism
...

## Column 3: Architecture and Workflow
### Main Architecture Diagram Description
...

### Workflow
...

### Layer Mapping Table
...

## Column 4: Evidence, Limits, and Future Work
### Real-World Evidence
...

### Benefits vs. Limitations
...

### Future Work
...

### Conclusion
...

## Footer
References:
GitHub QR:
YouTube QR:
```

## QKD/Post-QKD Poster-Specific Guidance

If the poster topic is Quantum Key Distribution, Post-Quantum Cryptography, or Post-QKD networking, ensure the poster includes:

1. The harvest-now, decrypt-later threat.
2. The difference between symmetric and asymmetric cryptographic risk.
3. QKD physical-layer key generation.
4. Classical authenticated channel requirement.
5. PQC algorithms such as ML-KEM and ML-DSA where relevant.
6. ETSI QKD key delivery concepts such as SAE, KME, key pool, key_ID, and REST API.
7. Hybrid integration with protocols such as IKEv2, IPsec, or TLS when relevant.
8. A clear statement that QKD does not replace authentication.
9. A balanced limitations section covering distance, trusted nodes, cost, deployment complexity, and key starvation.
10. A future-work section covering QKD networks, satellite QKD, QDS, or hybrid PQC/QKD adoption.

## Quality Checklist

Before finalizing, verify:

- The poster has a clear academic title.
- The layout is visually balanced.
- Each column has a distinct purpose.
- The main diagram is easy to find.
- Technical claims are accurate and not exaggerated.
- Emerging technologies are labeled as deployed, emerging, experimental, or speculative.
- Benefits and limitations are both included.
- References are included.
- Placeholder fields are clearly marked if information is missing.
- The poster can be recreated in Google Slides without needing specialized design software.

## What to Avoid

Avoid:
- Copying the old poster topic when the user asks for a new topic.
- Overcrowding the poster with long paragraphs.
- Using too many colors or inconsistent styles.
- Making unsupported technical claims.
- Treating speculative technologies as fully deployed.
- Omitting limitations.
- Creating a poster that looks like an essay pasted onto a slide.
- Ignoring the visual style of the provided PowerPoint or example poster.

## Default Recommendation

If the user does not specify a required poster format, use a four-column academic research poster with:
- Top title banner.
- Four content columns.
- One large central architecture or workflow visual.
- Benefits and limitations side-by-side.
- Status or evidence table.
- Footer with references and QR placeholders.

The final output should be practical, slide-ready, and easy to rebuild in Google Slides.