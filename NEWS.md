# Rnssp-rmd-templates
<hr>

## State Emergency Department template (`state_ed_report`)

<details>

<summary>11/16/2021</summary>
The State Emergency Department template has been updated. This version has:

* Modified algorithm for trajectory analysis to improve state and county-level trend classifications.

* Improved figure sizing to accommodate the selection of many categories.

* Improved time series visualizations, color palettes.

* Added interactive sparklines to DT table, Improve table formatting.

</details>


<details open>

<summary>6/8/2021</summary>
State Emergency Department template available.

</details>

<hr>

## Text Analysis Interactive Dashboard template (`text_mining`)

<details>

<summary>10/19/2021</summary>
The Text Mining template has been updated. 

This version contains a custom Query field that allows users to enter their own ESSENCE query.

</details>


<details>

<summary>9/29/2021</summary>
The Text Mining template has been updated. This version:

* Prematurely exits the knit when bad User Credentials are entered.

* Prematurely exits the knit when an empty dataset is returned by the API.

</details>

<details>

<summary>8/9/2021</summary>
The Text Mining template has been updated. This version:

* Asks for document title in parameter GUI

* Includes age groups 2 - 5

* Allows user to limit to a site or group of sites

* Allows users to subset down to particular age groups if they wish. By default, the data pull should pull CCQV data which doesn't contain age. If a user selects full details, then the age group filtering will apply. All possible age group options have been added. 

* Fixes a typo for a parameter name - replaced "ccdd_category_string" with "definition_string"

*Changes the default CCDD Category to COVID-DD
 

</details>

<details>

<summary>6/19/2021</summary>
The Text Mining template has been updated. This version contains the following updates:

* Users now have a choice to select a syndrome definition from a list of all CCDD categories, subsyndromes, and syndromes that are currently in the system. Users no longer need to manually paste in the query to populate on the Background tab. The input option allows for users to type and search for a definition type and name when knitting with parameters. As done in the combined category fields in ESSENCE, CCDD categories are proceeded by CCDD Category, subsyndromes by Subsyndrome, and syndrome by Syndrome.

* Chief complaint correlation network graph (based on Pearson correlation). Terms are filtered with a correlation greater than 0.15. Opacity of the edges/lines represents the magnitude of correlation. Note that pairs that occur next to each other in the chief complaint are removed in an attempt to avoid identifying term pairs that one would expect to see and that show up in the top 200 bigrams. Also added is a search table below the graph so that users can search for correlations for a term of interest. 

* n-gram trend analysis for chief complaint and discharge diagnosis unigrams and bigrams. The sections of code that generate these have been modified to prevent errors when there are no significant terms identified. 

</details>

<details open>
<summary>5/21/2021</summary>
Text Mining template available.
</details>

<hr>

## Essence Chief Complaint and Discharge Diagnosis Categories template (`essence_ccdd`)

<details>

<summary>9/13/2021</summary>
The Essence Chief Complaint and Discharge Diagnosis Categories template has been updated. This version:

* Contains some minor update to the GUI.

* Allows users to generate the report for a specific site.

</details>

<details open>

<summary>7/6/2021</summary>
The Essence Chief Complaint and Discharge Diagnosis Categories template is available.

This template generates a trend report of CCDD Categories between the MMWR weeks containing the dates you choose. Users are able to select as many of the CCDD Categories as they would like to generate, and are able to control for data quality using the Average Weekly DDI\% and CoV(HasBeenE) filters.

</details>


<hr>

## Emergency Department ICD-10 Category Volumes template (`ed_icd10_volume`)

<details>

<summary>11/10/2021</summary>
The Emergency Department ICD-10 Category Volumes template has been updated. This version:

* Has additional patient demographic stratifications
* Provides facility level selection variables

</details>

<details>

<summary>9/28/2021</summary>
The Emergency Department ICD-10 Category Volumes template has been updated. This version:

* Contains an Update of the medical grouping system to be chiefcomplaintsubsyndromes when a subsyndrome is selected

* Renders properly and properly prints DDI and CoV cutpoints in the output.

</details>


<details open>

<summary>9/13/2021</summary>
The Emergency Department ICD-10 Category Volumes template is available.

This template explores the top N categories by volume for the new ICD Chapter, Section, Diagnosis, and CCSR queries. It generates heat maps of the top N ICD-10-CM codes by ICD-10-CM chapter, ICD-10-CM section, ICD-10-CM diagnosis code, and the corresponding clinical classifications software refined (CCSR) category. Users are able to select the geographic region of interest, time frame, data quality filters, and ESSENCE age group category. 

</details>

<hr>

## Syndrome Definition Evaluation template (`syndrome_eval`)

<details>

<summary>1/14/2022</summary>
The Syndrome Definition Evaluation template has been updated.

This update allows the user to input up to three CCDD Free Text Queries.

</details>

<details>

<summary>1/6/2022</summary>
The Syndrome Definition Evaluation template has been updated.

This update adds a functionality to perform the data pull by chunks of one day.

</details>

<details>

<summary>11/3/2021</summary>
The Syndrome Definition Evaluation template has been updated.

This critical update fixes an issue related to API URLs being ill-constructed when syndromes or subsyndromes are selected.

</details>

<details>

<summary>11/1/2021</summary>
The Syndrome Definition Evaluation template has been updated for performance and efficiency. It contains:

* An update to the `detect_elements()` helper function solving therefore a memory limit issue preventing a successful render of the template when large datasets are pulled.

* Some minor improvements that remove large datasets from the memory stack when they are not used.

</details>


<details open>

<summary>9/13/2021</summary>
The Syndrome Definition Evaluation template is available.

This template allows ESSENCE users to evaluate the data details (line level) results of one, two, or three syndrome definitions at a time.

</details>

<hr>

## Word Alerts Report template (`word_alerts`)

<details>

<summary>11/15/2021</summary>
The Word Alerts Report template has been updated. This version:

* Updated the API for site-level full data details to use the Syndrome Subsyndrome CCDD Combined Category field to simplify the code.

* Added a new parameter, has_been_E, so that data can be limited to ED data if specified. This only applies to ESSENCE API pulls as CCQV backup table does not have a has_been_E field.

* Removed duplicate cat() statements when no alerts are found.

* Default date range is now the most recent 90 days. Default start and end dates are calculated using base R.

</details>

<details open>

<summary>11/9/2021</summary>
The Word Alerts Report template is available.

The Word Alerts Report template summarizes daily chief complaint and discharge diagnosis term alerts for a selected syndrome definition. 

The purpose of the word alert algorithm is to seek anomalous chief complaint free text terms and discharge diagnosis codes relative to a 28-day sliding baseline. 

The current implementation of word alerts in NSSP-ESSENCE is limited to data from the past 7 days. This template provides users the capability of running the word alert algorithm on any selected date range spanning up to 90 days.

</details>
