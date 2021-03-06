Overview
===========

.. contents::


This directory contains tools for scoring of the two sub challenges of NIEHS-NCATS-UNC DREAM Toxicogenetics Challenge. 


Subchallenge 1
-----------

**Challenge description:** Predict interindividual variability in in vitro cytotoxicity based on genomic profiles of individual cell lines. For each compound, participants will be challenged to predict the absolute values and relative ranks of cytotoxicity across a set of unknown cell lines for which genomic data is available. 

The template for scoring is provided within this synapse https://www.synapse.org/#!Synapse:syn1917708 page. 

For further information on the subchallenge and on the submission format go to https://www.synapse.org/#!Wiki:syn1761567/ENTITY/55909 

For details on the scoring metrics go to https://www.synapse.org/#!Wiki:syn1761567/ENTITY/60497.


Subchallenge 2
-----------

**Challenge description:** For each compound, predict the concentration at which median cytotoxicity would occur, as well as inter-individual variation in cytotoxicity, described by the 5-95th%ile range, across the population. Each prediction will be scored based on the participant’s ability to predict these two parameters within a set of compounds excluded from the training set. 

For further information on the subchallenge and on the submission format go to https://www.synapse.org/#!Wiki:syn1761567/ENTITY/55911 

For details on the scoring metrics go to https://www.synapse.org/#!Wiki:syn1761567/ENTITY/60498.

Scoring
---------

From the dreamtools package, you can score a submission from the D8C1 first sub challenge as follows:

::

  from dreamtools.dream8.D8C2 import sc1
  s = sc1.D8C1_sc1(filename)
  s.run()
  # results are stored in s.df 
  s.df


Note that the computation takes a few minutes. The computation for the sub-challenge 2 is much faster and works similalrly::

  from dreamtools.dream8.D8C2 import sc2
  s = sc2.D8C1_sc2(filename)
  s.run()
  # results are stored in s.df 
  s.df


Examples of submission files can be found in the source code (e.g., data/test_sc1.csv)




