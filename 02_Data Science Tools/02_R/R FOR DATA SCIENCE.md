# 📘R FOR DATA SCIENCE (Hadley Wickham et al., 2nd Ed.)

## 📝 Abstract

> This book is the **functional manifesto of the Tidyverse**. It establishes a coherent philosophy for the data science cycle: Import, Tidy, Transform, Visualize, and Communicate. For an engineer, it provides a highly fluid syntax (the pipe `|>`) and a "grammar of graphics" that makes exploratory data analysis (EDA) faster and more expressive than standard procedural code.

---
## 🏗️ I. STRUCTURAL ANALYSIS
- **👤 Authors:** Hadley Wickham, Mine Çetinkaya-Rundel, and Garrett Grolemund.
- **🌐 Global Topology:** **Cyclical & Iterative** 🔄 (Structured around the DS lifecycle).
- **🎯 Target Audience:** Engineers and scientists who need a fluent, domain-specific language for data manipulation and communication.
- **⚙️ Global Objective:** Mastery of the Tidyverse ecosystem to turn raw data into reproducible insights and professional reports.

---
## 🗺️ II. KNOWLEDGE MAPPING (Full Syllabus & Objectives)

|ID|📖 Chapter / Section|💡 Learning Objective (Engineering Focus)|
|---|---|---|
|**I**|**Whole Game**|**Rapid end-to-end prototyping.**|
|1|Data Visualization|Master `ggplot2` to visualize distributions and relationships.|
|2|Workflow: Basics|Internalize R coding basics, function calls, and naming conventions.|
|3|Data Transformation|Master `dplyr` verbs: `filter`, `arrange`, `mutate`, and the Pipe.|
|4|Workflow: Code Style|Implement professional Tidyverse styling for readability.|
|5|Data Tidying|Use `tidyr` to pivot data between long and wide formats.|
|6|Workflow: Scripts & Projects|Manage RStudio Projects and absolute vs. relative paths.|
|7|Data Import|Master `readr` for flat files and multi-file ingestion.|
|8|Workflow: Getting Help|Create reproducible examples (reprex) for system troubleshooting.|
|**II**|**Visualize**|**The Grammar of Graphics.**|
|9|Layers|Deep dive into aesthetic mappings, geoms, facets, and stats.|
|10|Exploratory Data Analysis|Use variation and covariation to detect unusual values/patterns.|
|11|Communication|Professionalize plots with labels, annotations, scales, and themes.|
|**III**|**Transform**|**Data Engineering with R.**|
|12|Logical Vectors|Master Boolean algebra and conditional transformations (`case_when`).|
|13|Numbers|Perform numeric transformations, rolling aggregates, and summaries.|
|14|Strings|Use `stringr` for extraction and handling non-English encodings.|
|15|Regular Expressions|Master Regex pattern matching, capturing, and control flags.|
|16|Factors|Manipulate categorical data and modify factor levels/order.|
|17|Dates and Times|Use `lubridate` for time spans, zones, and rounding.|
|18|Missing Values|Handle explicit vs. implicit missingness and carrying values forward.|
|19|Joins|Master Relational Algebra: Mutating, Filtering, and Non-equi joins.|
|**IV**|**Import**|**Advanced Data Ingestion.**|
|20|Spreadsheets|Read and write Excel and Google Sheets with formatting.|
|21|Databases|Connect to SQL databases and use `dbplyr` for SQL translation.|
|22|Arrow|Handle large-than-memory data using Parquet and Arrow.|
|23|Hierarchical Data|Rectangle JSON and deeply nested lists into tibbles.|
|24|Web Scraping|Master `rvest` for HTML extraction and scraping ethics.|
|**V**|**Program**|**Functional Programming in R.**|
|25|Functions|Write robust functions using Tidy Evaluation (Indirection).|
|26|Iteration|Master `purrr::map()` and `across()` for repetitive tasks.|
|27|A Field Guide to Base R|Master vector/DF subsetting and the "Apply" family.|
|**VI**|**Communicate**|**Reproducible Reporting.**|
|28|Quarto|Integrate prose, code, and results into a single YAML-controlled doc.|
|29|Quarto Formats|Export to HTML, PDF, Slides, Shiny, and Websites.|