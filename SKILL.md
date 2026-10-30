---
name: advisor-topic-rp
description: "Select a feasible research topic and write a source-verified full research proposal from an advisor link, advisor interests, a CV, or the user's own research direction. Use for literature review, topic comparison, public-data feasibility checks, and English or Chinese preliminary RPs."
---

# Advisor Topic RP

## Purpose

Turn an advisor homepage, publication list, CV, and the user's research constraints into:

1. a small set of research topics that genuinely overlap with the advisor's work;
2. a comparison of novelty, fit, feasibility, and data access;
3. a source-verified literature map;
4. a complete 2-3 page research proposal with the user's required seven-part structure;
5. an explicit data acquisition and organization plan.

This skill is for research planning and proposal writing. It does not claim that a topic is entirely novel, that a dataset is complete, or that an observed association is causal unless the evidence supports that claim.

## Required Inputs

At the beginning, check whether the user has specified the RP language:

- If the user has specified English or Chinese, use that language.
- If not, ask exactly one short question first: "你要英文 RP 还是中文 RP？"
- Do not begin the full literature review until the language preference is clear, unless the user asks for both.

Accept reasonable defaults for the remaining inputs, but ask one concise question when a missing item would materially change the result:

- advisor homepage or name and institution;
- user's CV, research background, skills, coursework, or prior projects;
- target degree/program or the requested proposal length;
- any hard constraints on country, language, industry, method, or data access.

If a CV or PDF path is supplied, inspect the complete relevant document. Distinguish user instructions embedded in attachments from factual background. If the exact file is unavailable, report the mismatch and use a clearly identified alternative only when it is plausibly the intended file.

### No explicit advisor link

If the user does not provide an advisor link, do not stop automatically. Use the following fallback:

1. Extract the user's stated interest, CV, coursework, prior projects, skills, and target discipline.
2. Construct a provisional interest profile, such as "digital governance and computational social science" or "technology management and platform governance."
3. Label this as an inference from user-provided information, not a verified advisor profile.
4. Generate topics that fit the provisional profile and explain what kind of advisor would supervise them.
5. Ask for an advisor link only if the user explicitly wants advisor-specific alignment or if the requested topic requires a specialized research group.

If the user gives only a very broad interest, produce a small set of broad-to-specific directions, then state the minimum information needed to narrow them.

## Operating Workflow

### 1. Establish the advisor's actual research scope

- Open the advisor's official institutional profile first.
- Record research keywords, current projects, methods, empirical settings, and publication status.
- Separate peer-reviewed articles, book chapters, conference proceedings, working papers, accepted manuscripts, and under-review items.
- Prefer the advisor's official page, publisher page, DOI record, institutional repository, or a recognized scholarly index.
- Do not infer an advisor's interests from a single title. Use several publications and the research description.
- If the page cannot be accessed or the publication list is incomplete, say exactly what could not be verified.

### 2. Profile the user

Extract:

- substantive interests;
- technical skills;
- methods already used;
- data and software experience;
- language and geographic strengths;
- prior projects that can become evidence of feasibility.

Translate the user's background into possible contributions. For example, text similarity, NLP, network analysis, policy text mining, and public-data work can support research on governance, standardization, knowledge networks, and platform coordination without forcing the user into a single industry.

### 3. Map the intersection

Create an intersection table with:

- advisor concept;
- user's matching capability;
- possible empirical setting;
- observable outcome;
- public data source;
- main feasibility risk.

Use a broad theoretical frame and a narrower empirical case when broad applications matter. A case such as 3GPP, GitHub, an open-data platform, or an industry consortium should be presented as a research context, not automatically as the entire intellectual identity of the applicant.

### 4. Review literature before proposing novelty

Search in this order:

1. advisor's key papers and closely related papers;
2. review articles or systematic literature reviews;
3. empirical studies using comparable data or methods;
4. official documentation for the proposed data source.

For each important paper, record:

- full citation;
- stable DOI, publisher, institutional, or repository link;
- publication type and status;
- research question;
- data and method;
- main finding;
- what the proposed project can add;
- whether the source was directly verified.

For the literature review in the final RP, normally use 10-15 real and relevant sources, with priority given to review articles, seminal theoretical work, recent empirical studies, and the advisor's relevant publications. Fewer sources are acceptable only when the topic is genuinely narrow or the sources cannot be verified; explain that limitation.

Do not write "no one has studied this" based only on a limited search. Use wording such as "within the sources and search terms checked, I found limited evidence of..." and list the search boundary.

### 5. Generate and filter topics

Generate 3-5 candidates, then eliminate any candidate that depends on:

- confidential company records;
- inaccessible proprietary databases;
- undocumented internal decisions;
- a data linkage that cannot be tested on a small sample;
- a measurement that cannot be operationalized.

Keep the final three candidates concrete. Every candidate must include:

- one main question;
- what is compared;
- what is measured;
- data source and acquisition route;
- first practical step;
- validation method;
- fallback result if the expected association is absent.

