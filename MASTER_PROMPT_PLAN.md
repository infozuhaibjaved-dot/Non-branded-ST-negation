# Master Prompt Plan — YouTube Content Creation Pipeline

## Overview

This document outlines the complete plan for building a **3-stage master prompt system** that takes competitor analysis insights and produces high-quality, viral-ready YouTube scripts. The pipeline flows as:

**Title Generation → Outline Generation → Script Generation**

Each stage's output feeds directly into the next stage as input.

---

## Competitor Channels for Analysis

| # | Channel URL | Purpose |
|---|-------------|---------|
| 1 | https://www.youtube.com/channel/UCFoGLU_SSf812tyOs3XGa_Q | Competitor analysis |
| 2 | https://www.youtube.com/channel/UCSGx8QZp__jnMf1JjBSLZXQ | Competitor analysis |
| 3 | https://www.youtube.com/channel/UCvKcmG5CPNAYdVXOLoJ4tow | Competitor analysis |
| 4 | https://www.youtube.com/channel/UCWhS0dkpQcB76Pdusz78leg | Competitor analysis |
| 5 | https://www.youtube.com/channel/UCUauz7dvekz4zL9XoXP2rBQ | Competitor analysis |
| 6 | https://www.youtube.com/channel/UCSoQs-drMuFDjJAQTkmPHEw | Competitor analysis |
| 7 | https://www.youtube.com/channel/UCQJ_ewnSqrpFjHWmIHEoZbw | Competitor analysis |
| 8 | https://www.youtube.com/channel/UCvbm6K5cbK4Ik7Vd293HjXw | Competitor analysis |
| 9 | https://www.youtube.com/channel/UCvbm6K5cbK4Ik7Vd293HjXw | Competitor analysis (duplicate of #8 — replace with a unique channel) |
| 10 | https://www.youtube.com/channel/UCw96Gp68WK6Vppr4k-yI2pw | Competitor analysis |

**Note:** Channel #9 is a duplicate of #8 from the original list — replace with a unique competitor channel before starting analysis. Channels include a mix of high-performing (viral) and low-performing (low views) channels — both are needed to identify success vs. failure patterns.

---

## Phase 1: Competitor Deep Analysis Framework

Before building the 3 master prompts, we need a structured competitor analysis. This analysis will be embedded as context/reference data inside each master prompt.

### 1.1 Data Points to Extract Per Channel

For each of the 10 competitor channels, extract:

#### Video Performance Data
- **Top 10 Most Popular Videos** (all-time by views)
- **Top 10 Recent Videos** (last 30–90 days by views)
- **Lowest Performing Videos** (bottom 10 by views) — for failure analysis
- **Average views per video** (channel-level benchmark)
- **View velocity** — how fast videos gain views in first 24h, 48h, 7 days

#### Title Analysis
- Full titles of top-performing vs. low-performing videos
- Title length (character count and word count)
- Title structure patterns (question format, list format, how-to format, curiosity gap, etc.)
- Power words used (shocking, secret, nobody tells you, etc.)
- Keyword placement (primary keyword position in title)
- Emotional triggers in titles
- Use of numbers/statistics in titles
- Capitalization patterns

#### Thumbnail Patterns (for context, not prompt generation)
- Face vs. no-face
- Text on thumbnail vs. no text
- Color schemes
- Emotion displayed

#### Topic Analysis
- Topic categories and niches covered
- Topic uniqueness score (saturated vs. non-saturated topics)
- Topic timing (trending vs. evergreen)
- Topic overlap between high-view and low-view channels
- Gaps: topics covered by viral channels but missed by low-performing ones

#### Script/Transcript Analysis
- Total script word count (proxy for video length)
- Hook structure (first 30 seconds — exact words used)
- Script pacing (short paragraphs vs. long blocks)
- Storytelling techniques used
- Vocabulary level (simple vs. complex)
- Call-to-action placement and frequency
- Pattern interrupts (how often and what type)
- Retention techniques (open loops, cliffhangers, teasers)
- Information density (facts per minute)

#### Video Length Analysis
- Duration of top-performing videos (in minutes)
- Duration of low-performing videos
- Sweet spot duration range for the niche
- Correlation between length and views

