# ZTF marshal

### Introduction

ZTF marshal will be the primary portal for partners and public in general to view, 
analyze, and collaborate objects of interests discovered in the ZTF survey. The
primary goal of this marshal is a container to collect information for each object 
of interest.

### Required functions

1. Create an object of interest by coordinates;
 2. Automatically retrieve existing ZTF data for objects of interest;
 3. Collecting information of existing objects of interest from external catalogs and alerts;
 4. Send alerts for objects of interest;
 5. Request follow-up observations;
 6. Include photometric and spectroscopic data for objects of interest;
 7. Allow users to comment w/ or w/o attachment;
 8. Perform basic searches by time, coordinates, etc..
 9. Optional anxillary functions: 
    1. Object visibility; 
    2. Provide finding charts;
    3. Preparing follow-up observing runs.

### High-level issues

The following high-level issues should be determined for marshal: 
 1. User privilege systems: maybe we can use the same Linux user system (user/group/all).
    But this needs discussion from the top level.
 2. Database type and schema: considering the heterogeneity of data and little
    connection between different objects, a non-relational database might be more
    appropriate, for example, MongoDB.
 3. Web interface design.

### Hardware requirements

TBD

### Implementation details

#### Programming languages

1. Marshal will be primarily written in Python 2.7. 
 2. When necessary, C should be used for speed-up.
 3. Web desgin should be done in CSS. 

#### Coding styles

In order for better communication and maintenance, we strictly implement 
[https://google.github.io/styleguide/pyguide.html][the Google coding style].
Code review will also be implemented for quality.

#### Version control

An internal git repository will be set up soon. The master branch should always
be the deliverable version and the dev branch will be the HEAD of the development.
Every participant should create their own branch based on the dev HEAD and merge
their branch to dev once the code is accepted by the reviewer. The dev and master
branches can only be merged when the dev version is fully tested.

#### Classes and APIs

TBD