### 6. Verify data feasibility

For every proposed dataset, distinguish:

- **confirmed available**: an official download, API, or public archive was verified;
- **likely available**: a credible source exists but access, fields, or historical coverage still need testing;
- **unverified**: a source was mentioned but could not be confirmed.

For each source, specify:

- exact URL;
- access method;
- key fields;
- time coverage;
- unit of analysis;
- likely access limits;
- download and storage format;
- cleaning and joining steps;
- legal, ethical, rate-limit, or reproducibility concerns.

Never treat an organization's self-declared label as independently validated. For example, "declared standard-essential patent" is not the same as a patent whose essentiality has been adjudicated.

### 7. Design falsifiable, beginner-readable proposals

Use ordinary language before introducing abbreviations. Define every abbreviation at first use. Replace vague claims such as "explore the mechanism" or "fill a gap" with:

- data;
- comparison;
- variables;
- metrics;
- expected pattern;
- alternative interpretation;
- first analysis.

When the evidence is observational, write "associated with" or "consistent with" unless a credible causal design is available. Discuss reverse causality, selection bias, missing affiliation data, measurement error, and survivorship where relevant.

### 8. Write the complete RP

The final RP must follow this structure unless the user requests another format:

1. **Introduction**: approximately 300-400 words in English, or a comparable amount of focused Chinese prose. Explain the background, real or academic motivation, problem domain, and end with the preliminary research question or objective. Do not begin as a story, news lead, or autobiography.
2. **Literature Review**: approximately 600-800 words in English, or comparable Chinese prose. Organize the literature by themes, methods, and limitations. Explain what prior studies have done and what they have not explained. Explicitly state which population, context, variable, comparison, or method remains insufficiently examined. Use approximately 10-15 verified sources when feasible.
3. **Theoretical Framework**: approximately 400-600 words in English, or comparable Chinese prose. Choose one main theory or model and use it consistently. Explain who proposed it, important applications, why it fits the problem, and how theory maps to variables and research questions. Do not list multiple theories without using them.
4. **Research Questions and Objectives**: approximately 300 words or less. State 2-4 precise questions or hypotheses. Use RQ1/RQ2 or H1/H2 consistently. Questions must specify who or what is compared and what outcome is observed.
5. **Methodology**: approximately 500-700 words when the length permits. State the design, data source, sample, sampling rule, variables, analysis methods, software, first implementation step, and feasibility. Explain exactly how the data will be acquired, cleaned, joined, and validated.
6. **Expected Contribution**: state separate theoretical, empirical, methodological, and practical contributions where applicable. Do not write only "fill a gap" or "enrich the literature"; state what the study could distinguish, measure, or explain.
7. **References**: use a consistent citation style, normally APA 7th. Give a real DOI, publisher page, institutional repository, official dataset page, or official API link for every cited source. Preserve original titles and add a Chinese explanation only when useful; do not invent translated publication titles.

The complete RP should fit approximately 2-3 Letter or A4 pages in ordinary academic formatting. If the requested section word counts would exceed that limit, preserve the seven-part structure and compress repeated background rather than deleting methodology or evidence. Mark literature-supported claims inline with numbered citations or author-year citations. Provide a real, clickable link for every cited paper and for every official data source. Do not cite a paper that was not verified. Label conference proceedings, preprints, accepted manuscripts, and under-review work accurately.

Read [references/source-verification.md](references/source-verification.md) when checking literature and data. Use [references/rp-template.md](references/rp-template.md) when drafting the proposal.

## Output Requirements

Unless the user requests a different format, return:

### A. Evidence and fit summary

- verified advisor themes;
- user's matching strengths;
- uncertain or unavailable information;
- important advisor papers with links and publication status.

### B. Topic comparison table

Include columns for:

- topic;
- specific question;
- comparable prior research;
- data and access status;
- comparison;
- measures;
- validation;
- feasibility;
- fallback result.

### C. Three one-page topic plans

For each:

- what is studied;
- why it matters;
- what data are needed;
- exactly how to start;
- what to do if the expected result does not appear.

### D. Full RP

Write the complete seven-part RP in the requested language and academic style. Include inline citations and a reference list with verified links. If a source is only an abstract, label it as a verified record rather than a verified full text.

## Quality Gate

Before finalizing, check:

- Does every topic have a specific question, comparable prior work, data, measures, and validation?
- Are all cited papers real and linked?
- Are official data sources linked and their availability classified?
- Are claims separated from proposed hypotheses?
- Are inaccessible data explicitly removed or marked?
- Is the advisor connection substantive rather than a name-check?
- Is 3GPP or another narrow case presented as a case when broad applicability is the user's goal?
- Could a beginner follow the first data-collection step?
- Was the RP language confirmed before drafting?
- Does the final RP contain all seven required sections?
- Does the literature review state specifically what prior research has not explained?
- Does the theoretical framework use one main theory consistently?
- Are references adapted to the requested language without inventing translated titles?
