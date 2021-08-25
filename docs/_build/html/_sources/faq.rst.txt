================================
Frequently asked questions
================================

+--------------------+------------+----------------------------------+
| *Document version* | *Date*     | *Authors*                        |
+====================+============+==================================+
| 1.0                | 2021-07-23 | D. Čápová, P. Kramolišová, L.    |
|                    |            | Kondrová, O. Moravcová           |
+--------------------+------------+----------------------------------+

*Last update:* 2021-07-23

*More questions:* egdi.metadata@geology.cz

Here is a pdf file of this FAQ :download:`pdf <_static/micka_faq.pdf>`

Metadata URL for uploading data
================================

**Question:** *I have tried to create a new EGDI metadata item, but I
still don’t understand how I get the URL which is required to upload the
actual data at the Admin
module*\ https://egditest01.geus.dk/egdiadmin/geopack.jsp\ *.*

**Answer:** Requested URL is the URL on Basic metadata view of your
record in the EGDI Metadata Catalogue.

For example, URL of example metadata record is: 

https://egdi.geology.cz/record/basic/5e8b7243-18b0-4d85-ab71-36680a010833

See picture:

|image1|

Inability to save metadata record
==================================

**Questions:** *Why it is not possible to save the record in editing
form?*

**Answer:** The required fields highlighted in red are left blank (see
picture below). You have to fill them in first, otherwise the record
cannot be saved as it is described in the Cookbook
(https://egdi.geology.cz/layout/egdi/MetadataCookbook_Lite.pdf) on page
15.

|image2|

Metadata record not visible to all users
========================================

**Question**: *Why is my newly created record not visible to my
colleague?*

**Answer:** Metadata **status of this record** is “Private”. Your
colleague views the record as an unlogged user. To make the record
visible to public, you must set the *Status*: “\ **Public”** and *For
viewing*: “\ **reader”**. See picture:

|image3|

Search metadata by *Project Name*
=================================

**Question:** *Why can´t I find my metadata in the EGDI Metadata
Catalogue when searching by Project name keyword, for example
“Mintell4EU” (picture below)?*

|image4|

**Answer:** You did not enter the right project name keyword from the
code list in your metadata record; you should select the appropriate
*Project name* as a keyword from the list. See picture:

|image5|

A common mistake is to include the project name as a *Free keyword*.
After that, the record can only be found using the full text search.

Upload metadata from XML file 
==============================

**Question:** *Is it possible to upload metadata from XML file to the
EGDI Metadata Catalogue?*

**Answer:** Yes, of course, see picture below with steps 1. to 5. as red
hints. The complete workflow is described in more details in the
Cookbook (https://egdi.geology.cz/layout/egdi/MetadataCookbook_Lite.pdf)
in the Chapter 3.1 on page 8.

Keep in mind that your xml file must meet international standards.

|image6|

Use of example records 
=======================

**Question:** *Is there any example record for creating metadata? Can I
use it as a template or to do a copy and edit it to create my own
metadata record?*

**Answer:** Yes, there are 3 examples:

-  **Dataset example record:**

https://egdi.geology.cz/record/basic/5e8b7243-18b0-4d85-ab71-36680a010833

-  **3D model dataset example record:**

https://egdi.geology.cz/record/basic/5e8b358e-7998-4f71-a363-2b260a010833

-  **Service example record:**

https://egdi.geology.cz/record/basic/5e8e29b8-e334-4b30-b78b-14750a010833

Unique resource identifier as URI
==================================

**Question:** *Is there any recommended URI format for the Identifier (item 5 Unique resource identifier in the EGDI Metadata Profile) or is there any agreed convention for its definition?*


**Answer:** There is no official standard other than formal URL rules,
but it is our effort to define uniform rules in EGDI. For example
*Identifier* as URI of harvested metadata from the Czech Geological
Survey is as follows: https://registry.geology.cz/id/VDC-POD-WMS, where
[https://registry.geology.cz/id] represents the domain, [VDC] represents
the thematic database within CGS data store, [POD] represents the data
set name, and [WMS] represents the type of access to the data set. For
data which are available and uploaded to the EGDI Map Viewer it is
recommended to begin the URI identifier with the EGDI domain:
http://www.europe-geology.eu/id .....

**Example URI:** http://www.europe-geology.eu/id/mineral-resources/

Adding Web Map URL to the dataset metadata as an on-line Resource Locator 
==========================================================================

**Question:** *I couldn’t find a link in my metadata record of
dataset to see appropriate uploaded data on the EGDI portal. What
should I do?*

**Answer:** After uploading your data to the EGDI Map Viewer via the
Admin module, return to your metadata record in the EGDI Metadata
Catalogue. In the EGDI-Lite editing form add a link to the Service from
the EGDI Map Viewer to the item “\ *4 Resource locator*\ ” of the
metadata record for related dataset. See picture below:

|image7|

Linking of dataset metadata - Source Citation and Parent Identifier elements
=============================================================================

**Question:** *How to link a*\ **Pan-European metadata**\ *record to
national records?*

**Answer:** It depends on how the related data layer is created and what
the relationship should express.

1. The data relationship when **“something is part of something else”.**
   The resulting dataset is a superset with lower units - subsets (like
   a book with its chapters). In the subset record, select the higher
   item from the list in item **30 Parent Identifier**.

|image8|

2. The data relationship when "**something comes out of/uses
   something**". The resulting layer is created by transforming or
   compiling other resources (modifying them, such as geographic or
   semantic harmonization). These resources must be identified by the
   item **31 Sources** (list the sources citation). If the source
   metadata does not exist in the EGDI Metadata Catalogue, the URL of
   the external metadata in xml can also be entered in the field.

|image9|

Metadata of a set of spatial products for one area
===================================================


**Question**: *If we upload a set of spatial products (e.g. temperature map, fault network, transmissivity map, etc.) covering the same area and coming from the same author/partner, does each single layer require a separate metadata entry or can we pool it for each set coming from the same author/partner, listing what the single layers are? For now, we applied the latter way, see the coupled resources (11 children / grandchildren) of* https://egdi.geology.cz/record/basic/602f94c8-8bfc-42b6-a8a2-61070a010833 


**Answer**: We think it is correct, see answer 9.1.

Validation of 3D models extended by vertical items compared to INSPIRE validation
=================================================================================

**Question**: *Why validation panel requires vertical reference system
and extent (item 22 and 23), when my metadata are 2D?*

**Answer**:

As described in the Cookbook
(https://egdi.geology.cz/layout/egdi/MetadataCookbook_Lite.pdf) on page
20, item **12 Presentation form,** filled as value **“Model digital”,**
is mandatory for 3D models. When selected from the codelist, the
validation rules change to meet the metadata description requirements of
the 3D models. You can also select the value “Model digital” for your
**2D dataset,** but then **do not worry about validation of vertical
items**. This is only required for 3D models.

|image10|

*Didn't find what you were looking for? Still have questions? Need help?
Send us an email on*: egdi.metadata@geology.cz

.. |image1| image:: _static/images/faq/media/image1.png
   :width: 6.29861in
   :height: 4.47431in
.. |image2| image:: _static/images/faq/media/image2.png
   :width: 5.9in
   :height: 3.90833in
.. |image3| image:: _static/images/faq/media/image3.png
   :width: 5.98333in
   :height: 0.30833in
.. |image4| image:: _static/images/faq/media/image4.png
   :width: 6.29566in
   :height: 4.03381in
.. |image5| image:: _static/images/faq/media/image5.png
   :width: 6.29861in
   :height: 1.97431in
.. |image6| image:: _static/images/faq/media/image6.png
   :width: 6.30208in
   :height: 5.69792in
.. |image7| image:: _static/images/faq/media/image7.png
   :width: 6.29861in
   :height: 6.01319in
.. |image8| image:: _static/images/faq/media/image8.png
   :width: 6.3in
   :height: 2.55502in
.. |image9| image:: _static/images/faq/media/image9.png
   :width: 6.3in
   :height: 1.72348in
.. |image10| image:: _static/images/faq/media/image10.png
   :width: 6.28542in
   :height: 2.07153in
