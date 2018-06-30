# StardogRevit-synchronizer

* note: tested for Revit v2018.3 and Stardog triplestore v5.2.1. Future versions of this plugin might include other SPARQL endpoints to communicate with
* note: dynamo script needs Dynamo for Revit v1.3.3 installed for the used Revit version
* note: this version of the Dynamo script expects RDF triples according to an older version of BOT, which is made available in this repo: `Linked Building Data ontologies/bot_v0.2.0_20171027.ttl`

## Installation details
0) Download or Git clone this repository to your computer
1) Download and install the following Dynamo packages via the Dynamo package manager:
>- archi-lab.net				2016.13.3
>- Bakery					2018.4.301
>- Clockwork for Dynamo 1.x	1.0.3
>- Data-Shapes				2018.3.9
>- DynaTools					2018.1.15
>- JsonData					1.1.4
>- LunchBox for Dynamo		2017.10.4
2) Copy the custom nodes in the 'Custom Dynamo nodes' folder to following folder on your drive: 

`C:\Users\<USER-NAME>\AppData\Roaming\Dynamo\Dynamo Revit\1.3\definitions`

3) Make sure a Stardog triplestore instance is running on [localhost:5820]()

`stardog-admin.bat server start`

>* note: the script now uses the default username:admin/pw:admin settings of Stardog, which should be safe as long as the Stardog instance is running locally
4) Close and open Dynamo so it will find the new custom nodes
5) Run each of the four numbered Dynamo scripts in the indicated order (.dyn)
>* note: in script 'PART4 - elements', the Excel mapping file 'MappingTable_RevitCategories-to-Product.xlsx' is found via a relative path starting from the Dynamo script location. Please leave the mapping file in its location for the script to function properly. 

## Details about the UI of the scripts
TBA

## Acknowledgement
This research is funded by the Research Foundation Flanders (FWO) in the form of a personal Strategic Basic research grant. 

Contributions were made by Mads Holten Rasmussen.
