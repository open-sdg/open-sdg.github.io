---
title: Newsletter 2 - July
exerpt: The second edition of Open SDG's newsletter
author_profile: false
---
Just a reminder that version 2.2.0 has been officially released. [Watch this video](https://www.youtube.com/watch?v=a6OEIyLwwSE) to learn about the main features of the release and [follow these instructions](https://open-sdg.readthedocs.io/en/latest/upgrades/upgrading-2-2-0/) to upgrade your platform.


## Let’s talk... Search Engine Optimisation (SEO) 
One of the main features in the 2.2.0 release are the SEO improvements that have been made to Open SDG. Here is a little more information to understand the importance of SEO for your platform and how you can benefit from the improvements if you upgrade your platform.  

### What is SEO? 
Search Engine Optimization (SEO) is the process of improving the visibility of your website in the search engine results pages (SERP) e.g. Google, Bing. The goal of SEO is to increase the organic traffic to your site. The focus of the updates to Open SDG is on [On-page SEO.](https://backlinko.com/on-page-seo) This means optimizing the content and code of your platform to make it more search engine friendly. Adding these customization options gives users the ability to include relevant keywords, creating clear and concise titles and descriptions to drive more traffic to your site. 

The two SEO additions to Open SDG are Meta Tags & Goal Page H1s & H2s: 
 
### Meta Tags 
[Title tags](https://www.constantcontact.com/blog/website-seo-title-tag/#:~:text=A%20title%20tag%20is%20a,These%20are%20the%20title%20tags.) and [meta descriptions](https://moz.com/learn/seo/meta-description) are two crucial elements of SEO. Title tags are the clickable headlines that appear in SERP, while meta descriptions are brief summaries of the page's content. Both title tags and meta descriptions can help improve your website's click-through rate (CTR), which is the percentage of people who see your listing in the SERPs and click on it. 
 
### Goal Page H1s & H2s 
[H1 and H2 tags](https://clictadigital.com/how-to-use-h1-h2-and-h3-header-tags-for-seo-effectively/#:~:text=To%20break%20it%20down%2C%20remember,content%2C%20making%20it%20easily%20scannable) are HTML elements that are used to define headings in a web page. H1 tags are the most important headings, followed by H2 tags. Heading tags are crucial for SEO because they help search engines understand your content and the topics that your website is about. They also help users scan your content to find the information they are looking for. 
 
For information on how to implement these to your platform see our [guidance page.](https://open-sdg.readthedocs.io/en/latest/upgrades/upgrading-2-2-0/#search-engine-optimization-seo-customisation-options) 
  
## Success stories 
Well done to all users who have already upgraded to 2.2.0 and thanks to those who helped with the testing of features! We’ve put together a [short video](https://www.youtube.com/watch?v=VjBUqQ6ED28) demonstrating one of our key features of the release – the Progressive Web App which allows users to access their Open SDG platform from an app on their phone, even when offline. 
Also, congratulations to [Ingolstadt](https://sdg.nachhaltigkeitsagenda-ingolstadt.de/) and [Enzkreis](https://agenda2030.enzkreis.de/) who successfully launched their regional reporting platforms in June! 
 
## Latest hotfixes/GitHub discussions 
Pydantic error 
Data builds have been erroring with the message: “cannot import name 'make_generic_validator' from 'pydantic.class_validators'.” This can be easily fixed by adding the line: “pydantic==1.*” to your requirements.txt file in your data repository. See the announcement on GitHub for more details. 

 If you would like to recieve this newsletter you can sign up by emailing [opensdg@outlook.com.](opensdg@outlook.com)
