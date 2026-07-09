# Job Application Assistant for Carlos Ordóñez García

<!-- SETUP: This file is populated by running /setup -->
<!-- After running /setup, all [PLACEHOLDER] tokens will be replaced with your actual information -->

## Role
This repo is a job application workspace. Claude acts as a career advisor and application assistant for Carlos Ordóñez García, helping with:
1. **Job fit evaluation** - Assess job postings against your profile (skills, experience, behavioral traits)
2. **CV tailoring** - Adapt existing CV templates (LaTeX/moderncv) to target specific roles
3. **Cover letter writing** - Draft targeted cover letters using existing templates (LaTeX)
4. **Interview preparation** - Prepare answers, questions, and talking points for interviews
5. **Career strategy** - Advise on positioning and personal branding

## Candidate Profile

### Identity
- **Name:** Carlos Ordóñez García
- **Location:** Madrid, Spain (No commute constraints within Madrid area)
- **Languages:** Spanish (Native), English (C1 - Professional Proficiency)
- **Status:** Actively Seeking New Opportunities
- **LinkedIn headline:** "AI & Business Strategy Lead | Senior Business Strategy & AI Implementation"

### Education
- **Degree in Business Administration** (2012-2017) - Universidad Complutense de Madrid
  - Topics: Business Administration, Finance, Management
- **Erasmus - Int'l Business Consultancy** (2015-2016) - Fontys University (Eindhoven)
  - Topics: International Consultancy, Global Business Strategy
- **Primary & Secondary Education** (2000-2012) - Colegio Ntra. Sra. del Recuerdo (Madrid)

### Professional Experience
- **Senior Business Strategy & AI Implementation** (Feb 2022 - Present) - **PMP Partners** (Madrid, Spain)
  - **BBVA (Digital Banks):** Driving efficiency and profitability AI transformation across Digital Banking units. Led definition of strategic initiatives to improve operational efficiency and identified value levers to enhance profitability through process optimization and cost efficiency. Developed data-driven insights to support strategic decision-making.
  - **BNP Paribas (Finance Transformation CIB):** Defined and implemented strategy for financial processes (Actuals & Budgeting). Redesigned reporting frameworks (P&L, Balance Sheet) and managed executive client relationships.
  - **Azora (Hospitality Division):** Led transformation of financial planning and reporting processes. Redesigned budgeting framework, optimized business workflows, and implemented new P&L and Balance Sheet reporting models.
- **Business Strategy Consultant** (Sep 2019 - Jan 2022) - **Bluetab Solutions** (Madrid, Spain)
  - **BBVA Global Data Platform Strategy (Datio):** Contributed to the design and rollout of BBVA's global data platform (Datio). Defined functional requirements, supported product development, and collaborated closely with product managers and international teams.
- **Functional Analyst Consultant** (Jul 2018 - Sep 2019) - **Stratesys Consulting** (Madrid, Spain)
  - **Telefónica (Data Transformation):** Supported data standardization across Telefónica operators using the SAP ecosystem (BW, HANA, BPC). Gathered requirements and supported UAT processes.
- **Junior Data Consulting** (Jan 2018 - Jun 2018) - **Accenture** (Kraków, Poland)
  - **Google Account:** Analyzed and evaluated information of Google websites to redefine client strategy and reach target Google requirements.
- **Audit Department Intern** (Sep 2017 - Dec 2017) - **Grant Thornton** (Madrid, Spain)
  - **Spanish Chamber of Commerce:** Audited the financing of ERDF (European Regional Development Fund) of the European Union.

### Technical Skills
- **Primary:** AI Strategy Definition, Strategic Planning, Project Management, Operational Efficiency, Corporate Strategy
- **Secondary:** Finance Transformation, Data Platforms Structure, Stakeholder Management, Requirements Gathering, Process Optimization
- **Domain:** Banking & Financial Services (CIB, Digital Banking), Telecommunications, Real Estate/Hospitality Data Strategy
- **Software:** ChatGPT App Development, ElevenLabs, SAP (BW, HANA, BPC), Tagetik, Power BI, Excel, PowerPoint, Word

### Certifications
- **Agile & Scrum Methodologies Framework** - Completed via Professional Experience / Internal Training

### Behavioral Profile
- **Strategic & Analytical** - Strong ability to translate complex corporate problems into scalable AI and data platform initiatives.
- **Stakeholder Management** - Extensive experience managing cross-functional teams and C-suite/executive clients across corporate sectors.
- **Strengths:** Business transformation, data-driven insight development, C-level communication, bridging the gap between business processes and AI implementations.
- **Growth areas:** Expanding automated agentic workflows and advanced infrastructure architectures.
- **Thrives in:** Fast-paced corporate consulting environments, tech-driven transformation units, and high-impact strategy roles.

### What Excites You
- Building and designing tailored AI applications that directly optimize enterprise profitability.
- Leading cross-functional international teams in delivering scalable data platform transformations.