#### Upload Patterns
- Upload day of week
- Upload time of day
- Upload frequency (videos per week/month)
- Correlation between upload timing and initial view velocity

### 1.2 Success vs. Failure Pattern Matrix

After extracting the above data, build a comparison matrix:

| Factor | Viral Videos (High Views) | Failed Videos (Low Views) | Key Difference |
|--------|--------------------------|--------------------------|----------------|
| Title length | ? | ? | ? |
| Title structure | ? | ? | ? |
| Topic type | ? | ? | ? |
| Script hook | ? | ? | ? |
| Video duration | ? | ? | ? |
| Upload timing | ? | ? | ? |
| Vocabulary | ? | ? | ? |
| Retention techniques | ? | ? | ? |

### 1.3 Viral Factor Identification

Identify and rank the factors that contribute to virality:

1. **CTR Factors** (what makes people click):
   - Title curiosity gap
   - Title relevance to trending search queries
   - Emotional triggers in title
   - Power words and numbers

2. **AVD Factors** (what keeps people watching):
   - Hook quality (first 5–30 seconds)
   - Open loops and pattern interrupts
   - Story structure and pacing
   - Information value density
   - Script energy and vocabulary

3. **YouTube Algorithm Factors** (what makes YouTube push the video):
   - High CTR + High AVD combination
   - Session time contribution
   - Audience retention curve shape
   - Engagement signals (likes, comments, shares)

---

## Phase 2: Three Master Prompts — Detailed Plan

### Master Prompt #1: Title Generation

**Purpose:** Generate high-CTR, algorithm-friendly video titles based on competitor insights and topic input.

#### What This Prompt Must Include:

1. **Role Definition**
   - AI acts as a YouTube title strategist with deep knowledge of CTR optimization

2. **Competitor Context (Embedded)**
   - Summary of title patterns from viral competitor videos
   - Summary of title patterns from failed competitor videos
   - List of power words that worked in the niche
   - Title structures that consistently perform (backed by data)

3. **Input Required from User**
   - Target topic/keyword
   - Target audience description
   - Content angle/unique hook (optional)

4. **Title Generation Rules**
   - Character limit: 60–70 characters max
   - Must include primary keyword in first 5 words
   - Must use at least one proven power word from competitor analysis
   - Must create curiosity gap or emotional trigger
   - Must avoid clickbait that doesn't deliver (trust factor)
   - Generate 10 title variations per topic
   - Each variation should use a different title structure (question, list, how-to, curiosity gap, contrast, etc.)

5. **Output Format**
   - 10 title options, ranked by estimated CTR potential
   - For each title: brief explanation of WHY it should work (which viral pattern it follows)
   - Recommended top 3 picks with reasoning

6. **Quality Checks**
   - No generic/overused titles
   - Each title must be differentiated from competitors' existing titles
   - Titles must match the audience's language level (simple, relatable)

---

### Master Prompt #2: Outline Generation

**Purpose:** Take the selected title from Prompt #1 and generate a detailed video outline optimized for audience retention (AVD).

#### What This Prompt Must Include:

1. **Role Definition**
   - AI acts as a YouTube content strategist specialized in audience retention and video structure

2. **Competitor Context (Embedded)**
   - Winning script structures from viral competitor videos
   - Hook formulas that achieved highest retention
   - Pattern interrupt techniques used by top performers
   - Average video duration sweet spots for the niche
   - Retention curve insights (where viewers drop off and how viral videos prevent it)

