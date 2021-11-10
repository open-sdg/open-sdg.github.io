---
title: An introduction to SDMX by someone who has never heard of it...
excerpt: A first look at SDMX and some important lessons when using it
date: 2021-11-10
---

This post covers some key takeaways if you are encountering Statistical Data and Metadata eXchange (SDMX) for the first time. A couple of months ago, that was me. So, I've looked at important lessons and highlighted resources to help improve your understanding.

SDMX is an ISO standard designed to describe statistical data and metadata. When we exchange complex data, it can be expensive, resource intensive and time consuming. SDMX can help us improve this, especially when we send data abroad.

If we all used SDMX we would break down the organizational silos of data structure. This means we would be vastly more efficient and productive. That is obviously a long way off, yet, if everyone in your team used the same file formats, it would save huge amounts of time. Now imagine extending that to your entire organisation or country.

## Why SDMX?

SDMX is already used in many domains, including economics, agriculture, and social statistics. There are seven sponsor organizations driving this change, these include the UN, OECD, and World Bank. They have used their enormous leverage to ensure that the SDMX standard is widely used across these fields. 

During your work, you may have encountered files in the SDMX format. You are likely to have seen any number of CSV, JSON, XML and countless other file formats to store your data. The purpose of SDMX is to streamline this. A consistent format would mean no time-consuming converters, unrecognised extensions or corrupted files.

When we exchange data, it helps to have agreement on common concepts, structures, formats. Further, a stable, predictable exchange scheme saves time and reduces the likelihood of errors. 

Metadata is the data that provides detail on your statistical data. This is also standardised with SDMX. This means the structure of the data and reference metadata (content and quality of the data) meet a universal standard.

## Push/Pull Data Exchange

An important lesson to understand is whether your data exchange is a push or pull method.  When working with SDMX we use a pull method, this may be unfamiliar to you, however, this method of exchange is more efficient and secure.

Whenever you send an email, share a link, or give someone a storage device you are exchanging data. In most instances this will have been a push exchange, the receiver requests data and it is sent across. This causes a time lag, is labour intensive and therefore is less efficient. There is also a security risk of your data being stolen or intercepted.

Imagine your team needs to receive some complex, sensitive data from a supplier. Hypothetically, you could share this via email, link, or USB. However, you may encounter restrictions on what you can send and anyone who finds it will be able to access your data.

To improve the efficiency and security of this process, you could make a pull request of the information you need. The sender then uploads the data to a secure central platform. When SDMX data is uploaded to the online storage depository, you receive a notification. You bypass the constraints of sending directly as you can both access the shared platform.

This pull method adds an additional layer of security and takes less time to complete.  It also allows all team members with the correct permissions to collaborate on these files.  

## Experience with Mapping

An important consideration when working with SDMX is the need to map non-SDMX data. This can be difficult to grasp at first, however once your data is in the correct format it makes the entire process easier. 

For our dataset to be exchanged easily, we need a consistent organisation and set of criteria. This is known as the Data Structure Definition (hereafter DSD).  This acts as a template to describe the structure of a dataset in terms of its dimensions and coding. 

When converting your data to SDMX, the dimensions have a code list, this is a list of variable codes with descriptions for each. Coding principles here should follow the central standards (see below).

Learning to map CSV data to the SDMX format helped me grasp the requirements of the DSD. Each DSD has its own specific requirements, ensuring the data fits within these are the basis of mapping. First, it is worth familiarising yourself with the fundamental coding principles. This makes identifying dimensions and values that do not fit the DSD more intuitive. 

My initial experience with SDMX mapping demonstrated to me the need for agreement on coding. Making changes manually was time consuming and required some external guidance and discussion. Further, any time this source data is now updated, we will have to reproduce the changes required to make it SDMX compatible.

This experience helped teach me the fundamentals of SDMX but also demonstrated its necessity. Without agreement and consistency, exchanging data will continue to be complex and inefficient. 

## Additional Useful Resources

Introduction guidance: <https://sdmx.org/?page_id=2555> 

SDMX user guide: <https://sdmx.org/?page_id=1119>  

SDMX Guidelines: <https://sdmx.org/?page_id=4345> 

Learn how to convert files to SDMX: <https://webgate.ec.europa.eu/fpfis/wikis/display/RMSDE/SDMX+Converter+-+User+Guide> 

## SDMX Convertor

Eurostat SDMX Converter: <https://ec.europa.eu/eurostat/web/sdmx-infospace/sdmx-it-tools> 
