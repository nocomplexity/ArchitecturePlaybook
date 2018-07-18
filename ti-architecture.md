# Technology Infrastructure (TI) Architecture


A Technology Infrastructure (TI) Architecture is all about the hard IT.
Hosting, capacity, connectivity, monitoring and operations. Having a
flexible TI architecture serves all business processes.

Tools for creating a Technology Infrastructure Architecture:

-   [IP Address range
    calculator](https://nocomplexity.com/networkip-calculator/)
-   [Simple Network Bandwidth
    Calculator](https://nocomplexity.com/simple-network-bandwidth-calculator/)
-   [Simple Capacity Calculator for web
    servers](https://nocomplexity.com/simple-capacity-calculator/)

For systems that are not using PaaS Cloud Services a lot of attention,
time and effort is needed for the TI part of the system. Below some TI
templates that will make with creating the technical solution.

TI Templates:

-   [Technical
    Architecture (MSWORD)](http://www.dot.state.fl.us/ois/PDM/4_Design/Technical%20Architecture.docx).
    Template used at US Florida Department of Transportation.
-   [High-Level Technical
    Design (MSWord)](https://www.cms.gov/research-statistics-data-and-systems/cms-information-technology/xlc/downloads/highlvltechdesign.docx).
    HLD Template used at US Centers for Medicare & Medicaid Services.
-   [System Design
    Document (MSWord)](https://www.cms.gov/research-statistics-data-and-systems/cms-information-technology/xlc/downloads/systemdesigndocument.docx).
    Source US CMS.
-   [Service Design & Transition
    (MSWord).  ](http://fitsm.itemo.org/sites/default/files/FitSM_Template_Service_design_and_transition_package_1.1-final.docx)
    Source [EU FitSM
    program](http://fitsm.itemo.org/fitsm-templates-samples-guides).
-   [IT Service Capacity Plan (MSWord).  Source EU
    FitSM program.](http://fitsm.itemo.org/sites/default/files/FitSM_Sample_Capacity_Plan_v1.docx)

## Abstraction Tools

To be flexible and remain portable open interfaces you SHOULD think of using abstraction layers.
Abstraction layers on TI level can make your implementation easier. But the trade-off is of course that using an extra layer adds another dependency. 

Good TI abstraction Tools to be used are:
* Apache Libcloud (http://libcloud.apache.org/). Apache Libcloud is a Python library which hides differences between different cloud provider APIs and allows you to manage different cloud resources through a unified and easy to use API. Great documentation which offers standardization over the fuzzy Cloud Terms are included, check: https://libcloud.readthedocs.io/en/latest/index.html