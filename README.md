# ANT ???: Archaeological Data Management and Analysis
### Informatics for Archaeology and Zooarchaeology

**Graduate course, MA Program in Cultural Resource Management**
**University of Texas at Austin / Department of Anthropology**

|                    |                                                                            |
| ------------------ | -------------------------------------------------------------------------- |
| **Instructor**     | Professor Denné Reed                                                       |
| **Email / Office** | reedd@austin.utexas.edu · WCP 5.158                                        |
| **Office hours**   | [days/times], or by appointment                                            |
| **Meeting time**   | Weekly, 3 hours                                                            |
| **Location**       | TBD - TARL? / online?                                                      |
| **Course site**    | https:// · **Course repository:** https://github.com/reedd-austin/adma     |
| **Prerequisites**  | Graduate standing in the MA program. No programming experience is assumed. |

---

## 1. Course Description

This is a hands-on, lab-based course on how archaeological and zooarchaeological data are created, structured, stored, shared, and analyzed in archaeological practice. Students learn to work fluently in Windows, macOS, and Linux environments and at the Unix command line; to design relational databases, controlled vocabularies, and ontologies for archaeological data; and to use Python or R to extract data from their databases and produce analyses and report-ready products.

The course is organized around a **simulated Section 106 / Antiquities Code project**. Students work as a small CRM firm that has been contracted to survey, evaluate, and partially mitigate a site on a pipeline or county-road corridor. The assignments correspond to the common deliverables CRM firms produce: a data management plan, a project database, QA/QC documentation, a curation-ready collection inventory, a confidentiality plan, and report tables and figures.

## 2. Learning Outcomes

By the end of the course, students will be able to:

1. **Manage computing environments.** Navigate Windows, macOS, and Linux file systems; use the Unix shell (and PowerShell equivalents) to inspect, clean, transform, and automate work with data files.
2. **Practice reproducible data management (FAIR).** Use version control, documented workflows, and consistent file and naming conventions that survive staff turnover, client review, and curation.
3. **Design relational databases.** Translate archaeological recording practice into normalized, constraint-enforced schemas (SQLite/GeoPackage, PostgreSQL/PostGIS) and write SQL to query, validate, and summarize data.
4. **Handle spatial data correctly.** Select, transform, and troubleshoot coordinate reference systems, and move spatial data between open-source and Esri environments.
5. **Build controlled vocabularies and ontologies.** Develop SKOS thesauri and OWL ontologies from competency questions, and align local terminology to published standards.
6. **Publish and exchange data.** Export relational data as RDF, query it with SPARQL, and prepare a repository deposit that applies appropriate access restrictions.
7. **Analyze archaeological and faunal data programmatically.** Use Python or R to extract data from databases, compute standard quantitative measures, produce figures and tables, and report uncertainty honestly.
8. **Apply the legal and ethical context.** Connect data design decisions to Section 106, the Antiquities Code of Texas, curation requirements, site-location confidentiality, and descendant-community consultation.

## 3. Course Structure and Format

Each 3-hour session follows a consistent rhythm:

| Segment | Time | Activity |
|---|---|---|
| Discussion / short lecture | ~30 min | Concepts, readings, case examples |
| Live demonstration | ~30 min | Instructor works through the week's tools on screen |
| Hands-on lab | ~110 min | Supervised lab work on the project dataset |
| Wrap-up | ~10 min | Commit work, preview next week, assign prep |

**Three parts**

| Part | Weeks | Focus |
|---|---|---|
| I. Computing Environments and the Command Line | 1–3 | Operating systems, shell, scripting, command-line geospatial tools |
| II. Database and Knowledge Base Design (core) | 4–9 | Relational design, SQL, PostGIS, vocabularies, ontologies, linked data, curation |
| III. Data Analytics | 10–13 | Python/R, quantification, inference, spatial analysis, reproducible reporting |

## 4. The Running Project: The "[Project Name]" Corridor

All students work from the same mock project dataset, hosted in the course repository. The scenario is designed to trigger **both** compliance regimes, so that one dataset must support two sets of deliverables:

- **Section 106 of the National Historic Preservation Act (36 CFR 800):** a pipeline or road corridor requiring a U.S. Army Corps of Engineers permit or federal funding.
- **Antiquities Code of Texas (Texas Natural Resources Code, Chapter 191):** the corridor crosses state or local public land, requiring an Antiquities Permit from the THC.

