---
layout: entry
title: "Protein_molecule"
shortdef: "Protein molecule (GENIA)"
order: 31
---

The name of this entity group is based on the <a href="http://www.nactem.ac.uk/meta-knowledge/">GENIA-Meta-knowledge corpus</a> at <a href="http://www.nactem.ac.uk/">NaCTeM</a>.

<!--
This entity is based on 
<a href="https://www.uniprot.org/">UniProt</a> database and <a href="https://pir.georgetown.edu/pro/"> PIR ontology</a>.
-->

The definition of 'Anatomical_entity' is based on the Semantic types of 
- 'aapp' (Amino Acid, Peptide, or Protein), 
- 'enzy' (Enzyme),
- 'rcpt' (Receptor), 
- 'horm' (Hormone)

in the <a href="https://www.nlm.nih.gov/research/umls/">UMLS database</a>.
However, some data of UMLS 'horm' might be for [Organic_compound_other]().

Protein molecules, gene products, are categorized into this entity group.

~~~ ann
Patients with high MMP-9 levels.
T1 Subject 0 8 Patients
T2 Protein_molecule 19 24 MMP-9
~~~

~~~ ann
matrix metalloproteinase 9 (MMP-9), myeloperoxidase (MPO), and arginase 1 (ARG1)
T1 Protein_molecule 0 26 matrix metalloproteinase 9
T2 Protein_molecule 28 33 MMP-9
T3 Protein_molecule 36 51 myeloperoxidase
T4 Protein_molecule 53 56 MPO
T5 Protein_molecule 63 73 arginase 1
T6 Protein_molecule 75 79 ARG1
R1 is_equivalent Arg1:T2 Arg2:T1
R2 is_equivalent Arg1:T4 Arg2:T3
R3 is_equivalent Arg1:T6 Arg2:T5
~~~

<!-- details -->
