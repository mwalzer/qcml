# Introduction #

The control of metrics via a controlled vocabulary is quite forward. A controlled vocabulary entry can describe both experimental as well as programmatic environmental variables. It is comprised of a name, a identifier, a definition and associated relations. The latter makes the CV  hierarchical structurable.

# Details #

Here is an example of what a cv term looks like:
```
[Term]
 id: QC:0000039
 name: delta ppm
 def: "The deviation of the precursor ion mass and the theoretical mass of the matched identification." [PXS:QC]
 relationship: has_units UO:0000169 ! parts per million
 is_a: QC:0000025 ! MS identification result details
```
The qualitative description of mass deviation is called _delta ppm_ and runs under the identifier _QC:0000039_. It is subordinate to the comprising term of _MS identification result details_ and has the unit _parts per million_.

## Quality parameter control ##

A _quality parameter_ has cv elements built in that will describe his type and alike. The cv structure is called cv param type and all it's attributes will be directly built in the _quality parameter_.

Basically, a _quality parameter_ will look like that:
```
<QualityParameter name="MS1 spectra count" ID="20100219_SvNa_SA_Ecoli_PP_ms1aquisition" cvRef="QC" accession="QC:0000006" value="4536"/>
```

The _name_ attribute is the name of the cv term chosen for this _quality parameter_, the _ID_ attribute is a file wide unique identifier that will make it easier to hold the many different _quality parameter\_s contained in a file apart. The_accession_attribute is the cv terms accession within its vocabulary. The_cvRef_attribute gives back a link to the vocabulary from which the cv term stems from. Lastly, the_value_attribute contains the value this\_quality parameter_ holds for the given cv term, in this case the amount of MS1 spectra contained in the respective run.

As you can see from the schema below, a _quality parameter\_s can hold more cv control than the example above with optional attributes. These are indicated by the dashed boxes. You can control the unit of the associated value by giving a suitable cv term triplet of_name_,_accession_and_reference_from a vocabulary containing unit cv terms.
For example
```
... unitAccession="UO:0000169" unitName="parts per million" unitCvRef="UO" ...
```
from the [unit ontology](http://www.ebi.ac.uk/ontology-lookup/?termId=UO:0000169).
As you can see from the schema the value attribute is also optional, as for some_quality parameter_it just suffices, that it is present._

![http://qcml.googlecode.com/svn/trunk/schema/qcml_qp.png](http://qcml.googlecode.com/svn/trunk/schema/qcml_qp.png)