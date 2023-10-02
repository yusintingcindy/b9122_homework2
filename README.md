# b9122_homework2  
### This repository is created as part of an assignment for the "Computing for Business Research" course at the Columbia Business School. It contains python code files with sample codes for performing webcrawling.  

## Author Information  

**Name:** Cindy Yu  
**Course:** MS in Marketing Science  
**GitHub:** https://github.com/yusintingcindy   

## Description of Code Files  

**webcrawler.py:**  
This file contains codes which systematically visits up to 50 web pages under the domain www.gsb.columbia.edu and keeps track of the web pages that have been visited.  The process involves:  
(i) specifying www.gsb.columbia.edu as the starting web address (i.e. seed_url) and setting it as the first element of the list of web pages to visit; 
(ii) visiting the first element of the list of web pages to visit and removing it from the list;  
(iii) identifying hyperlinks on the web page and adding them to the list of web pages to visit if they meet certain requirements (e.g. they have not been seen before and are web pages under the specified domain);  
(iv) repeating steps (ii) and (iii) until 50 web pages have been visited (or there are no more web pages left in the list to visit).  

**hw2_question_1.ipynb:**  
This file has two parts, each of which contains codes to systematically extract press releases that satisfy certain requirements from the United Nations and the European Parliament websites respectively.  
  
***Part 1 - Extracting 10 United Nations press releases containing the word "crisis"***  
The process involves:  
(i) specifying https://press.un.org/en as the starting web address (i.e. seed_url) and setting it as the first element of the list of web pages to visit;  
(ii) visiting the first element of the list of web pages to visit and removing it from the list;  
(iii) checking if the web page is a press release;  
(iv) if the condition in step (iii) is met, checking if the press release contains the word "crisis" and if so, extracting the press release; 
(v) checking if the web page is the starting web page or a page titled "Press Release" containing all press releases;  
(vi) if the condition in step (v) is met, identifying hyperlinks on the web page and adding them to the list of web pages to visit if they have not been seen before;  
*Note: steps (v) and (vi) prevent us from further crawling web pages that would not contain hyperlinks to other press releases*  
(vii) repeating steps (ii) to (vi) until 10 press releases have been extracted (or there are no more web pages left in the list to visit).  

***Part 2 - Extracting 10 European Parliament press releases that cover the plenary session and contain the word "crisis"***  
The process involves:
(i) specifying https://www.europarl.europa.eu/news/en/press-room as the starting web page (i.e. seed_url);  
(ii) visiting the starting web page;  
(iii) identifying hyperlinks that would lead to individual press releases and adding them to the list of web pages to visit if they have not been seen before;  
(iv) visiting the first element of the list of web pages to visit and removing it from the list;  
(v) checking if the web page is a press release that cover the plenary sessions;  
(vi) if the condition in step (v) is met, checking if the press release contains the word "crisis" and if so, extracting the press release; 
(vii) repeating steps (iv) to (vi) until there are no more web pages left in the list to visit;  
(viii) going back to the starting web address and clicking on the "load more" button (if the button exists);  
(ix) repeating steps (iv) to (viii) until 10 press releases have been extracted (or there is no longer a "load more" button on the start web page)
