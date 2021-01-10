---
title: Open SDG - How we got here
excerpt: A history of the origins and evolution of the Open SDG reporting platform
---
The [UN Sustainable Development Goals](https://sustainabledevelopment.un.org/sdgs) (SDGs) set out an ambitious agenda to address the world’s most pressing challenges. This global action plan, which includes 17 goals and 169 targets that are tracked using 232 unique indicators, can only be achieved if data on the SDG indicators is made available to government decision makers and the general public.

Solutions for managing and publishing this data － known as SDG reporting platforms － can help governments save time and resources. The Open SDG reporting platform is a strong example of what collaboration using open-source tools can achieve. Open SDG grew organically from a collaboration of teams solving a common problem with a shared approach, and evolved into a full-fledged open-source project and community.

## Origins

The Open SDG story starts 2 years before its initial release. In 2016, the USA government launched an open-source platform for the SDGs at <https://sdg.data.gov>, leveraging open-source code that was originally developed by the City of Philadelphia. The design principles of these original implementations continue to be central to Open SDG today:

* Using open-source technologies
* Leveraging Github.com free services
* Fast and secure as a generated static site
* CSV data management

The UK Office for National Statistics forked this platform on GitHub and added a range of custom features, including disaggregation support, maps, high-contrast mode, and a separate web service for data. At the same time, the USA platform continued development by adding multilingual support. As part of its SDG National Reporting Initiative, the Center for Open Data Enterprise (CODE) connected with the USA and the UK to support and facilitate greater information sharing about open-source reporting platforms for the SDGs.

By 2017 these three teams were communicating regularly to compare notes and discuss new developments. Because both the USA and UK platforms were open-source, it was possible to share code and functionality between them. Additionally several other countries around the world began adopting the USA and UK SDG reporting platforms, including Ghana, Jamaica, Poland, and Rwanda.

## The need for Open SDG

Despite the successful implementations of the USA and UK platforms, and the continued adoption by other countries, there were two clear challenges that needed solutions:

* As the USA and UK platforms continued to diverge, it became more and more difficult to share code and features.
* With some countries adopting the USA platform, and others adopting the UK platform, there was not a "standard" approach.

The CODE team began to focus on the development necessary to combine the features from both platforms into a shared open-source library which could be used by all countries simultaneously. This approach aimed to solve the challenges mentioned above:

* As features were added to the shared library, they could immediately be used by all other countries without requiring any extra work.
* With a single library shared by all, documentation and outreach could become focused on one standard approach.

This project became known as "Open SDG" and was released in late 2018, as version 0.1.0. Both the USA and UK updated their platforms to use Open SDG. The project was hosted at <https://github.com/open-sdg> as a trio of repositories:

* [Open SDG](https://github.com/open-sdg/open-sdg): The core platform combining the USA and UK features into a re-usable library
* [SDG Build](https://github.com/open-sdg/sdg-build): A Python library for preparing and converting SDG data
* [SDG Translations](https://github.com/open-sdg/sdg-translations): A repository for translating the platform to an ever-growing number of languages.

## Path to 1.0.0

With the release of Open SDG as a shared platform, Open SDG itself (rather than the individual country platforms) became the focus of the teams' development efforts. Incremental versions were released over the course of 2019, from [version 0.2.0](https://open-sdg.readthedocs.io/en/latest/updates/#020) in January to [version 0.10.0](https://open-sdg.readthedocs.io/en/latest/updates/#0100) in November. In addition to the important release of [platform documentation](https://open-sdg.readthedocs.io/en/latest/) and automated tests, the releases during this time focused on adding new features and fixing bugs.

After reaching version 0.10.0, the next milestone was to release a "stable" 1.0.0 version. Version 1.0.0 was critical because it would represent a solidifying of the platform's evolving architecture. With this [intensive push towards 1.0.0](https://github.com/open-sdg/open-sdg/issues?q=project%3Aopen-sdg%2Fopen-sdg%2F5+) came a [project website](https://open-sdg.org/) and many improvements to the platform. The UK team during this time contributed resources to an expert review of the platform from the perspective of user-centered design, as well as a web accessibility audit. As a result, the usability and accessibility of the Open SDG platform received a great deal of attention, and improved significantly.

[Version 1.0.0](https://open-sdg.readthedocs.io/en/latest/updates/#100) was released in April of 2020.

## Growing community

As Open SDG grew in popularity a community formed around the project. This influx of new users and use-cases spurred on development and inspired new functionality. The Jekyll-based architecture of the platform proved to be successful in allowing any part of the platform to be altered by a country, and then allowing for those alterations to be contributed back to the project to become part of Open SDG.

The platform was adopted by [Germany](https://sustainabledevelopment-germany.github.io/), and the German team contributed greatly to the project, both by their involvement in the community and by their many examples of extensive platform customization. The city of [Los Angeles](https://sdgdata.lamayor.org/) also adopted Open SDG and initiated outreach about the platform, which was instrumental in producing new features allowing the platform to be used at the local level.

As more countries expressed interest in using [SDMX data](https://unstats.un.org/sdgs/iaeg-sdgs/sdmx-working-group/) rather than CSV, new functionality was added which allowed Open SDG to be used in an unexpected new way: as a front-end for a completely separate (non-CSV) data source. This has opened the door to adoption by many countries that may already have an established data back-end, but would like a front-end specialized for the SDGs.

Multiple webinars held during 2020 continued to spread the word about Open SDG. At the time of this writing, Open SDG is being used or developed in at least 20 countries and cities. The process of creating a new implementation of Open SDG has become progressively faster and less technical; to the point where it can now be done in less than an hour, using only a web browser.

## Looking ahead

So this brings us to where we － the Open SDG community － are today. As of January 2021 we are about to release version 1.2.0, and are already working on version 1.3.0. This open-source platform continues to adhere to those original design principles started years earlier, at the same time as it continues to accumulate features and functionality to better help countries and cities report their SDG data.
