# EUtilities Reference Guide

## EUtilties API URL

EUtility API query URLs have three parts:

* Base URL
* EUtility endpoint
* One or more parameters

Figure 1. Parts of the Entrez API Query

![Parts of the Entrez API Query](apiurlparts.png)

### Base URL

All EUtility queries start with this base url: &nbsp; **https://eutils.ncbi.nlm.nih.gov/entrez/eutils/** .

### Endpoints

The EUtilities API offers nine EUtility endpoints. In Table 1, see the list of EUtility endpoints with a brief description. For more information about each EUtility endpoint, in Table 1 click the endpoint in the first column to go to a page with detailed information. 

Table 1: List of E-utilities in Order of Use

| **EUtility&nbsp;Endpoint** | **Brief Description**  |
| --- | --- |
| ESearch  | Returns a list of UIDs from a single database containing the searched text |
| ESummary   | Downloads document summaries for each UID  |
| EFetch | Returns a full data record |
| EGQuery  | Searches for text in NCBI databases and returns the number of results for each database  |
| ELink  | Returns a list of UIDs for records that are linked between two databases. <br> The UIDs returned by elink can be passed on directly to epost, esummary, or efetch.  |
| EInfo    | Retrieves information and statistics about a single database, including indexing fields and available link names. <br>If no database is provided, EInfo returns the list of current databases in the network.  |
| ESpell    | Returns spelling suggestions for a text query   |
| ECitMatch | Searches PubMed for citations |
| EPost | Saves a list of UIDs to use with other E-utilities like ESummary or EFetch |

## EUtilities Parameters

Parameters are options you add to the base URL and EUtility to refine the results. Each EUtility has required and optional parameters. Null values or inappropriate parameters are generally ignored.

See Table 2 for a list of the most commonly used parameters. For a full list, see E-utilities Parameters for the required and optional parameter options for each EUtility.

| Parameter | EUtilities that Use it | What Does it Do? | Example | 
| --- |--- |--- |--- |
| Database | EInfo <br>ESearch<br> ESummary <br>EPost<br>ELink<br>ESpell<br>ECitMatch<br>EFetch | Limits results to the provided database |db=pubmed | [See list of database names BROKEN LINK FIX ME] |
| Term | EGQuery <br> ESearch <br> ELink <br> ESpell | Queries for the term you provide  | term=asthma 
| UID | ESummary <br> epost<br>elink<br>EFetch  | Limits results to the provided UIDs <br> For more than one UID, add a comma to separate<br> See UIDs for more information  ADD LINK HERE| id=19393038,30242208,29453458 |  
| usehistory | esearch <br>  OTHERS | Saves results to use with a subsequent EUtility query | usehistory=y |
| retmax | esearch <br> esummary | Total number of DocSums from the input set to be retrieved, up to a maximum of 10,000 | retmax=100 |
| retmode | esummary <br>einfo<br>esearch<br>efetch<br>elink | Formats of the output | retmode=json <br>retmode=xml  | xml is default |
| reldate | esearch | Sets the days to be searched relative to the current date, set reldate=1 for the most recent day | reldate=1 |
| mindate <br> maxdate |  esearch <br> elink | Specifies the date according to the format YYYY/MM/DD, YYYY, or YYYY/MM  <br> A query must contain both mindate and maxdate parameters| mindate=2000/01<br> maxdate=2022/12  | A query must contain both mindate and maxdate parameters | 

