# Technology Infrastructure (TI) Architecture


A Technology Infrastructure (TI) Architecture is all about the hard IT.
Hosting, capacity, connectivity, monitoring and operations. Having a
flexible TI architecture serves all business processes.

Creating a simple overview of your systems is key for understanding. Of course you can use the great [Archi](http://www.archimatetool.com/) to create Archimate TI views. But Archimate is not designed for the needs to get a good understandable overview of your TI components. Simple is better, so think of using the following tools for visualisation of your TI Architecture:

- [diagrams.net](https://www.diagrams.net/) General easy to use drawing software. Diagrams.net is open source, online, desktop and container deployable diagramming software. It has many default shapes and templates to create a quick system overview or network topology view quick.
- [Diagrams](https://diagrams.mingrammer.com/). Diagrams lets you draw the cloud system architecture in Python code. Also easy to integrate with Jupyternotebooks. Diagrams was created to program your Cloud system documentation. So it support shaped for many Cloud Providers.


When creating a Technology Infrastructure Architecture you SHOULD calculate network usage. This to prevent performance issues and availability issues. Think of calculating:

-   Network usage per user.
- IOPS usage per user and peak usage. This to check if your TI hosting provider meets your requirements.
- Network bandwidth peak usage.
- Average and peak network usage for some typical use cases.
Since you do not live in a perfect world you will be forced to use assumptions. But document it and improve the calculations when major changes or incidents occur.

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
* [Apache Libcloud](http://libcloud.apache.org/). Apache Libcloud is a Python library which hides differences between different cloud provider APIs and allows you to manage different cloud resources through a unified and easy to use API. Great documentation which offers standardization over the fuzzy Cloud Terms are included, check: https://libcloud.readthedocs.io/en/latest/index.html