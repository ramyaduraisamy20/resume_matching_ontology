# Resume Matching Ontology

Ontology-based resume and job-description matching project that combines **Semantic Web technologies (OWL/RDF + SPARQL)** with **NLP (spaCy)** to retrieve structured, explainable candidate-role insights.

---

## Project Overview

This project models recruitment knowledge as a graph and enables query-driven analysis of:

- candidate skills and qualifications
- job role requirements
- education and experience alignment
- semantic links between applicants and job descriptions

Instead of relying only on keyword matching, the system uses ontology relationships to return more meaningful and transparent results.

---

## Key Features

- **Ontology modeling (`mp1.owl`)** for resume-job domain knowledge
- **NLP query preprocessing** using spaCy (`en_core_web_sm`)
- **Dynamic SPARQL query generation** from parsed user intent
- **Structured semantic retrieval** with `SPARQLWrapper2`
- **Explainable matching logic** based on class-property relationships

---

## Knowledge Model (Ontology)

The ontology includes major classes such as:

- `Person`, `Applicant`
- `Job_description`
- `Skills`
- `Education`
- `Work_experience`
- `Internships`
- `Awards`
- `Certificates`
- `Location`

### Core Object Properties

- `has_skills`
- `graduated_as`
- `has_experienced_as`
- `has_internship_experience`
- `require_skills`
- `require_education`
- `require_internship`
- `require_workexperience`

### Example Datatype Properties

- `name`
- `email`
- `age`
- `gender`
- `salary`
- `years_of_experience`
- `internship_time_limit`

---

## Tech Stack

- **Python**
- **Jupyter Notebook**
- **spaCy** (`en_core_web_sm`)
- **SPARQLWrapper2**
- **OWL / RDF**
- **SPARQL**

---

## Repository Structure

- `Resume.ipynb` — NLP preprocessing + dynamic SPARQL query workflow
- `mp1.owl` — ontology schema and individuals for the resume matching domain

---

## Workflow

1. User enters a natural-language-style query.
2. spaCy preprocesses text (lemmatization, POS tagging, entity extraction).
3. Extracted terms are mapped to ontology concepts and relations.
4. SPARQL query is constructed programmatically.
5. Query is executed and results are returned as semantic records.

---

## Example Query Intents

- "All available Job_description"
- "Person and their Skills"
- "Person with Education"
- "What are the require_skills for each Job_description"

---

## Outcomes

- Built a reusable semantic framework for resume-job analysis
- Enabled ontology-driven retrieval beyond basic keyword search
- Improved explainability and traceability of matching results
- Demonstrated practical integration of NLP + Semantic Web in recruitment intelligence

---

## Future Improvements

- Add scoring/ranking layer for candidate-role fit
- Expand ontology with certifications, proficiency levels, and domain hierarchies
- Build a web interface for interactive query input and result visualization
- Add validation metrics comparing semantic matching vs keyword baseline

---

