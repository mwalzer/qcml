This project develops and implements a data exchange format geared towards capturing
quality control (QC) data from high-throughput biology experiments. The current focus
of the project is towards mass spectrometry based proteomics, but the format is suitable
for metabolomics and next-generation sequencing as well.

The format itself is designed to hold quality control data (numbers, texts and images) in either single elements or tabular format, each classified by controlled vocabulary terms, associating it with a QC metric, unit or type.
It is built to sort the data according to the inherent design of every scientific experiment:
  * single runs of a experiment (with different settings or as replications)
  * sets of runs consolidating certain settings

As an open format, it can be used to plug in new analyses or methods as well as established ones. It is not fixed to a single QC tool or suite.
As such it can capture QC data all along the way of scientific research. By the tools used or the application of their resulting files - from raw data acquisition, over analysis and reporting to storage in repositories and databases.

![http://qcml.googlecode.com/svn/trunk/website-images/Alternate%20qcml%20implementation%20zoo.png](http://qcml.googlecode.com/svn/trunk/website-images/Alternate%20qcml%20implementation%20zoo.png)

Several  software tools able to handle qcML are already available:

  * [OpenMS](http://www.OpenMS.de) provides tools for calculation proteomics and metabolomics QC data as well as a parser and writer for qcML (C++)
  * [jqcML](https://bitbucket.org/proteinspector/jqcml/wiki/Home#) provides a parser/writer for qcML in Java
  * [SympatiQCo](http://ms.imp.ac.at/?goto=simpatiqco) provides export of its QC data as qcML


[OpenMS](http://www.OpenMS.de) is also integrated into [KNIME ](http://www.knime.org/) allowing for easy graphical workflow and report generation. Have a look at [how the QC workflows are done with KNIME](QCWorkflowsInKNIME.md) or jump directly to the [examples](ExampleKNIMEworkflows.md). The datasets used in the publication can be found [here](http://genesis.ugent.be/files/costore/qcml/)

<img src='http://qcml.googlecode.com/svn/trunk/website-images/qc_workflow_knime.png' alt='knimeworkflow' />

KNIME also permits the construction of reporting workflows. Its [WYSIWYG](http://en.wikipedia.org/wiki/WYSIWYG) editor makes constructing tailor-made QC workflows as simple as typing a document in Microsoft Word. An example of such a QC report in PDF format can be seen [here](http://qcml.googlecode.com/svn/trunk/example/report.pdf).


The quality metrics you can capture with qcML are controlled by a  [controlled vocabulary](http://code.google.com/p/qcml/source/browse/trunk/cv/qc-cv.obo). If you have a suggestion for a new metric, feel free to make a suggestion via [submit metric entry](http://code.google.com/p/qcml/issues/entry) or drop us an email.
If you want to know more about how it's done have a look at [QCMetricControlByCV](QCMetricControlByCV.md).



qcML is supported by: [![](http://qcml.googlecode.com/svn/trunk/website-images/primexs.png)](http://www.primexs.eu/)   [![](http://open-ms.sourceforge.net/wp-content/themes/light-clean-blue/images/openms-logo.png)](http://www.OpenMS.de)