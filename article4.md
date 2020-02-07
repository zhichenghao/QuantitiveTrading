# Translating Semantic Web Service Based Business Process Models

## Abstract

- handle the translations between the ontologies to navigate from different views a the business level to the IT view at the execution level
- transforms instances of BPMO to instances of sBPEL

## 1 Introduction
- main obstacle of BPM: business process space inside the organization, from the business expert perspective to the actual implementation is widely not accessible at the semantic level and thus neither to machin reasoing.
- semantic business process management reserach area address this problem and propose the use of ontologies and semantic web service to provide a unified view on business process in a machine understandable way.

## 2 Business Process Ontologies
- main ontolog: BPMO
	- import UPO (Upper-level Process Ontology)
	- sEPC and sBPMN semantically annotate the correspoding standard notations used to model process workflows at the business level
	- SBPEL is an ontologies for the BPEL language which is used by IT experts
	- translation between BPMO and sBPEL
		- use the unambiguous meaning of constrcuts in the ontologies

### 2.1 BPMO
- BPMO: is an ontology for high-level business process woekflow models, abstracring from existing business process notations
- workflow elements of the BPMO process diagram comply with a correspoding subset of BPMN control flow elements and named according to workflow patterns
- BPMO concepts related to interaction activities adopt a number of web servie attributes also used in BPEL constructs
- BPMO process description captures the business context of the modelled process and contains the process workflow which represents the behaviour of the process and process activities. 
	- process itself can also have a corresponding Web Service description
	- the concepts related to semantic Web Service in BPMO are GoalTask, Receive, send and ReceiveMessage Event which are subconcepts of Tasks.
	- tasks have attributes to represent information about the interaction with a partner process

### 2.2 SBPEL
- SBPEL is a langugae for specifying the compositio of Wen Services using a conroslflow based approach.
	- control-flow constructes are structured activities or basic activities including assign and interaction activities: links(dependencies) between activities wtihin a flow (parallel execution) activity in a graph-based style 
	- add interaction and converstion extention sonstructs

## Translation Approach
- BPMO2SBPEL translator: transforms between instances of a BPMO models and sBPEL model
	- input: WSML file containing BPMO instances of individual business process
	- output: WSML file contain conrrespoding sBPEL file
	- use WSMO4J API to parse and serialize XML versions of WSML




## Translation Example

## related work