3. **Input Required from User**
   - Selected title (output from Prompt #1)
   - Target video duration (e.g., 8–12 minutes)
   - Key points/facts to cover (optional)
   - Target audience specifics

4. **Outline Structure Rules**
   - **Hook Section** (0:00–0:30): Exact hook type to use, word count target: 50–80 words
   - **Introduction/Setup** (0:30–1:30): Context setting, word count target: 100–150 words
   - **Main Content Sections** (3–5 sections): Each with:
     - Section title
     - Key points to cover
     - Retention technique to use (open loop, story, data reveal, etc.)
     - Estimated word count per section: 200–350 words each
     - Pattern interrupt placement (every 2–3 minutes)
   - **Climax/Key Revelation**: The biggest value drop or revelation
   - **CTA + Outro** (last 30–60 seconds): Word count target: 50–100 words
   - **Total target word count** for the full outline: specified based on video duration
     - 8 min video ≈ 1,200–1,400 words outline
     - 10 min video ≈ 1,500–1,800 words outline
     - 12 min video ≈ 1,800–2,100 words outline
     - 15 min video ≈ 2,200–2,600 words outline

5. **Output Format**
   - Timestamped outline (approximate timestamps)
   - Section-by-section breakdown with:
     - Section purpose
     - Key talking points (3–5 per section)
     - Retention technique used
     - Word count target for that section
   - Open loops: where to place them and what they tease
   - Pattern interrupts: exact placement and type

6. **Quality Checks**
   - Outline must maintain viewer curiosity throughout
   - No section should be pure filler
   - Every section must deliver clear value
   - The flow must be logical — each section builds on the previous one
   - Must include at least 2 open loops and 3 pattern interrupts

---

### Master Prompt #3: Script Generation

**Purpose:** Take the outline from Prompt #2 and write a full, production-ready script optimized for engagement.

#### What This Prompt Must Include:

1. **Role Definition**
   - AI acts as an expert YouTube scriptwriter who writes conversational, engaging scripts that maximize watch time

2. **Competitor Context (Embedded)**
   - Vocabulary patterns from viral scripts (simple vs. complex words ratio)
   - Sentence structure patterns (short punchy sentences vs. long explanations)
   - Hook word-for-word examples from top-performing videos
   - Storytelling frameworks used by viral competitors
   - Energy/tone patterns (casual, authoritative, excited, etc.)

3. **Input Required from User**
   - Complete outline (output from Prompt #2)
   - Tone/voice preference (casual, professional, energetic, etc.)
   - Any specific facts/data points to include
   - Target audience reading/comprehension level

4. **Script Writing Rules**

   **Word Count Controls (CRITICAL):**
   - Total script word count must match the outline's target
   - Each paragraph: 30–60 words maximum (short, punchy)
   - Each sentence: 8–18 words maximum (conversational length)
   - Hook section: exactly 50–80 words
   - No section should exceed its allocated word count from the outline by more than 10%

   **Writing Style Rules:**
   - Conversational tone — write as if talking to one person
   - Use "you" and "your" frequently (direct address)
   - Short paragraphs (2–3 sentences max per paragraph)
   - Use transition phrases between sections
   - Include verbal pattern interrupts ("But here's the thing...", "Now, this is where it gets interesting...")
   - Use power words from competitor analysis
   - Avoid jargon unless the audience expects it
   - Reading level: Grade 6–8 (accessible to wide audience)

   **Retention Techniques in Script:**
   - Open loop in first 15 seconds ("By the end of this video, you'll know...")
   - Re-hook every 2–3 minutes with a mini curiosity gap
   - Payoff all open loops before the video ends
   - Use stories/anecdotes to illustrate points
   - Include surprising facts or counterintuitive information
   - Place the biggest value bomb at 60–70% through the video (reward for watching)

   **Engagement Triggers:**
   - Ask at least 2 questions to the viewer
   - Include 1 CTA for likes/comments in the middle (not just at the end)
   - End with a strong CTA + teaser for next video

5. **Output Format**
   - Full script with clear section headers matching the outline
   - [HOOK] section clearly labeled
   - [PATTERN INTERRUPT] markers where energy/approach shifts
   - [B-ROLL SUGGESTION] notes for visual cues (optional)
   - Word count displayed per section and total
   - Estimated video duration based on word count (assuming ~150 words/minute speaking rate)

6. **Quality Checks**
   - Script must read naturally when spoken aloud
   - No repetitive phrases or filler content
   - Every sentence must either inform, entertain, or create curiosity
   - The script must stay on-topic (no tangents)
   - Must follow the exact outline structure — no skipping sections
   - Final word count must be within ±5% of the target

---

## Phase 3: Workflow Pipeline

```
┌─────────────────────────┐
│  USER INPUT:            │
│  - Topic/Keyword        │
│  - Target Audience      │
│  - Video Duration       │
└──────────┬──────────────┘
           │
           ▼
┌─────────────────────────┐
│  MASTER PROMPT #1       │
│  Title Generation       │
│                         │
│  Output: 10 titles      │
│  User picks best title  │
└──────────┬──────────────┘
           │ (selected title)
           ▼
┌─────────────────────────┐
│  MASTER PROMPT #2       │
│  Outline Generation     │
│                         │
│  Output: Detailed       │
│  timestamped outline    │
│  with word counts       │
└──────────┬──────────────┘
           │ (complete outline)
           ▼
┌─────────────────────────┐
│  MASTER PROMPT #3       │
│  Script Generation      │
│                         │
│  Output: Full script    │
│  ready for recording    │
└─────────────────────────┘
```

### Data Flow Between Prompts

| From | To | What Gets Passed |
|------|----|-----------------|
| User | Prompt #1 | Topic, audience, optional angle |
| Prompt #1 | User | 10 ranked titles with reasoning |
| User | Prompt #2 | Selected title + video duration + optional key points |
| Prompt #2 | User | Complete outline with timestamps, word counts, retention techniques |
| User | Prompt #3 | Full outline + tone preference + any additional facts |
| Prompt #3 | User | Production-ready script with section markers and word counts |

---

## Phase 4: Word Count & Duration Reference Table

This table will be embedded in Prompts #2 and #3 to maintain consistency:

| Target Video Duration | Total Script Words | Hook Words | Intro Words | Main Sections (count × each) | Outro Words | Paragraphs Max Words | Sentences Max Words |
|----------------------|-------------------|------------|-------------|------------------------------|-------------|---------------------|-------------------|
| 5 minutes | 750 | 50 | 80 | 3 × 180 = 540 | 80 | 40 | 15 |
| 8 minutes | 1,200 | 60 | 120 | 4 × 220 = 880 | 140 | 50 | 18 |
| 10 minutes | 1,500 | 70 | 150 | 4 × 280 = 1,120 | 160 | 50 | 18 |
| 12 minutes | 1,800 | 80 | 150 | 4 × 340 = 1,360 | 210 | 60 | 18 |
| 15 minutes | 2,250 | 80 | 180 | 5 × 350 = 1,750 | 240 | 60 | 18 |
| 20 minutes | 3,000 | 80 | 200 | 5 × 480 = 2,400 | 320 | 60 | 18 |

*(Based on average speaking rate of ~150 words per minute)*

---

## Phase 5: Anti-Hallucination & Quality Safeguards

Each master prompt will include these safeguards:

1. **No Assumptions Rule**: AI must only use information explicitly provided in the prompt context or by the user — no making up statistics, facts, or claims
2. **Source Tagging**: When referencing competitor patterns, the prompt will specify which patterns are from data analysis vs. general best practices
3. **Explicit Constraints**: Every measurable element (word count, sentence length, number of sections) will have hard limits defined
4. **Output Validation Instructions**: Each prompt will instruct the AI to self-check its output against all constraints before delivering
5. **Structured Output Format**: All outputs follow a strict template — reducing room for the AI to go off-track
6. **Context Completeness**: All necessary competitor insights, niche-specific vocabulary, audience details, and structural rules are embedded directly in the prompt — leaving nothing for the AI to "guess"

---

## Next Steps (After Plan Approval)

1. **Step 1**: Perform the actual competitor analysis on the 10 channels (Phase 1) — extract all data points listed above
2. **Step 2**: Build the Success vs. Failure Pattern Matrix
3. **Step 3**: Write Master Prompt #1 (Title Generation) with competitor data embedded
4. **Step 4**: Test Prompt #1 with 5 different topics — evaluate title quality
5. **Step 5**: Write Master Prompt #2 (Outline Generation) with competitor data embedded
6. **Step 6**: Test Prompt #2 with titles from Step 4 — evaluate outline quality
7. **Step 7**: Write Master Prompt #3 (Script Generation) with competitor data embedded
8. **Step 8**: Test full pipeline end-to-end — Topic → Title → Outline → Script
9. **Step 9**: Refine all 3 prompts based on output quality
10. **Step 10**: Finalize and document the complete master prompt system

---

*This plan focuses exclusively on the strategic framework. The actual competitor data collection and prompt writing will happen in the next phase after this plan is reviewed and approved.*
