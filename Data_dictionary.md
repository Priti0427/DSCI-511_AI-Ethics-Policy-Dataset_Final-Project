# Dataset Overview

- Number of rows: 1,886 policy initiatives
- Number of columns: 26 variables describing national and regional AI-related policy initiatives and associated instruments

---

## Variables

### Policy initiative ID

- **Type:** Integer
- **Description:** Unique identifier of the policy initiative in the OECD STIP/OECD.AI database.

### Platform URL

- **Type:** String
- **Description:** URL to the initiative’s entry on the OECD.AI platform.

### English name

- **Type:** String
- **Description:** Official English-language title of the policy initiative.

### Original name(s)

- **Type:** String
- **Description:** Initiative name in the original language(s), if different from English.

### Country

- **Type:** String
- **Description:** Country or jurisdiction responsible for the initiative.

### Start date

- **Type:** Date (YYYY-MM-DD or year)
- **Description:** Start date or launch year of the initiative.

### Description

- **Type:** String
- **Description:** Short narrative description of the policy initiative’s content and scope.

### Theme area(s)

- **Type:** String (list; delimiter `;`)
- **Description:** High-level thematic areas (e.g., AI, digital government, research, skills) covered by the initiative.

### Theme(s)

- **Type:** String (list; delimiter `;`)
- **Description:** More specific themes or topics targeted by the initiative within the broader theme areas.

### Background

- **Type:** String
- **Description:** Context, motivation, or problem statement that led to the initiative.

### Objective(s)

- **Type:** String
- **Description:** Declared policy goals or objectives of the initiative.

### Target group type(s)

- **Type:** String (list; delimiter `;`)
- **Description:** High-level categories of target groups (e.g., firms, public sector, research organisations, citizens).

### Target group(s)

- **Type:** String (list; delimiter `;`)
- **Description:** Specific target groups or beneficiaries of the initiative (e.g., SMEs, start-ups, universities).

### Responsible organisation(s)

- **Type:** String (list; delimiter `;`)
- **Description:** Public bodies or organisations in charge of designing or implementing the initiative.

### Yearly budget range

- **Type:** String
- **Description:** Approximate annual budget range of the initiative, usually expressed as intervals in EUR.

### Has funding from private sector?

- **Type:** Boolean
- **Description:** Indicates whether private-sector funding contributes to the initiative’s budget (`TRUE`/`FALSE`).

### Public access URL

- **Type:** String
- **Description:** Publicly accessible URL with official information about the initiative (e.g., government page, legal text).

### Is a structural reform?

- **Type:** Boolean
- **Description:** Flags initiatives that constitute structural or systemic reforms rather than standalone programmes (`TRUE`/`FALSE`).

### Is evaluated?

- **Type:** Boolean
- **Description:** Indicates whether the initiative has been formally evaluated (`TRUE`/`FALSE`).

### AI Principle(s)

- **Type:** String (list; delimiter `;`)
- **Description:** OECD AI Principles or related ethical principles explicitly addressed or implemented by the initiative.

### AI Policy Area(s)

- **Type:** String (list; delimiter `;`)
- **Description:** Policy domains related to AI covered by the initiative (e.g., skills, innovation, governance, data).

### Policy instrument ID

- **Type:** Integer
- **Description:** Identifier of the associated policy instrument used within the initiative.

### Policy instrument type category

- **Type:** String
- **Description:** Broad category of the policy instrument (e.g., financial support, regulatory measure, information and coordination).

### Policy instrument type

- **Type:** String
- **Description:** Specific type of instrument within the category (e.g., grants, tax incentives, regulations, strategies).

### Policy instrument name

- **Type:** String
- **Description:** Name or label of the policy instrument as recorded in the STIP/OECD.AI database.

### Policy instrument mini-field(s)

- **Type:** String (list; delimiter `;`)
- **Description:** Detailed subject-matter fields or sub-areas addressed by the policy instrument (e.g., AI R&D, digital skills, data governance).