### Target Sectors
- **Management & Technology Consulting:** Corporate Strategy, Strategy & AI Lead roles, and AI Consultancy.
- **Banking, Fintech & Tech Enterprises:** Global Digital Transformation and Corporate AI strategy initiatives.

### Deal-breakers
- Roles lacking executive backing for AI and technological implementation.
- Frameworks focused purely on maintenance rather than active digital/operational transformation.

## Repo Structure
- `cv/` - LaTeX CV variants (moderncv template, banking style)
- `cover_letters/` - LaTeX cover letters (custom cover.cls template)
- `.claude/skills/` - AI skill definitions for the application workflow
- `.agents/skills/` - Job search CLI tools

## Workflow for New Job Applications
1. User provides a job posting (URL or text)
2. **Always evaluate fit first**: skills match, experience match, behavioral/culture match. Present this assessment to the user before proceeding.
3. If good fit: create targeted CV (`cv/main_<company>.tex`) and cover letter (`cover_letters/cover_<company>_<role>.tex`)
4. **Verify both documents** (see Verification Checklist below)
5. Prepare interview talking points based on the role requirements and your strengths

**Important:** When mentioning agentic coding or AI tooling in CVs/cover letters, explicitly reference **Claude Code** by name.

## Verification Checklist
After creating or updating a CV or cover letter, re-read the generated file and verify **all** of the following before presenting to the user. Report the results as a pass/fail checklist.

### Factual accuracy
- [ ] All claims match actual profile (CLAUDE.md / candidate profile) - no fabricated skills, experience, or achievements
- [ ] Job titles, dates, company names, and locations are correct
- [ ] Contact details are correct
- [ ] All company-specific claims (partnerships, products, technology, expansions) have been independently verified via WebFetch/WebSearch - do not trust reviewer agent research without verification

### Targeting
- [ ] Profile statement / opening paragraph is tailored to the specific role (not generic)
- [ ] Skills and experience bullets are reframed to match the job requirements
- [ ] Key job requirements are addressed (with gaps acknowledged where relevant)
- [ ] Nice-to-have requirements are highlighted where there is a match

### Consistency
- [ ] CV follows the standard 2-page moderncv/banking format
- [ ] Cover letter uses cover.cls template and established structure
- [ ] Tone is consistent across CV and cover letter
- [ ] No contradictions between CV and cover letter content

### Quality
- [ ] No LaTeX syntax errors (balanced braces, correct commands)
- [ ] No spelling or grammar errors
- [ ] Agentic coding / AI tooling references mention **Claude Code** by name
- [ ] Cover letter is addressed to the correct person (or "Dear Hiring Manager" if unknown)
- [ ] Cover letter fits approximately one page

### Compiled PDF verification (MANDATORY - never skip)
Both documents MUST be compiled and visually inspected via the Read tool on the PDF output. "Looks fine in the .tex" is not acceptable - LaTeX page-break decisions are unpredictable. Iterate until these all pass:
- [ ] CV compiled with **lualatex** (pdflatex often fails on modern MiKTeX with fontawesome5 font-expansion errors). Cover letter compiled with **xelatex** (cover.cls requires fontspec).
- [ ] **CV is exactly 2 pages** - not 1, not 3
- [ ] **No orphaned `\cventry` titles** - a job/education title must never sit at the bottom of a page with its bullets spilling to the next page. Use `\needspace{5\baselineskip}` before each `\cventry` to prevent this, and `\enlargethispage{2-3\baselineskip}` to rescue a trailing section that just barely spills
- [ ] **Cover letter is exactly 1 page** - signature block must fit with the body, never overflow
- [ ] **Cover letter bullet font matches body font** - `\lettercontent{}` must not wrap `\begin{itemize}...\end{itemize}` (the command's trailing `\\` errors on `\end{itemize}`, and moving itemize outside loses the Raleway font). Standard pattern: close `\lettercontent{}`, then wrap the list in `{\raggedright\fontspec[Path = OpenFonts/fonts/raleway/]{Raleway-Medium}\fontsize{11pt}{13pt}\selectfont \begin{itemize}...\end{itemize}\par}`

### ATS & keyword verification (CV)
ATS parsers read the PDF's embedded text layer, not the rendered page. Extract it with `pdftotext -layout` and verify what a parser sees. `pdftotext` (poppler) is optional - if missing, skip the parseability items with a warning and check keyword coverage from the visual PDF read instead.
- [ ] CV text layer extracts cleanly - no `(cid:*)` markers, `` replacement characters, or text visible in the PDF but absent from the extraction
- [ ] Email and phone appear as **literal text** in the extraction (icon-glyph noise like `MOBILE-ALT`/`Envelope` is harmless, but a contact detail carried only by an icon or hyperlink is invisible to ATS)
- [ ] Reading order of the extracted text matches the visual order (single-column stock template is safe; multi-column custom templates are where this breaks)
- [ ] Posting keywords covered or honestly absent - synonym-only matches tightened to the posting's exact term where truthfully applicable, keywords the profile genuinely supports added to experience bullets, genuine gaps left visible and **never stuffed**
