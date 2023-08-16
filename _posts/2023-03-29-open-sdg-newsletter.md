---
title: Newsletter 1 - March
exerpt: Open SDG's first ever newsletter!
author_profile: false
---

Welcome to our first newsletter which we aim to issue throughout the year to keep our Open SDG users and community up to date with the latest relevant information. 

## Let’s talk... accessibility 

Open SDG incorporates many accessibility features that allows each platform to be accessible for most users. The UK SDG site conducts annual testing to meet the [Web Content Accessibility Guidelines version 2.1](https://www.w3.org/TR/WCAG21/) [AA standard.](https://digitalaccessibilitycentre.org/index.php/ons-sustainable-development-goals/)This involves end to end testing to make content more accessible to a wider range of people with disabilities, including accommodations for blindness and low vision, deafness and hearing loss, limited movement, speech disabilities, photosensitivity, and combinations of these, and some accommodation for learning disabilities and cognitive limitations. Many improvements are made available to Open SDG for everyone to make use of. 

 

Here is a list of features included in Open SDG to make platforms accessible as standard: 

* Chosen an easy-to-read font (open sans) 

* High contrast mode  

* Highlighted boxes when you click on things  

* Can navigate the site using just the keyboard  

* Screen readers can be used to listen to the website  

* Speech recognition can be used to navigate around the website  

* Default map colours are as accessible as possible  

* Can zoom in up to 300% without the text spilling off the screen  

* Can use the website on any device including mobile phones and tablets 

* Default language has been kept simple 

 

Before you make changes to your platform, it may be worth considering whether this affects the accessibility of the site, such as customising the map colours. 

 

## Success stories 

We are excited to announce that the Vanuatu Bureau of Statistics have been working hard on their Open SDG platform by developing the functionality to create a progressive web app from their website. This allows their users to utilise the website via an app on their mobile phone, tablet and/or desktop, wherever they are and even when offline.  

 

Thanks to Vanuatu’s work, we have been able to adapt this functionality more widely to Open SDG so it will be a new feature of the upcoming 2.2.0 release we are working on. This will allow all Open SDG users to apply the same functionality if they wish to enable their users to access the platform via an app on their phone!  

 

<ins>Quote from Chief Statistician, Benuel Lenge:</ins>

"Vanuatu’s National Sustainable Development Plan (NSDP) is the country’s highest policy framework and has been aligned to the Sustainable Development Goals (SDGs). The NSDP Platform & Mobile App will put official statistics in the hands of policy and decision-makers wherever they are, helping to build the statistical capacity of the country." 

 

Also, congratulations to Turkey who have recently launched their national reporting platform [here](https://sdg.tuik.gov.tr/). You can check out all Open SDG live platforms on our community page [here.](https://open-sdg.org/community) 

 

## Latest hotfixes/GitHub discussions 

There are three main fixes relevant to most Open SDG platforms that have been needed over the past few months to enable builds to run. These have been added to the [Open SDG Discussions board](https://github.com/open-sdg/open-sdg/discussions) on GitHub. The most recent is the [Openpyxl](https://github.com/open-sdg/open-sdg/discussions) issue which is outlined below. The other two, relating to [Ruby version 2.6.x](https://github.com/open-sdg/open-sdg/discussions/1884) and [cached property](https://github.com/open-sdg/open-sdg/discussions/1923) build errors, may still be relevant if you have not come across these already since December 2022. 

 

### Openpyxl update 

You may be experiencing a build failure with the following error:  

 

AttributeError: 'ReadOnlyWorksheet' object has no attribute 'defined_names'  

 

This is due to the python library, openpyxl, being updated so we need to pin the requirements.txt file to the previous version that Open SDG uses – see discussion on GitHub for the code to fix [here](https://github.com/open-sdg/open-sdg/discussions/1947). 



 If you would like to recieve this newsletter you can sign up by emailing [opensdg@outlook.com](opensdg@outlook.com)
