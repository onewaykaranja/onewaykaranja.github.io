+++
title = 'G00gle Dorking'
date = 2024-06-12T09:12:31Z
tags = ["research", "internet"]
+++

## Understanding Google dorking
 
Google dorking or google hacks, this is uses specific queries to find information that wouldn't be easily accessible from a normal google search.
Do not worry this is completely legal as the information is open source.

What you need is an internet connection and a browser that supports dorking queries(most browsers).
While doing research or recon 'dorking' definitely comes through.Below are some examples of intresting dorks:

```
1. “not for public release” filetype:pdf
2. inurl:/t/ (portal OR intranet OR login)
3. allintext: “zakayo” 
4. wwwboard WebAdmin inurl:passwd.txt wwwboard|webadmin
5. filetype:txt inurl:@passwords
6. filetype:log inurl:password
7. inurl:admin intitle:index.of
8. inurl:view/view.shtml axis
9. intitle:index.of inurl:backup

# fun ones
1. inurl:fun intitle:humor
2. inurl:comic site:imgur.com
3. meme generator intitle:create
4. garfield site:youtube.com

```
Google has made it easier to understand your syntax and craft your queries with [google advanced search.] (https://www.google.com/advanced_search)

## Crafting your query
#### Basic Operators:

AND (or &&): Use this operator to include multiple keywords in your search query i.e ``` "puss AND boots."```      
OR (or ||): This operator broadens your search by including results that contain either of the specified keywords i.e ``` "black OR brown." ```   
NOT (or !): Excludes specific keywords from your search results i.e ``` "green NOT greens"  ```  
  
#### Phrase Search:

Use quotation marks to search for an exact phrase. For instance,``` "brown paper" ``` will only return results with that exact phrase.  

#### Site-specific Search:

The "site:"  operator restricts your search to a specific website or domain. For example,``` "site:x.com Christopher Hadnagy" ``` will only show results about Christopher Hadnagy from the "x.com" website.
Filetype Search:

The "filetype:" operator allows you to specify the type of file you're looking for. This is useful for finding specific formats like PDFs, Word documents, Excel sheets, etc. For example, ``` "cv filetype:pdf" ``` will search for resumes in PDF format.  

#### Intitle and Inurl Search:

The "intitle:" operator searches for a specific word or phrase in the title of a web page. For instance, "intitle:admin" will return results with "admin" in the title. 
Similarly, the "inurl:" operator searches for keywords in the URL of a web page i.e ``` "inurl:blog phishing"  ``` will find pages with "blog" in the URL and related to phishing.

#### Exclusion Operators:

Use a hyphen (-) before a word to exclude it from your search results i.e ``` "green -greens" ```will exclude results that mention greens.
Specific Number Ranges:

Use two periods (..) between numbers to specify a range. For example, ```"camera $50..$100"``` will search for cameras priced between $50 and $100.  

#### Related Searches:

The "related:" operator finds websites similar to a specified URL. For instance,``` "related:x.com" ```will show sites similar to "x.com."

#### Cache and Similar Pages:

Use "cache:" to view the cached version of a web page. For example, ```"cache:x.com."```  
The "similar:" operator finds pages similar to a specified URL. For instance, ```"similar:x.com."``` 

#### Combination Techniques:

Combine multiple operators to create more targeted searches. For example, ```"site:x.com intitle:backup filetype:pdf" ```will search for PDFs about backups on the "x.com" website.  

#### Wildcards:

Use an asterisk (*) as a placeholder for unknown or variable words in a phrase. For instance, ``` "microsoft word * documents" ``` will return results with various completions of the phrase.  

#### Parentheses:

Use parentheses to group keywords and create more complex queries. For example,``` "(black OR brown) AND (colour review)" ```will search for colour reviews related to either black or brown.

#### Language and Region:

Specify the language of the search results with "language:" or the region with "gl=." For example, ``` "movie language:french"  ``` or  ``` "movie gl=fr" for ``` French results.

#### Date Range:

Use "before:" and "after:" operators to specify a date range for your search. For instance,``` "Shogun after:2024-01-01 before:2024-12-31." ```

#### Custom Search Engines:

Create custom search engines for specific sites using ``` "site:," "filetype:," ``` and other operators to focus your searches on particular domains or file types.

More on dorking in [HTB](https://www.hackthebox.com/blog/What-Is-Google-Dorking) & [stationX](https://www.stationx.net/google-dorks-cheat-sheet/)
