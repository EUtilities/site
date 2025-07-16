# EUtilities Usage Guidelines and API Key

## Usage Guidelines
 
To avoid overloading the EUtility servers, NCBI recommends the following:

* Post no more than three URL requests per second
* Limit large jobs to either weekends or between 9:00 PM and 5:00 AM Eastern time during weekdays

Failure to comply with this policy may result in an IP address being blocked from accessing NCBI. 

If NCBI blocks an IP address, you must:

* Register your email and tool information with NCBI
* Include this information in all subsequent EUtility requests from that software package

---

### Register Your Tool and Email

The values for tool and email must be registered with NCBI. 

* Providing values for tool and email in requests is not sufficient to comply with this policy. 
* Requests from any IP that lack registered values for tool and email and that violate the above usage policies may be blocked. 
* Software developers may register values of tool and email at any time and are encouraged to do so.

To register your tool and email, e-mail [eutilities@ncbi.nlm.nih.gov](eutilities@ncbi.nlm.nih.gov). Include the following information: 

* Name of either a developer or the organization creating the software
* The tool Information should be a string with no internal spaces that uniquely identifies the software producing the request. 
* The email should be a complete and valid e-mail address of the software developer and not that of a third-party end user
     - The email will be used only to contact developers if NCBI observes requests that violate our policies. We will attempt to contact prior to blocking access. 

Once NCBI establishes communication with a developer, receives values for tool and email, and validates the e-mail address in email, the block will be lifted. 



**EUtilities Mailing List**

To get announcements of software updates, known bugs, and other policy changes affecting the EUtilities, request to be added to the EUtility mailing list at [eutilities@ncbi.nlm.nih.gov](eutilities@ncbi.nlm.nih.gov).

## API Key

An API key is only needed if you expect to access EUtilities at a rate of more than three requests per second. Without an API key, IP address posting more than 3 requests per second to the EUtilities will receive an error message. 

**Example Error Message if Rates are Exceeded**

`{"error":"API rate limit exceeded","count":"11"}`

By including an API key, a site can post up to 10 requests per second by default. Higher rates are available by request at [eutilities@ncbi.nlm.nih.gov](eutilities@ncbi.nlm.nih.gov). 

### Obtain an API Key

Users can obtain an API key from the Settings page of their NCBI account. To create an account, visit [http://www.ncbi.nlm.nih.gov/account/](http://www.ncbi.nlm.nih.gov/account/). After creating the key, include it in each EUtility request by assigning it to the api_key parameter. For example:

`api_key={API key value}`

To get your API key, follow these steps:

1.	While signed in to your My NCBI account, go to your NCBI Account Settings. To create an account, go to [https://account.ncbi.nlm.nih.gov/signup/](https://account.ncbi.nlm.nih.gov/signup/).
2.	Scroll to the bottom of the page to find the API Key Management section.
3.	Click the **Create API Key** button. A unique sequence of characters will be generated and displayed in the  API Key Management box. This is your API key.
    - Only one API key is allowed per NCBI account. 
    - You may request a new key at any time. 
    - Requests for new API Keys invalidate any existing API key associated with that NCBI account.

### Use Your API Key with EUtilities

To use your API key as a parameter in an NCBI EUtility API query, add the api_key parameter:

`esummary.fcgi?db=pubmed&id=123456&api_key={PUT_YOUR_API_KEY_HERE}`

 Note:  Do not include the curly braces.

###  Minimize the Number of Requests

If a query requires searching for and/or downloading a large number of records, use the [History parameter](/site/Reference_Guide/a_reference/#eutilities-parameters), which works in batches rather than using separate requests for each record.

**CHECK THIS LINK WORKS AFTER DEPLOYING**



