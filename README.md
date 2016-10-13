# ZTF marshal

### Introduction

ZTF marshal will be the primary portal for partners and public in general to view, 
analyze, and collaborate objects of interests discovered in the ZTF survey. The
primary goal of this marshal is a container to collect information for each object 
of interest.

### Policies

#### Programming language
Marshal will be primarily written in Python 2.7. When necessary, C should be 
used to speed up applications.

#### Coding style
In order for better communication and maintenance, we strictly implement 
[https://google.github.io/styleguide/pyguide.html][the Google coding style].
Code review will also be implemented for quality.

#### Version control
An internal git repository will be set up soon. The master branch should always
be the deliverable version and the dev branch will be the HEAD of the development.
Every participant should create their own branch based on the dev HEAD and merge
their branch to dev once the code is accepted by the reviewer. The dev and master
branches can only be merged when the dev version is fully tested.

### APIs

The base class ZTFMarshal will have the following abstract APIs: 
 1. Create: create an object of interest by coordinates;
 2. Request: request existing data or follow-up data for a given object of interest;
 3. Add: add relevant data to each object of interest;
 4. Output: output relevant data of a given object upon request. 

The base class will have two subclasses: CMDMarshal and WebMarshal which provides
detailed APIs for end users. The exact formats of these APIs will be determined
shortly.

### High-level issues

Three high-level should be discussed and finalized soon. 
 1. User system and corresponding privileges.
 2. Database type and schema: given the heterogeneity of incoming data, a non-relational
 database might be more appropriate. Plus the fact that there will be little connection
 between two objects of interest, a database like MongoDB seems appropriate. 
 3. Web interface design: this should be done in CSS files.