**Scenario:** a linear corridor in the Edwards Plateau or Blackland Prairie region [instructor to select]. The dataset contains:

- Area of Potential Effects (APE) polygons and a project centerline
- Survey transects, shovel-test locations, and shovel-test results (Phase I)
- One multicomponent site with burned rock midden features and excavation units (Phase II/III)
- An artifact catalog (lithics, ceramics, historic items) and a **faunal catalog** (deer, bison, rabbit, turtle, freshwater mussel, unidentified fragments) with provenience, taxon, element, side, portion, fusion, burning, butchery and weathering notes, NISP counts, and weights
- Soil, geology, and hydrography layers from public Texas sources
- Deliberately messy legacy files (Excel with merged cells and dropped leading zeros, mixed delimiters, misspelled taxa and provenience, duplicate catalog numbers, mismatched coordinate systems)

**Using your own data:** Students may substitute sanitized data from their employment, with written permission from the employer or client. Do not bring restricted site-location data, human remains information, or any client-confidential material onto shared course infrastructure. See Section 9.

## 5. Technology and Materials

### Computing environment
- **Required:** a laptop running Windows 10/11, macOS, or Linux, with administrator rights. Windows students will install **WSL2** (Ubuntu) in Week 1.
- **Course server [if available]:** a shared PostgreSQL/PostGIS instance and an RStudio Server or JupyterHub, so that all database work in Weeks 6–13 has an identical configuration. Fallback: a course Docker image distributed through the repository.
- **Software (all free unless noted):** Git, VS Code, SQLite, DB Browser for SQLite, PostgreSQL + PostGIS, QGIS, GDAL/OGR, Protégé, Apache Jena Fuseki, R + RStudio and/or Python + Jupyter, Quarto.
- **ArcGIS Pro:** [university license, if available]. Used for demonstrations of interoperability (File Geodatabase, GeoPackage, Survey123/Field Maps); all assignments can be completed with open-source tools.

### Texts
There is no single required textbook. Most readings are free online. Please verify current editions and availability.

