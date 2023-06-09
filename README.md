# Database_parsing

A Jupiter notebook for parsing and structuring xml data in the context of our project **Drug Information Delivery** as a part of the course Assistive Technologies Challenge at EPFL.

The notebook 'create_db' is used extract meaningfull information about drugs in the Swissmedic database on Refdata. The data can be downloaded at https://sai.refdata.ch and https://www.swissmedicinfo.ch by clicking on "Download" at the top of the page.

*Instructions to run the notebook*

1 : Please Adapth the paths of the 2 downloaded zipped folders following the instructions at the start of the notebook. 

2 : Run the notebook to create/update 'drugdb.db' database. WARNING : This might take several minutes !

'drugdb.db' is a database type file. It contains 3 tables : 
- 'drug_leaflets' that contains 2 columns, index and content, content is a JSON object that contains a list of the section titles and paragraphs of the leaflet.
- 'gtin_lang_lookup' is a lookup table of 3 columns, GTIN, language and index, so that we get the index of the corresponding drug leaflet in the chosen language when scanning the GTIN number of a barcode on a drug box.
- 'packages_info' contains some additional informations to the drug packaging (authorization number, etc) that can be usefull for the developer.
