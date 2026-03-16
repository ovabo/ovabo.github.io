---
layout: page
title: Projects
permalink: /projects/
---

# Projects

Everything I build connects to the same problem: psychiatric care is broken across the diagnostic, administrative, and policy layers simultaneously. Fixing any one layer without addressing the others does not work. These projects attack different parts of that system.

---

## Project overview

| Area            | Project / Item                              | One-line description                                                                 | Link                     |
|-----------------|---------------------------------------------|--------------------------------------------------------------------------------------|--------------------------|
| Clinical tech   | Stratification Labs                         | Studio for clinical tools that stratify psychiatric patients before treatment.      | —                        |
| Clinical tech   | Psykick                                     | Automates the administrative work that consumes psychiatrists' time and attention.  | [View Psykick](https://psykicksv1.vercel.app/) |
| Clinical tech   | Psychify                                    | Uses foundation models to stratify biotypes and predict treatment response at day zero. | [View Psychify](https://psychify-dz8w.vercel.app/) |
| Patient access  | Project Jatoria                             | Navigator for understanding and accessing mental healthcare services.               | [View Project Jatoria](https://jt-app.vercel.app/) |
| Research        | BH Spending & Access (HPD)                  | Links behavioral health spending to access and facility supply in California.       | —                        |
| Research        | Low-Value Psychiatric Care                  | Quantifies overuse of pharmaceuticals vs lower-cost alternatives in inpatient psych. | —                       |
| Research        | Medicaid BH Fraud Vulnerability             | Tests fraud patterns in Medi-Cal behavioral health services.                        | —                        |
| Research        | Autism Centers & Medicaid Funding           | Examines how autism centers are funded through Medicaid and distributed across states. | —                     |
| Tools           | Psychiatric Hospital Review Scraper         | Scrapes and analyzes patient reviews of psychiatric hospitals across California.    | —                        |
| Writing         | Essay Collection                            | Seventeen essays (May 2025–Mar 2026) tracing my journey and systems analysis.       | [Read the essays](/)     |

---

## Stratification Labs

Stratification Labs is the parent company for my clinical technology work. The core thesis is that modern psychiatry fails because it treats a wildly diverse patient population as though their problems all have the same origin. We need to stratify before we treat: social causes, chemical causes, and biological causes require fundamentally different interventions.

### Psykick

| Field           | Detail |
|----------------|--------|
| **What it does** | Reduces the administrative burden that eats psychiatrists alive. The average psychiatrist spends over ten hours a week fighting insurance companies and filling out forms, more than any other medical specialty. Psykick automates that work. |
| **Components**   | AI clinical scribe, prior authorization automation, claims defense system, electronic prescribing, time analytics dashboard, collaborative care platform, and contract intelligence. |
| **Why it matters** | APA President Theresa Miskimen Rivera identified administrative burden as a top priority for the psychiatric workforce in her 2025–2026 presidential agenda, specifically recommending AI scribing and EHR streamlining as solutions. Psykick is the implementation of that recommendation. |
| **Built in**     | Python |
| **Link**         | [View Psykick](https://psykicksv1.vercel.app/) |

### Psychify

| Field           | Detail |
|----------------|--------|
| **What it does** | Uses foundation models to stratify patient biotypes and predict treatment response at day zero, before the months of trial and error that currently define psychiatric prescribing. |
| **Why it matters** | Half of adults with depression do not improve on their first medication. The last major breakthrough in psychiatric medication was Clozapine in the 1980s. Psychify aims to end the guesswork by matching patients to mechanism-based treatments using computational models rather than sequential drug trials. |
| **Built in**     | Python |
| **Link**         | [View Psychify](https://psychify-dz8w.vercel.app/) |

---

## Project Jatoria — Mental Health Navigator

| Field           | Detail |
|----------------|--------|
| **What it does** | A web application that helps people understand and access mental healthcare services, starting with California and expanding to all 50 states. |
| **Data source**  | California Department of Health Care Services (DHCS) |

### Current components

- **Facility Finder:** Search and filter mental health facilities by county, services, and designations.
- **Healthcare Rights Guide:** Plain-language guide to patient rights and healthcare laws.
- **Price Transparency Tool:** Upload hospital price lists, compare costs, and understand medical billing.

### Planned additions

- **Guided intake flow:** Modeled on Garner Health's approach. Users describe their situation in plain language and get matched to the right facility type and insurance match, rather than navigating a raw directory.
- **Facility quality signal layer:** Composite scoring using licensing violations, accreditations (Joint Commission, CARF), modalities offered (MAT, DBT, trauma-informed care), staff ratios, and insurance acceptance.
- **Behavioral health data directory:** Modeled on Trilliant Health's Oria. Consolidate scattered public facility data into a single queryable dataset exposed through both structured search and a conversational AI interface.
- **Open dataset publication:** For researchers, journalists, and policy advocates, with integration into Project Jatoria.

| Field   | Detail |
|---------|--------|
| **Link** | [View Project Jatoria](https://jt-app.vercel.app/) |

---

## Research

Current and planned research directions that connect claims data, facility supply, and frontline observations.

### Behavioral Health Spending and Access in California (HPD)

| Field             | Detail |
|-------------------|--------|
| **Status**        | Data access requested from HCAI. |
| **Research question** | Does behavioral health spending in California reach the populations and geographies that need it, and what structural factors — facility supply, payer mix, parity enforcement — predict the gap? |
| **Method**        | Extend HCAI's existing Milbank methodology (currently commercial-only, statewide aggregates) to all payers at the county level using Healthcare Payments Data. Overlay DHCS facility data to measure spending-per-bed and spending-per-capita-with-BH-diagnosis ratios by county. |
| **Output**        | County-level behavioral health access-to-spending map for California. The first analysis of its kind linking claims data to facility supply for behavioral health in the state. |
| **Context**       | HCAI has published a behavioral health spending brief covering commercial claims (2018–2023) and a utilization dashboard covering health conditions by county and payer type. Neither links spending to access or breaks behavioral health down by county and payer simultaneously. This project fills that gap. |
| **Grant opportunity** | CHCF Affordability Research Funding Pool (up to $500K, spring 2026 cycle) specifically funds HPD-based research on consumer affordability challenges and systemwide cost drivers. Dissemination through peer-reviewed journal submission and integration into Project Jatoria. |

### Low-Value Psychiatric Care and Pharmaceutical Overuse

| Field             | Detail |
|-------------------|--------|
| **Research question** | How does the current reimbursement structure incentivize pharmaceutical intervention over lower-cost, potentially more effective alternatives in inpatient psychiatric settings? |
| **Approach**      | Combine floor-level observations from acute psychiatric hospital work with California HPD claims data to quantify spending on emergency psychiatric medications versus outpatient alternatives, and compare outcomes. Examine whether patients whose primary driver is social (homelessness, poverty, grief) receive the same pharmaceutical interventions as patients with genuine neurobiological conditions. |
| **Policy relevance** | Directly addresses Paragon Health Institute's MAHA research call on low-value and counterproductive medical care, including inappropriate use of pharmaceuticals to treat behavioral and mental health problems. Also relevant to the APA's precision psychiatry agenda. |

### Medicaid Behavioral Health Fraud Vulnerability in California

| Field             | Detail |
|-------------------|--------|
| **Research question** | Do California's Medi-Cal behavioral health services, specifically applied behavioral analysis for autism and substance use disorder treatment, exhibit the same structural fraud vulnerabilities identified in Minnesota? |
| **Approach**      | Analyze California spending patterns, provider entry rates, and billing anomalies using DHCS facility data and HPD claims data. Account for the methodological limitations KFF identified in CMS's February 2026 provider spending dataset (missing enrollment context, diagnosis codes, benefit structure, and payment rates). |
| **Context**       | Paragon Health Institute's February 2026 brief identified ABA and SUD services as two of four Medicaid categories most vulnerable to fraud nationally, driven by explosive spending growth, low barriers to provider entry, and fragmented oversight. California-specific analysis does not yet exist. |

### Autism Centers and Medicaid Funding

| Field             | Detail |
|-------------------|--------|
| **Status**        | Early stage. |
| **Research question** | How are autism service centers funded through Medicaid, and what does CMS data reveal about spending patterns, provider concentration, and service delivery across states? |

---

## Tools

### Psychiatric Hospital Review Scraper

| Field           | Detail |
|----------------|--------|
| **What it does** | Scrapes and analyzes patient reviews of psychiatric hospitals across California to test whether patterns observed at a single hospital hold up statewide. |
| **Purpose**       | I cannot work at every facility, so this is a way to gather data at scale and see whether the inefficiencies I document in my essays — intake failures, medication cycling, environmental design problems — are systemic or local. |

---

## Essay collection

Seventeen essays written between May 2025 and March 2026 documenting my journey from a personal crisis to a new mission in mental health. The collection covers floor observations, systems analysis, policy research, and the founding of Stratification Labs.

[Read the essays](/)

---

*All projects are active and in various stages of development. If you are a researcher, clinician, policy analyst, or engineer interested in collaborating on any of these, reach out.*

