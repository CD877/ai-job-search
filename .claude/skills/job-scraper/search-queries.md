# Search Queries for Job Scraper

UK job market. Candidate: applied AI / agentic systems + 10 yrs CRM/martech delivery (Adobe Campaign, SFMC, Data Cloud).

## Search Sites

Primary (UK job market):
- **linkedin.com/jobs** - LinkedIn job listings (filter: London / United Kingdom)
- **uk.indeed.com** - Indeed UK
- **reed.co.uk** - Reed
- **totaljobs.com** - Totaljobs
- **cwjobs.co.uk** - CWJobs (tech roles)
- **consultancy.uk/jobs** - consulting roles (Big 4, Capgemini, Accenture, etc.)
- **otta.com / welcometothejungle.com** - startup / scale-up roles

Secondary (company career pages via search):
- Consultancies: Capgemini Invent, Accenture, Deloitte, PwC, EY, KPMG, IBM Consulting, BCG X, McKinsey QuantumBlack, Publicis Sapient, Slalom, Thoughtworks
- AI vendors / platforms: Anthropic, OpenAI, Google Cloud, Microsoft, Cohere, Mistral, Databricks, Snowflake, Salesforce (Agentforce), Adobe

## Query Categories

Combine with "London", "United Kingdom" or "remote UK" where the site supports it.

### Priority 1: Agentic / Applied AI Engineering

Any role building agentic systems, AI agents, LLM pipelines, evals.

```
site:linkedin.com/jobs "agentic" engineer London
site:linkedin.com/jobs "AI agents" engineer "United Kingdom"
site:linkedin.com/jobs "Applied AI Engineer" London OR remote
site:uk.indeed.com "agentic AI" engineer London
site:cwjobs.co.uk "AI engineer" agents LLM
```

### Priority 2: AI Consulting (Manager level)

Data & AI / GenAI / agentic consulting at Manager / Senior Consultant grade.

```
site:linkedin.com/jobs "AI Manager" consulting London agentic OR GenAI
site:consultancy.uk/jobs "AI" Manager agentic OR "generative AI"
"Capgemini Invent" OR Accenture OR Deloitte "agentic AI" Manager London job
site:linkedin.com/jobs "GenAI consultant" OR "AI consultant" London
```

### Priority 3: AI Solutions Architect / Forward Deployed Engineer

Client-facing technical roles at AI vendors and platforms.

```
site:linkedin.com/jobs "Forward Deployed Engineer" London
site:linkedin.com/jobs "AI Solutions Architect" OR "Solutions Engineer" LLM London
"Forward Deployed" OR "Solutions Architect" "applied AI" London careers
```

### Priority 4: AI in Martech / CRM

AI for CRM, personalisation, customer engagement, marketing decisioning.

```
site:linkedin.com/jobs "Agentforce" OR "Salesforce AI" London
site:linkedin.com/jobs "Adobe Experience Platform" AI OR agents London
site:linkedin.com/jobs "AI" CRM personalisation "marketing technology" London
site:uk.indeed.com "AI" martech OR "customer engagement" agents London
```

## Location Filter

Acceptable:
- London (hybrid, up to ~3 days/week in office)
- Fully remote, UK-based

Borderline (flag, don't drop):
- Hybrid outside London with low office days (e.g. Manchester/Glasgow base with London option)
- Roles requiring frequent client-site travel

Too far:
- Non-UK roles, or UK roles requiring 4-5 days/week outside London

## Date Filter

Only include jobs posted within the last 14 days, or with an application deadline that has not yet passed. If a posting date cannot be determined, include it but flag as "date unknown".

## Adapting Queries

If the user specifies a focus area, select queries from the matching category and also generate 2-3 custom queries for that focus. For example:
- "/scrape consulting" -> Priority 2 queries + custom consulting queries
- "/scrape fde" -> Priority 3 queries + custom forward-deployed queries
