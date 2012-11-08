NER
===

Scripts for Named Entity Recognition data preparation. An attempt at replication of the experiments described in:

Nuno Freire, Jose Borbinha and Pável Calado (2012) An approach for Named Entity Recognition in Poorly Structured Data. Proceedings of the 9th Extended Semantic Web Conference (ESWC 2012), May 27 - 31 2012, Heraklion, Greece. 

Prerequisites
--

These scripts have been written and tested on Mac OS X, with perl 5.14.0, but should work in similar Linux/UNIX environments. Furthermore, the following perl modules were used:

- HTML::Entities
- Lingua::EN::Tokenizer::Offsets
- Encode
- Lingua::Wordnet
- Lingua::Wordnet::Analysis
- Geo::GeoNames
- XML::LibXML::SAX

As well as Wordnet version 3.0 ([http://wordnet.princeton.edu/wordnet/download/] ) 
After downloading Wordnet-3.0 and untarring in /usr/local find the perl file Lingua-Wordnet-0.74/scripts/convertdb.pl and run it. When asked "Where do you want these files saved? Say: /usr/local/WordNet-3.0/dict/ 
If you install WordNet in another directory, you will need to change line 34 in createFeatureInstances.pl to your WordNet installation directory.

The scripts are made to work on the annotated .xml files that were described in Freire et al. 2012, which you can find here: [http://web.ist.utl.pt/~nuno.freire/ner]
Basically, any other similar xml file will do, but then you need to adjust the createFeatureInstances.pl to work with different data elements. 

The easiest setup is to copy all scripts and files to the directory in which your xml files reside and run run.sh from the command line. This will take a while, so go have some tea. After that you can use your favourite machine learning tool (Weka, Mallet) to test the performance of these features. 

Good luck!
