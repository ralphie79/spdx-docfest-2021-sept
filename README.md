# spdx-docfest-2021-sept
## What is this?
This repository is the home for an analysis application utilizing the [spdx/tools-python](https://github.com/spdx/tools-python) library to process the SPDX SBOM documents submitted for the [SPDX DocFest on 16 September 2021](https://drive.google.com/drive/u/0/folders/1k-9tTyCuzT3QKVy9CZPxvDFzrSY-m-ob) and the data that was summarized in the [final analysis report](https://docs.google.com/presentation/d/1Jwxc-rLQY2ZqH7VwFbGtWQKIIHXKqWQJ/edit#slide=id.gebff13e659_0_28)

## What's here?
This repository sadly contains only a single data file generated with now-irrevocably-deleted (always back up / push to remote, kids!) application that has the results of processing the submissions as they were on 13 September 2021

### Report Structure
The report is a JSON document consisting of an array of entries, each having:
* path;	    The path of the analyzed file
* type;     The type of SPDX SBOM detected, from the supported choices of [JSON, YAML, RDF, XML, TV]
* error;    Whether or not processing errors were encountered
* status;   Status of document parsing and the text of any 'error' if failed
* log;      Array of strings representing the internal log messages from this analysis tool; primarily useful for observing the format decoding or detailed tracebacks
* messages; Array of strings representing messages logged by the spdx/tools-python parsers with the value of each key indicating the number of times a message occurred*  
(* Location information in the message like file path or line number was stripped)  

## What's next?
* Rebuild the parser tool from scratch...
