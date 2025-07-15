---
title: E-Utilities Quick Start Guide
---

#E-Utilities Quick Start Guide

E-Utilies Options:

*  [ESearch](#esearch) - Searches one database
*  [ESummary](#essumary) - Downloads summaries of database records
*  [Efetch](#efetch)  - Returns full data records
*  [Elink](#elink) - Returns data linked within the same database or between two databases
*  [EGQuery](#egquery) - Returns the number of records in each database for a search term
*  [EInfo](#einfo) - Returns statistics for a single database or a list of all NCBI databases
*  [ESpell](#espell) - Returns spelling suggestions for terms within a single text query  
*  [ECitMatch](#ecitmatch) - * Returns PubMed IDs (PMIDs) for a set of citation strings 
*  [EPost](#epost) - Saves your search history for use in another E-Utility

## Base URL
All E-Utility queries begin with the following URL: 
https://eutils.ncbi.nlm.nih.gov/entrez/eutils/{  }.fcgi? 

## ESearch

To use Esearch:
1.	Start with the base URL: https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esearch.fcgi? 
2.	Add required parameters to the base URL
* If more than one parameter, join with an ampersand (&) 
* Do not include spaces

| --- | --- | --- |
| ESearch Required Parameters  | Description | Example |
| db | Database you want to search | db=pubmed |
| term  | Word or phrase  you want to search for in the database | term = asthma |

3. Paste the URL with parameters into any internet browser and press **Enter** key

**Result**

Returns a list of UIDs displayed in the internet browser. By default, the maximum number of results is limited to 20. 
* To change the number of results or add in other optional parameters, see [ESearch](reference_guide/esearch.md) for more information.

**Example**

[https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esearch.fcgi?db=pubmed&term=asthma](https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esearch.fcgi?db=pubmed&term=asthma)

---

## ESummary

To use ESummary:
1.	Start with the base URL: https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esummary.fcgi? 
2.	Add required parameters to the base URL
* If more than one parameter, join with an ampersand (&) 
* Do not include spaces

| --- | --- | --- |
| ESummary Required Parameters  | Description | Example |
| db | Database you want to search | db=pubmed |
| id  | One UID or a set of UIDs separated with commas that you want a document summary  | id=40654110|

3. Paste the URL with parameters into any internet browser and press **Enter** key

**Result**

Returns document summaries (DocSums) that provide brief overviews of the records associated with the provided UIDs.


**Example**

[https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esummary.fcgi?db=pubmed&id=40654110](https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esummary.fcgi?db=pubmed&id=40654110)


---

## EFetch

To use EFetch:
1.	Start with the base URL: https://eutils.ncbi.nlm.nih.gov/entrez/eutils/efetch.fcgi? 
2.	Add required parameters to the base URL
* If more than one parameter, join with an ampersand (&) 
* Do not include spaces

| --- | --- | --- |
| EFetch Required Parameters  | Description | Example |
| db | Database you want to search | db=pubmed |
| id  | One UID or a set of UIDs separated with commas that you want a document summary. <br> There is no set maximum for the number of UIDs that can be passed to EFetch, but if more than about 200 UIDs are provided, the request should be made using the HTTP POST method **LINK TO POST METHOD**  | id=40654110|

3. Paste the URL with parameters into any internet browser and press **Enter** key

**Result**

Returns formatted data records for the UIDs, in a format specified in the request, e.g., XML or FASTA.


**Example**

[https://eutils.ncbi.nlm.nih.gov/entrez/eutils/efetch.fcgi?db=pubmed&id=19393038,30242208,29453458 ](https://eutils.ncbi.nlm.nih.gov/entrez/eutils/efetch.fcgi?db=pubmed&id=19393038,30242208,29453458)

---


## ELink

To use EFetch:
1.	Start with the base URL: https://eutils.ncbi.nlm.nih.gov/entrez/eutils/efetch.fcgi? 
2.	Add required parameters to the base URL
* If more than one parameter, join with an ampersand (&) 
* Do not include spaces

| --- | --- | --- |
| EFetch Required Parameters  | Description | Example |
| db | Database you want to search | db=pubmed |
| id  | One UID or a set of UIDs separated with commas that you want a document summary. <br> There is no set maximum for the number of UIDs that can be passed to EFetch, but if more than about 200 UIDs are provided, the request should be made using the HTTP POST method **LINK TO POST METHOD**  | id=40654110|

3. Paste the URL with parameters into any internet browser and press **Enter** key

**Result**

Returns a list of UIDs displayed in the internet browser. By default, the maximum number of results is limited to 20. 
* To change the number of results or add in other optional parameters, see [ESearch](reference_guide/esearch.md) for more information.


**Example**

[https://eutils.ncbi.nlm.nih.gov/entrez/eutils/efetch.fcgi?db=pubmed&id=19393038,30242208,29453458 ](https://eutils.ncbi.nlm.nih.gov/entrez/eutils/efetch.fcgi?db=pubmed&id=19393038,30242208,29453458)


---


## ELink

To use EFetch:
1.	Start with the base URL: https://eutils.ncbi.nlm.nih.gov/entrez/eutils/efetch.fcgi? 
2.	Add required parameters to the base URL
* If more than one parameter, join with an ampersand (&) 
* Do not include spaces

| --- | --- | --- |
| EGQuery Required Parameters  | Description | Example |
| term  | Word or phrase you want to search for | term = asthma |


3. Paste the URL with parameters into any internet browser and press **Enter** key

**Result**

Returns a list of UIDs displayed in the internet browser. By default, the maximum number of results is limited to 20. 
* To change the number of results or add in other optional parameters, see [ESearch](reference_guide/esearch.md) for more information.


**Example**

[https://eutils.ncbi.nlm.nih.gov/entrez/eutils/egquery.fcgi?term=asthm](https://eutils.ncbi.nlm.nih.gov/entrez/eutils/egquery.fcgi?term=asthma)

---

# EGQuery

To use EGQuery:
1.	Start with the base URL: https://eutils.ncbi.nlm.nih.gov/entrez/eutils/egquery.fcgi? 
2.	Add required parameters to the base URL
* If more than one parameter, join with an ampersand (&) 
* Do not include spaces

| --- | --- | --- |
| EFetch Required Parameters  | Description | Example |
| db | Database you want to search | db=pubmed |
| id  | One UID or a set of UIDs separated with commas that you want a document summary. <br> There is no set maximum for the number of UIDs that can be passed to EFetch, but if more than about 200 UIDs are provided, the request should be made using the HTTP POST method **LINK TO POST METHOD**  | id=40654110|

3. Paste the URL with parameters into any internet browser and press **Enter** key

**Result**

Instead of returning the actual records, EGQuery provides the number of matching records in each database, which is useful for quickly assessing the scope of your query across different NCBI databases.

**Example**

[https://eutils.ncbi.nlm.nih.gov/entrez/eutils/egquery.fcgi?term=asthma](https://eutils.ncbi.nlm.nih.gov/entrez/eutils/egquery.fcgi?term=asthma

---

# EInfo
To use EInfo:
1.	Start with the base URL: https://eutils.ncbi.nlm.nih.gov/entrez/eutils/einfo.fcgi? 
2.	Add required parameters to the base URL
* If more than one parameter, join with an ampersand (&) 
* Do not include spaces

| --- | --- | --- |
| EINfo **Optional**  Parameters  | Description | Example |
| db | Database you want to search | db=pubmed |
| version | version | Used to specify version 2.0 EInfo XML. The only supported value is ‘2.0’. |
| retmode | format | Determines the format of the returned output. The default value is ‘xml’. Also ‘json’ is supported. |

3. Paste the URL with parameters into any internet browser and press **Enter** key

**Result**

EInfo provides one of the following:
* When a database parameter is given, statistics for a single database including lists of indexed fields and link names returns
* When no database parameter is given, a list of the names of all valid databases returns

**Examples**

[https://eutils.ncbi.nlm.nih.gov/entrez/eutils/einfo.fcgi?db=protein](https://eutils.ncbi.nlm.nih.gov/entrez/eutils/einfo.fcgi?db=protein)

[https://eutils.ncbi.nlm.nih.gov/entrez/eutils/einfo.fcgi?db=protein&version=2.0&retmode=json](https://eutils.ncbi.nlm.nih.gov/entrez/eutils/einfo.fcgi?db=protein&version=2.0&retmode=json)

---

## ESpell

To use ESpell:
1.	Start with the base URL: https://eutils.ncbi.nlm.nih.gov/entrez/eutils/espell.fcgi? 
2.	Add required parameters to the base URL
* If more than one parameter, join with an ampersand (&) 
* Do not include spaces. Spaces may be replaced by '+' signs

| --- | --- | --- |
| ESpell Required Parameters  | Description | Example |
| db | Database you want to search | db=pubmed |
| term  | Word or phrase you want to search for in the database. Spaces may be replaced by '+' signs. | term = asthma |

3. Paste the URL with parameters into any internet browser and press **Enter** key

**Result**

Provides spelling suggestions for terms within a single text query  

**Example**

[https://eutils.ncbi.nlm.nih.gov/entrez/eutils/espell.fcgi?db=pubmed&term=asthmaa+OR+alergies](https://eutils.ncbi.nlm.nih.gov/entrez/eutils/espell.fcgi?db=pubmed&term=asthmaa+OR+alergies)


---

# ECitMatch
To use ECitMatch:
1.	Start with the base URL: https://eutils.ncbi.nlm.nih.gov/entrez/eutils/ecitmatch.fcgi? 
2.	Add required parameters to the base URL
* If more than one parameter, join with an ampersand (&) 
* Do not include spaces

| --- | --- | --- |
| EINfo Required Parameters  | Description | Example |
| db | Database you want to search | db=pubmed |
| bdata | Citation strings | Each input citation must be represented by a citation string in the following format:<br>
journal_title|year|volume|first_page|author_name|your_key|
 |
| retmode |  format | Determines the format of the returned output. The default value is ‘xml’. Also ‘json’ is supported. |

3. Paste the URL with parameters into any internet browser and press **Enter** key

**Result**

ECitMatch 
* Retrieves PubMed IDs (PMIDs) that correspond to a set of input citation strings. 

**Examples**

[https://eutils.ncbi.nlm.nih.gov/entrez/eutils/einfo.fcgi?db=protein](https://eutils.ncbi.nlm.nih.gov/entrez/eutils/einfo.fcgi?db=protein)

[https://eutils.ncbi.nlm.nih.gov/entrez/eutils/einfo.fcgi?db=protein&version=2.0&retmode=json](https://eutils.ncbi.nlm.nih.gov/entrez/eutils/einfo.fcgi?db=protein&version=2.0&retmode=json)

---


## EPost

To use EPost:
1.	Start with the base URL: https://eutils.ncbi.nlm.nih.gov/entrez/eutils/epost.fcgi? 
2.	Add required parameters to the base URL
* If more than one parameter, join with an ampersand (&) 
* Do not include spaces

| --- | --- | --- |
| ESummary Required Parameters  | Description | Example |
| db | Database you want to search | db=pubmed |
| id  | One UID or a set of UIDs separated with commas. All must be from same database  | id=40654110|

3. Paste the URL with parameters into any internet browser and press **Enter** key

**Result**

Epost does the following: 

* Uploads a list of UIDs to the History server 
* Appends the list of UIDs to an existing set of UIDs attached to a Web Environment or creates a new Web Environment if one does not yet exist.


**Examples**

Post UIDs to History Server:

[https://eutils.ncbi.nlm.nih.gov/entrez/eutils/epost.fcgi?db=pubmed&id=11237011,12466850](https://eutils.ncbi.nlm.nih.gov/entrez/eutils/epost.fcgi?db=pubmed&id=11237011,12466850)

Attach UIDs to Web Environment

[epost.fcgi?db=protein&id=15718680,157427902,119703751&WebEnv=1](epost.fcgi?db=protein&id=15718680,157427902,119703751&WebEnv={webenv string})