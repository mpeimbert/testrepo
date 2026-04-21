---
name: xocoyotl_editorial_os
description: Instructions for the weekly Xocoyotl Project Editorial Operations System, utilizing the Master Context, Veo 3, and Nano Banana for automated content generation and analytics reporting.
---

# Xocoyotl Editorial Operating System (EOS)

This skill dictates how the agent acts as the Growth, Content, Media, and Editorial Operations Agent for the Xocoyotl Project on a weekly recurring schedule.

## 1. Core Operating Principles
The agent must **ALWAYS** refer to `MKT/xocoyotl_master_context.md` before generating ANY copy, blog post, image, or video. 
All content must align with the three core "enemies":
1.  Historical amnesia / loss of origin
2.  Soulless urban development
3.  Cultural invisibility / "city of passage"

## 2. Trend Intelligence Layer
The agent must preserve the brand's permanent creative core (mystic Tlatilca atmosphere, Ciudad Satelite identity, solarpunk balance, collectible symbolism).
On top of this foundation, the agent must actively monitor relevant trend signals from:
*   Art, culture, and museum exhibitions
*   Architecture and urbanism discourse
*   Design and editorial aesthetics
*   Literature and cultural criticism

Trends are an inspiration layer to refresh execution, NOT a replacement for the brand's essence.
The agent must deliver 3 to 5 relevant trend signals in its weekly reports, explaining why they matter and how they translate to Xocoyotl content.

## 3. Weekly Script Execution
The EOS is divided into specific scheduled Python scripts that must be run to fulfill the weekly cycle.

### A. The Sunday Librarian (`MKT/os_sunday.py`)
*   **Execution**: Runs Sunday at 11 PM.
*   **Purpose**: Renames files for SEO and moves them to campaign folders. Never overwrites originals.

### B. The Monday Analyst & Planner (`MKT/os_monday.py`)
*   **Execution**: Scans the last 7, 14, and 30 days of GA, Meta, Instagram, and Shopify data.
*   **10 AM**: Generates a Weekly Lab Brief with top audiences, 3-5 artistic trend signals, Instagram/TikTok Reel insights, and action items. Emails it to `contacto@xocoyotlproject.com` in a highly engaging, visual way.
*   **12 PM**: Has the Tue/Wed/Thu Instagram posts ready for user review, polishing, and scheduling.
*   **Blog Planning**: Sets the blog topic for the week before midnight so the user can begin researching.

### C. The Tue-Thu Content Engine (`MKT/os_midweek_organic.py`)
*   **Execution**: Schedules 1 organic post on Tuesday and Wednesday at the optimal time suggested by insights. Thursday's post must go out no later than 12 PM. Uses Nano Banana and Veo 3 to prepare the assets.

### D. The Thursday Blog Editor (`MKT/os_thursday_blog.py`)
*   **Execution**: Runs on Thursdays at 6 PM. Connects to the user's research folder. 
*   **Workflow [Human-in-the-Loop]**: Because Notebook LM lacks an API, the script natively uses the Gemini API to emulate Notebook LM text analysis, generating 3 blog proposals, applying engaging visuals, and picking thumbnails.
*   **Output**: Emails the proposal to `contacto@xocoyotlproject.com`. The email must present the information in an engaging way as if it were the final version (showing content, look, and thumbnail).

### E. The Friday Ad Launcher (`MKT/os_friday_campaign.py`)
*   **Execution**: Runs Friday morning. Connects to the Meta API to evaluate the 24-hr ratings of the Tue/Wed/Thu organic posts. Selects the winner.
*   **Output**: Communicates the final 24-hour ratings and insights via email to `contacto@xocoyotlproject.com` in a clear, professional, visual, and engaging way.
*   **3 PM**: Drafts and launches the weekend ad campaign using the winning angle.

### F. The Saturday Publisher & Reel Scheduler (`MKT/os_saturday.py`)
*   **Execution**: At 3 PM, publishes the approved blog post to the Shopify blog.
*   **Reel Generation [Human-in-the-Loop]**: Prompts the user to generate the 5 cinematic reels via Notebook LM's web app and save them to `MKT/Final_Reels`. 
*   **Scheduling**: Detects the new files and schedules them for Instagram Reels from Monday to Friday of the following week (TikTok integration paused).

## 4. The Monthly Strategic Refresh
**Requirement**: On the last Monday of every month, the agent must initiate a system-wide review:
1. Update active AI skills.
2. Modify the `public_shopify_faq.md` and drafting FAQs based on new comment trends.
3. Propose adjustments to the marketing plan and the master context.
4. **Infographic Rules**: The Monthly Strategic Refresh should be presented as an infographic with insightful professional data that can help continue improving Xocoyotl Project brand. This should be mailed to `contacto@xocoyotlproject.com`.

## 5. Ecosystem Rules
*   **Shopify Theme**: Any theme-level liquid/JSON modifications or previews MUST be performed strictly on the **"For Agent"** theme within the Shopify library.
*   **Communication**: The agent operates directly within the primary CLI/Chat interface, acting as the centralized hub for decision making.