**Primary (required, free or low cost)**
- Shotts, W. *The Linux Command Line* (No Starch Press; free PDF from the author)
- Software Carpentry lessons: *The Unix Shell*, *Version Control with Git*, *Databases and SQL* (free online)
- Wickham, H., Çetinkaya-Rundel, M., & Grolemund, G. *R for Data Science* (2nd ed., free online), **or** McKinney, W. *Python for Data Analysis* (3rd ed., O'Reilly)
- Keet, C. M. *An Introduction to Ontology Engineering* (free online): selected chapters
- Noy, N., & McGuinness, D. "Ontology Development 101" (free online)

**Recommended references**
- Hernandez, M. *Database Design for Mere Mortals*
- Beaulieu, A. *Learning SQL* (O'Reilly)
- Obe, R., & Hsu, L. *PostGIS in Action* (Manning): selected chapters
- Allemang, D., Hendler, J., & Gandon, F. *Semantic Web for the Working Ontologist* (3rd ed.)
- Janssens, J. *Data Science at the Command Line* (2nd ed., free online)
- Carlson, D. L. *Quantitative Methods in Archaeology Using R* (Cambridge)
- Lovelace, R., Nowosad, J., & Muenchow, J. *Geocomputation with R* (free online)
- Gillings, M., Hacıgüzeller, P., & Lock, G. (eds.) *Archaeological Spatial Analysis: A Methodological Guide* (Routledge)
- Lyman, R. L. *Quantitative Paleozoology* (Cambridge)
- Reitz, E., & Wing, E. *Zooarchaeology* (2nd ed., Cambridge): background for students new to zooarchaeology
- King, T. F. *Cultural Resource Laws and Practice* (AltaMira/Rowman & Littlefield)
- Kansa, E., Kansa, S. W., & Watrall, E. (eds.) *Archaeology 2.0* (free, open access)
- Digital Antiquity (tDAR) and Archaeology Data Service *Guides to Good Practice* (free)

**Regulatory and Texas sources (free; check current versions)**
- 36 CFR 800 (Section 106); 36 CFR 79 (curation of federally owned and administered collections); Secretary of the Interior's Standards and Guidelines for Archeology and Historic Preservation
- Texas Natural Resources Code, Chapter 191 (Antiquities Code of Texas); Texas Administrative Code, Title 13, Part 2 (THC rules) **(VERIFY current chapters)**
- THC Archeology Division guidance: survey standards, permitting, reporting guidelines, curation
- Texas Archeological Sites Atlas and Texas Historic Sites Atlas (access is tiered) **(VERIFY current access procedures)**
- Texas Archeological Research Laboratory (TARL) collections and digital resources; Texas Beyond History
- Council of Texas Archeologists (CTA) guidelines; *Bulletin of the Texas Archeological Society*
- TNRIS / StratMap (statewide geospatial data), NRCS Web Soil Survey, USGS National Hydrography Dataset, Bureau of Economic Geology geologic atlas
- Texas Health and Safety Code, Chapter 711 (cemeteries and unmarked burials); NAGPRA (25 USC 3001 et seq.; regulations substantially revised in 2024) **(VERIFY)**

## 6. Assessment

| Component | Weight | Due |
|---|---|---|
| Weekly lab completion and participation | 20% | Weekly (committed to repository by the following Monday) |
| Assignment 1: Reproducible cleaning pipeline and Data Management Plan | 10% | End of Week 3 |
| Assignment 2: Relational project database with QA/QC and data dictionary | 20% | End of Week 6 |
| Assignment 3: Ontology, linked data, and curation/confidentiality plan | 20% | End of Week 9 |
| Final project: reproducible research compendium and presentation | 30% | Week 13 |

**Grading scale:** A (90–100), B (80–89), C (70–79), below 70 is not passing for graduate credit. [Adjust to department policy.]

**Weekly labs** are graded complete / partial / incomplete (full / half / no credit). The lowest lab score is dropped.

**Working in teams:** Weekly labs may be done in pairs (one driver, one navigator, rotating). All four assignments and the final project are completed individually unless the instructor approves a team structure. Every student must have a personal commit history showing their own work.

**Late work:** [e.g., 10% per day late, up to 3 days; one 48-hour extension permitted per semester without penalty.]

### Assignment overviews

**Assignment 1 (Week 3): Data Pipeline and Data Management Plan**
- A Git repository containing scripts (Bash and/or PowerShell) that take the raw legacy files and produce cleaned, validated, UTF-8 CSVs with a processing log.
- A README documenting the environment, how to run the pipeline, and every transformation applied.
- A one-page Data Management Plan covering: data types, file formats and naming (including permit number and trinomial conventions), roles, backup, QA/QC, version control, confidentiality, and curation destination.

**Assignment 2 (Week 6): Relational Database**
- Complete DDL for a normalized schema in PostgreSQL/PostGIS (and a GeoPackage export), with primary/foreign keys, check constraints, and lookup tables for controlled vocabularies.
- Entity-relationship diagram and data dictionary.
- Loaded project data with a record of the load process.
- A set of at least 10 QA/QC queries flagging impossible or suspicious records (e.g., orphan specimens, element/taxon conflicts, duplicate catalog numbers, geometries outside the APE, CRS mismatches).
- At least 10 analytic queries (NISP by taxon and context, density by unit, and others).

**Assignment 3 (Week 9): Ontology, Linked Data, and Curation/Confidentiality Plan**
- An OWL ontology and SKOS vocabulary developed from documented competency questions and aligned to at least three published vocabularies.
- An RDF export of a defined subset of the database, loaded in a triple store, with SPARQL queries answering each competency question.
- A 2–3 page rationale comparing relational and graph approaches for the same data.
- A curation and confidentiality plan: collection inventory in curation-ready form, a mock tDAR deposit with masked locations, and a role-based access design (restricted versus public views).

**Final Project (Week 13): Reproducible Research Compendium**
- A Git repository containing the database (or reproducible build scripts), ontology/RDF layer, analysis code that queries the database directly, and a Quarto-generated technical report section with tables, figures, and a Criterion D-style evaluation of what the data can and cannot support.
- A curation and data-sharing plan.
- A 12-minute presentation to the class (and invited guests where possible).
- Archived with a Zenodo (or equivalent) DOI.

## 7. Weekly Schedule

Readings are listed for preparation before class unless noted. Labs are the core of each session.

---

### PART I: COMPUTING ENVIRONMENTS AND THE COMMAND LINE

---

#### Week 1: Operating Systems, File Systems, and Professional Data Management

**Objectives:** Students can describe how the three major operating systems organize files, permissions, and processes; set up a working Linux shell; and establish a project structure and naming convention suitable for CRM practice.

**Topics**
- Course overview; the simulated project and its deliverables
- File systems on Windows, macOS, and Linux: paths, permissions, hidden files, processes, package managers (winget, Homebrew, apt)
- WSL2 and PowerShell on Windows; Terminal on macOS and Linux
- Project folder structure and naming standards for CRM work, including permit number, project number, and Texas trinomial in file names; what counts as the "record copy" for a client or the THC
- Plain text, character encodings (UTF-8), and line endings
- Why Excel corrupts data: auto-converted dates, lost leading zeros in catalog and project numbers, scientific notation, merged cells, and hidden sheets
- Introduction to Git and GitHub: commit, status, log, remote; why large binaries and GIS data require different handling (Git LFS, external storage)

**Readings:** Shotts, Ch. 1–4; Software Carpentry, *Git* (first lessons); Zeeberg et al. on gene-name corruption in Excel (a well-known example of the problem) or similar case study [instructor to select]

**Lab**
1. Install and test the environment (WSL2/terminal, Git, VS Code).
2. Create the course repository from the template; make a first commit.
3. Build the project directory structure and write a naming convention document.
4. Open the raw catalog in Excel and in a text editor; identify and list five corruption problems.

**Due:** Environment check-off; repository created and shared with the instructor.

---

#### Week 2: Unix Command Line Fundamentals

**Objectives:** Students can navigate and manipulate files from the shell and chain tools together with pipes to inspect and clean tabular data.

**Topics**
- Navigation, file manipulation, globbing, redirection, pipes, `man` and help systems
- Text-processing tools: `head`, `tail`, `less`, `wc`, `cut`, `sort`, `uniq`, `grep`, `sed`, `awk`, `find`, `tr`
- Regular expressions for pattern matching and replacement
- PowerShell equivalents (Get-ChildItem, Select-String, Import-Csv) for Windows-native work

**Readings:** Shotts, Ch. 5–7, 19–20; Software Carpentry, *The Unix Shell*

**Lab**
1. Profile the messy catalog from the command line: row counts, distinct taxa, distinct provenience values, empty fields.
2. Identify inconsistent spellings (e.g., "Odocoileus virginianus," "O. virginianus," "odocoileus virg."), whitespace, and mixed delimiters.
3. Write a command pipeline that standardizes provenience strings and flags duplicate catalog numbers.
4. Document each command in a lab notebook (Markdown) in the repository.

**Due:** Weekly lab.

---

#### Week 3: Scripting, Automation, and Command-Line Geospatial Tools

**Objectives:** Students can write shell scripts to automate repetitive data tasks and use GDAL/OGR to inspect and convert spatial data.

**Topics**
- Bash scripting: variables, loops, conditionals, functions, exit codes, error handling; PowerShell equivalents
- Remote work: `ssh`, `scp`/`rsync`, scheduled tasks (`cron`), environment variables
- Tabular tools: `csvkit`, `jq`, `sqlite3`
- GDAL/OGR: `ogrinfo`, `ogr2ogr` for converting among shapefiles, file geodatabases, GeoJSON, and GeoPackage; inspecting CRS and attribute schemas
- Public Texas data: TNRIS/StratMap, NRCS Web Soil Survey, USGS hydrography, and BEG geology
- Setting up Python (venv/conda) or R (renv) environments for Part III

**Readings:** Shotts, Ch. 24–27, 29–30; GDAL/OGR documentation (vector utilities); Janssens (selected chapters)

**Lab**
1. Write a script that validates a folder of field-crew spreadsheets and GPS exports (required columns present, no duplicate IDs, valid coordinates) and writes a log.
2. Use `ogr2ogr` to convert a mixed set of spatial files into a single GeoPackage and report each layer's CRS.
3. Download and clip one TNRIS/NRCS layer to the project area from the command line.
4. Create the Python or R environment file for the project.

**Due:** **Assignment 1** (pipeline and Data Management Plan).

---

### PART II: DATABASE AND KNOWLEDGE BASE DESIGN

---

#### Week 4: Data Modeling for the CRM Project Lifecycle

**Objectives:** Students can analyze an archaeological recording system and produce a normalized entity-relationship model that supports the project lifecycle and a target report schema.

**Topics**
- Archaeological data as hierarchical, relational, and uncertain: project → survey area → site → locus/unit → level/context → bag/lot → artifact/specimen
- How data evolves from Phase I (survey) to Phase II (evaluation) to Phase III (data recovery), and what must survive to curation
- Entities, attributes, relationships, cardinality, keys, and normalization (1NF–3NF); when to denormalize
- Modeling uncertainty: "cf." identifications, "unidentified medium mammal," ranges, and null semantics
- The case against Excel and Access as systems of record
- **Texas-specific modeling:**
  - The **Texas trinomial** as a structured key: state code (41), two-letter county code, and site number. Compare storing it as a single string, as a composite key, and as derived fields from components. Create a lookup table of all 254 counties.
  - The THC/TARL archeological site form and THC survey/reporting standards as the "target schema" the database must be able to populate **(VERIFY current form and standards)**
  - Permit-centered reporting under the Antiquities Code: modeling the relationships among permit, project, sponsor, site, collection, and report
  - Federal undertaking versus state permit identifiers on the same project

**Readings:** Hernandez, Ch. 1–8 (selected); sample THC site form and survey standards; a published zooarchaeological recording protocol [instructor to select]

**Lab**
1. In pairs, review the site form and two recording sheets (lithic, faunal) and list every entity and attribute.
2. Draw a conceptual and logical ER diagram in dbdiagram.io or draw.io.
3. Present diagrams to the class; critique one another's treatment of provenience, uncertainty, and the trinomial.
4. Revise and commit the final diagram.

**Due:** ER diagram and brief design memo.

---

#### Week 5: SQL Fundamentals with SQLite and GeoPackage

**Objectives:** Students can implement a schema in SQL and write queries that summarize archaeological data.

**Topics**
- DDL: `CREATE TABLE`, data types, primary and foreign keys, `CHECK`, `UNIQUE`, `NOT NULL`
- Lookup tables as controlled vocabularies (taxon, element, material class, burning/weathering stage)
- DML and queries: `INSERT`, `UPDATE`, `DELETE`, `SELECT`, `WHERE`, joins (inner, left), `GROUP BY`, aggregation, subqueries, views
- GeoPackage / SpatiaLite as a bridge between a database and GIS; open the same file in QGIS and ArcGIS Pro

**Readings:** Software Carpentry, *Databases and SQL*; Beaulieu, Ch. 1–10 (selected)

**Lab**
1. Implement the Week 4 schema in SQLite.
2. Load the cleaned Week 2–3 data, resolving foreign key failures and recording each fix.
3. Write queries for NISP by taxon and context; artifact counts by material class and unit; density per excavated volume; and a view that reproduces a report table.
4. Open the GeoPackage in QGIS (and ArcGIS Pro, if available) and map unit-level counts.

**Due:** Weekly lab (schema script and query file in repository).

---

#### Week 6: Multi-User Databases, PostgreSQL/PostGIS, and Field Data Capture

**Objectives:** Students can deploy a multi-user spatial database, manage coordinate reference systems, and build QA/QC checks into the database.

**Topics**
- PostgreSQL: roles and privileges, indexes, transactions, views, triggers, audit tables (who changed what, when)
- PostGIS: geometry types, spatial indexes, spatial joins, `ST_Transform`, `ST_Within`, `ST_Intersects`, buffers
- **Coordinate systems in Texas:** the State Plane zones (North, North Central, Central, South Central, South), UTM zones 13–15, NAD83 versus WGS84, and the TxDOT Texas Centric Mapping System; the US survey foot versus international foot problem in legacy datasets
- Field data capture: Esri Survey123 and Field Maps, QField, and CSV exchange; designing forms that map to the database; offline sync issues
- Building validation into the system: constraints, domain tables, QA/QC views

**Readings:** Obe & Hsu, selected chapters; PostgreSQL documentation (roles, triggers); a TxDOT or THC description of Texas coordinate systems [instructor to select]

**Lab**
1. Migrate the SQLite database to PostgreSQL/PostGIS.
2. Add geometry for excavation units, shovel tests, and the APE.
3. **CRS exercise:** the instructor has deliberately loaded several layers with the wrong or unlabeled CRS (including a survey-foot error). Students detect the problems with queries and fix them.
4. Write QA/QC queries (orphan records, impossible element/taxon pairs, geometries outside the APE, duplicate catalog numbers) and an audit trigger on the specimen table.

**Due:** **Assignment 2** (relational database).

---

#### Week 7: Controlled Vocabularies and Ontologies, Part 1

**Objectives:** Students can explain the differences among taxonomies, thesauri, and ontologies, and can build an ontology driven by competency questions.

**Topics**
- Why CRM data fails to integrate: firms, agencies, and repositories code the same things differently
- Taxonomy versus thesaurus versus ontology; open-world versus closed-world reasoning
- RDF, RDFS, OWL, and SKOS: classes, properties, individuals, labels, hierarchies, and reasoning
- Methodology: scope, competency questions, reuse, class and property definition (Noy & McGuinness)
- Writing competency questions that a regulator, curator, or analyst would really ask (for example: "Which sites in the APE have intact Archaic components?" "Which collections contain *Bison bison* remains with butchery marks?")

**Readings:** Noy & McGuinness; Keet, selected chapters; Allemang et al., Ch. 1–5 (selected)

**Lab**
1. Write 10–15 competency questions in teams, drawing on the project's stakeholders (THC reviewer, curator, project archaeologist, zooarchaeologist).
2. Build a first ontology in Protégé: skeletal elements, taxa, modifications, artifact classes, features, contexts, components, and temporal periods.
3. Create a SKOS concept scheme for burned rock midden feature types and Texas cultural periods (Paleoindian, Archaic, Late Prehistoric, Historic).
4. Run a reasoner and examine inferences.

**Due:** Competency question list and draft ontology.

---

#### Week 8: Standards, Reuse, and Linked Data

**Objectives:** Students can align local vocabularies to published standards and export relational data as RDF.

**Topics**
- Existing vocabularies and standards: FISH (Forum on Information Standards in Heritage) vocabularies, Getty AAT, Darwin Core, Uberon, CIDOC CRM and extensions, Dublin Core, SKOS
- How the THC Texas Archeological Sites Atlas, TARL site files, and Texas projects in tDAR each represent the same site **(VERIFY current systems)**
- Reconciling local Texas terminology (burned rock midden, regional point-type and phase names) with published vocabularies; the limits of crosswalks
- Linked data principles, persistent identifiers (URIs, DOIs, ARKs), FAIR and CARE principles
- Mapping relational data to RDF with R2RML or Python/rdflib

**Readings:** CIDOC CRM documentation (introductory sections); FISH vocabulary documentation; Carroll et al. on the CARE Principles for Indigenous Data Governance

**Lab**
1. Align the Week 7 ontology and vocabularies to at least three published sources, recording each mapping type (exact, close, broader, narrower).
2. Write a script that exports specimen, context, and site tables as RDF.
3. Validate the RDF and inspect it in Protégé.

**Due:** Weekly lab (mapping table and RDF export script).

---

#### Week 9: Querying, Publishing, Curation, and Ethics

**Objectives:** Students can query a knowledge base with SPARQL and prepare a deposit that complies with curation and confidentiality requirements.

**Topics**
- SPARQL: basic graph patterns, filters, `OPTIONAL`, aggregation, property paths, federated queries
- Triple stores (Apache Jena Fuseki, GraphDB Free); brief comparison with graph databases (Neo4j) and document stores (JSON/MongoDB)
- **Curation:** federal (36 CFR 79) and Texas curation requirements, certified curatorial facilities, and TARL's role as the principal state repository; what a curation-ready collection inventory, catalog export, and documentation set looks like **(VERIFY current THC curation rules and TARL submission requirements)**
- **Confidentiality:** why site location data are restricted (NHPA §304, ARPA §9, and Texas provisions); tiered access in the Atlas; Texas Public Information Act considerations **(VERIFY statutory citations)**; designing restricted versus public views in PostgreSQL
- **Human remains and consultation:** unmarked burials under Texas Health & Safety Code Chapter 711 and NAGPRA; tribes with historical ties to Texas (including Oklahoma-based Caddo, Comanche, Kiowa, and Tonkawa nations, and the federally recognized tribes resident in Texas); tribal data sovereignty; modeling a consultation log
- Repositories: tDAR, Open Context, TARL, state systems; metadata, licensing, and embargoes

**Readings:** Selected tDAR and ADS *Guides to Good Practice*; THC curation and permit guidance; 36 CFR 79 (overview); Kansa et al., selected chapter(s) from *Archaeology 2.0*

**Lab**
1. Load the RDF into Fuseki; write SPARQL queries answering every competency question.
2. Create public and restricted database views and roles; demonstrate that a "public" user cannot retrieve site coordinates.
3. Generate a curation-ready collection inventory from the database.
4. Assemble a mock tDAR deposit (metadata, file formats, masked locations).

**Due:** **Assignment 3** (ontology, linked data, and curation/confidentiality plan).

---

### PART III: DATA ANALYTICS

*Students choose Python or R. Demonstrations are given in both; R is the default for instructor examples.*

---

#### Week 10: Connecting to Databases and Wrangling Data

**Objectives:** Students can pull data directly from PostGIS and SPARQL endpoints into an analysis environment and reshape it into tidy form.

**Topics**
- Database connections: DBI / RPostgres / dbplyr (R) or SQLAlchemy / psycopg2 / pandas (Python)
- Tidy data principles; joins, reshaping, grouping, missing data
- Querying a SPARQL endpoint into a data frame
- Reading public spatial layers (SHPO, TNRIS) with `sf` or `geopandas`
- Notebooks and literate programming: Quarto and Jupyter
- Credentials and secrets: never hard-code passwords; environment variables and `.Renviron` / `.env` files

**Readings:** Wickham et al., *R for Data Science*, selected chapters (import, tidy, transform) or McKinney, Ch. 5–8

**Lab**
1. Connect to the project database and build an analysis-ready table (specimens joined to contexts, units, volumes, and components).
2. Save the SQL query in the repository and call it from the notebook.
3. Pull one SPARQL result set into a data frame and reconcile it with the SQL result.

**Due:** Weekly lab.

---

#### Week 11: Exploratory Analysis and Zooarchaeological Quantification

**Objectives:** Students can compute standard archaeological and zooarchaeological measures from a database and understand their limitations.

**Topics**
- Descriptive statistics and visualization (ggplot2 or matplotlib/seaborn)
- Artifact and faunal quantification: counts, NISP, MNI, weights, density per volume or per unit
- Taxonomic abundance, diversity and evenness indices, rarefaction, body-part representation, age and sex profiles
- Statistical pitfalls: aggregation, interdependence of specimens, sample size, and recovery bias (screen size, field methods)
- Linking analysis to National Register Criterion D: what the data can and cannot support

**Readings:** Lyman, selected chapters on quantification; Carlson, selected chapters

**Lab**
1. Produce the standard tables and figures for a Phase II technical report directly from the database: counts by component, faunal abundance, body-part representation.
2. Compute diversity indices and a rarefaction curve for each component.
3. Write a short interpretive paragraph that states what the figures do and do not demonstrate.

**Due:** Weekly lab.

---

#### Week 12: Inference, Sampling, and Modeling

**Objectives:** Students can quantify uncertainty and compare assemblages using resampling and multivariate methods.

**Topics**
- Evaluating survey and shovel-test coverage; site density estimates by landform
- Bootstrapping and confidence intervals for small, non-random samples
- Multivariate methods: correspondence analysis, PCA, clustering
- Mortality profile analysis [time permitting]
- Predictive site-location modeling: methods, limits, and how agencies (including TxDOT) and the THC have used and evaluated probability models
- Reporting uncertainty in terms regulators and clients can use

**Readings:** Carlson, selected chapters; a published Texas predictive-model case study [instructor to select]

**Lab**
1. Compare two components or two sites with a multivariate technique; report results with bootstrap confidence intervals.
2. Compute shovel-test positive rates by landform using the Week 3 soil and geology layers.
3. Build a simple site-probability model and discuss its failure modes.

**Due:** Weekly lab; final project proposal (one page).

---

#### Week 13: Spatial Analysis, Reproducible Reporting, and Presentations

**Objectives:** Students can produce a reproducible, citable research compendium and communicate results.

**Topics**
- Spatial analysis with `sf` or `geopandas`: mapping finds, density surfaces, buffers and distance analyses relevant to effects assessment
- Quarto-to-Word reporting workflows suitable for CRM technical reports
- Research compendia: README, environment files, licensing, and archiving with a DOI (Zenodo)
- Final presentations

**Readings:** Marwick, B. et al. on reproducible research compendia in archaeology (or similar) [instructor to select]

**Lab / Session**
1. First hour: mapping lab and final repository checks.
2. Remaining time: student presentations (12 minutes plus questions). Invited guest reviewers if possible.

**Due:** **Final project.**

---

## 8. Suggested Guest Sessions

| Week | Guest | Purpose |
|---|---|---|
| 4 or 6 | Texas CRM firm data manager | Reality-check database designs against firm practice |
| 6 or 9 | THC Archeology Division / Atlas staff | Site-file systems, review workflow, access tiers |
| 9 | TARL curator | Curation requirements; what makes a collection easy or hard to accession |
| 9 or 12 | TxDOT Environmental Affairs archeologist | How a large agency manages data across many projects |
| 8 | tDAR / Open Context representative (virtual) | Repository deposits and metadata |

## 9. Data Ethics, Confidentiality, and Client Data Policy

- **Site location data are sensitive.** Real, unmasked site coordinates, particularly for burials or looting-prone sites, may not be placed on shared course infrastructure, public GitHub repositories, or any cloud service. Course repositories should be **private** unless the instructor states otherwise.
- **Use of employer or client data** requires written authorization and sanitization (masked coordinates, generalized provenience, removed client names). The instructor can review sanitization plans.
- **Human remains and sacred objects.** The mock dataset contains no real human remains data. Discussion of real cases follows descendant-community guidance and NAGPRA principles.
- **Consultation.** Students are expected to treat descendant communities as rights holders in data decisions, not merely as audiences.
- **Professional conduct.** Work follows the ethics codes of the Society for American Archaeology and the Register of Professional Archaeologists.

## 10. Course Policies

**Attendance and participation.** The course is lab-driven, and missing a session sets you back quickly. Notify the instructor in advance of absences. [Insert attendance policy.]

**Use of AI tools.** [Instructor to define. Suggested language: Students may use AI coding assistants for debugging and learning, but must be able to explain every line they submit and must note substantive AI assistance in their lab notebook. AI tools may not be given any sensitive or client data. Exams of understanding (brief oral check-ins) may be used.]

**Academic integrity.** Collaboration on labs is encouraged; assignments and the final project are individual work. Copying code or data without attribution is plagiarism. All code taken from documentation, forums, or other sources must be cited in comments. [Insert university honor code.]

**Accessibility and accommodations.** [Insert disability services statement.] Command-line and coding work can be hard on screen readers and small screens; please contact the instructor early so that accommodations can be arranged.

**Title IX, basic needs, and other university statements.** [Insert required university statements.]

**Changes to the syllabus.** The instructor may adjust the schedule in response to class progress, guest availability, or regulatory changes. Changes will be announced in class and posted on the course site.


## 11. At-a-Glance Calendar

| Wk | Date | Topic | Key tools | Due |
|---|---|---|---|---|
| 1 | [ ] | OS, file systems, data management | WSL2, Git, VS Code | Environment check |
| 2 | [ ] | Unix command line | grep, sed, awk, regex | Lab |
| 3 | [ ] | Scripting, GDAL/OGR | Bash/PowerShell, ogr2ogr | **Assignment 1** |
| 4 | [ ] | Data modeling | dbdiagram.io, ER diagrams | ER diagram |
| 5 | [ ] | SQL, GeoPackage | SQLite, QGIS | Lab |
| 6 | [ ] | PostgreSQL/PostGIS, CRS, QA/QC | PostGIS, Survey123/QField | **Assignment 2** |
| 7 | [ ] | Vocabularies, ontologies I | Protégé, SKOS | Draft ontology |
| 8 | [ ] | Standards and linked data | rdflib, R2RML | Mapping table |
| 9 | [ ] | SPARQL, curation, ethics | Fuseki, PostgreSQL roles | **Assignment 3** |
| 10 | [ ] | Database connections, wrangling | DBI/dbplyr or SQLAlchemy, Quarto | Lab |
| 11 | [ ] | Quantification and EDA | ggplot2/matplotlib | Lab |
| 12 | [ ] | Inference, multivariate, modeling | boot, vegan/FactoMineR or scikit-learn | Lab; project proposal |
| 13 | [ ] | Spatial analysis, reporting, presentations | sf/geopandas, Quarto, Zenodo | **Final project** |
