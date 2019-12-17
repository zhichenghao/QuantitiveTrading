# The Open University’s repository of research publications and other research outputs, 2009

## Abstract
A  model-driven translation approach etween semantic web service based business process models in the context of the SUPER project.
	- provide a set of business process ontologies for enabling access to the business process space inside the organization at the semantic level.
	- handle the translation between the ontologies in order to navigate from different views at the business views to IT views at the execution level.

## 1. Introduction

**1.1 Busines Process Management**: provide process modelling languages and tools to faciliate bridging between the business and IT views

- obtacle: business expert perspective to the actual implementation is not accesible at the semantic level and neither to machine reasoning.
- sollition: use of ontologies and Semantic Web Services(SWS) to provide a unified view on business process in a machine understandable way.

**1.2 SBPM**: provide a set of integrated ontologies developed in [WSML](https://www.w3.org/Submission/WSML/)

- provide ontologies for standards (e.g. BPMN, EPC, BPEL) and Business Process Modelling Ontology
- goal: support BPM lif-cycle activities at the semantic level (modelling, querying, translation and execution)
- tasks: handling the translations between the provided ontologies in order to navigate from different views at the busienss level to the IT at the excution level

**1.3**:model-driven approach
- implement translator for transforming instances of BPMO to instences of the ontology for BPEL
- implements mappings using [ATL rules](https://wiki.eclipse.org/ATL/User_Guide_-_The_ATL_Language) and XML format of [WSML](https://en.wikipedia.org/wiki/Web_Services_Modeling_Language) as both source and target models of the ATL transformation engine
-reuslt: semantically annotated executable business process model.


