# ChEMBL-based-training-set
This repo holds the code and description of the process of training set formation to build classifiers aiming to be useful for preclinical safety assessemnt of medical drug's active substances.

## In short:

Preclinical safety assessment is a complex process allowing one to be reasonably sure that the drug being developed is good enough to be evaluated in humans for its ability to be safe and useful in clinical practice.
Corresponding research area is quite large and important.
One of the key directions is the developement of assays, which endpoints could predict the degree of safety for a drug substance in humans.
Main problem is that, as far as I know, there is no single ideal model of the human organism, which can be used to assess all of the risks.
Thus, the whole process becomes complex (multi-staged and branched) and resource consuming ivolving the usage of multuple models corresponding to the different level of organisation (animals, cells, biomacromolecules, etc.).
Unfortunately, despite all this complexity and resources, preclinical assessement does not provide 100 % guarantee that the drug will be safe in clinic.
Estimating the exact number of cases when drug fails in clinical trials because of the safety issues is also hard, and there is a number of reasons for that,
one of them is that safety depends on efficacy; and I will not comment more on this topic here; have no doubt only in that: there are cases when drug candidates fail because of the safety issues.
So, when things get complicated - simple solutions are needed and the idea is as follows:
The most of the drugs are useful for the treatment because they modulate somehow the activity of an important, in the context of the disease being treated, biomolecule(s) in human body.
From this, one can assume that potential drug may have safety issues because it modulates some other biomolecules, which are important for maintaining normal body functioning.
From this, to predict safety of the drug, it is enough to assess the whole spectrum of its interactions with biomolecules in human body and know, which of them needs to be modulated to achieve therapeutic effect (therapeutic targets)
and which of them should be left intact to avoid safety issues.
Such an approach has limitations:
- lists of therapeutic targets and targets associated with the safety issues are intersected, e.g.:
  Affecting hERG channel (https://en.wikipedia.org/wiki/KCNH2) leads to arrythmia and is the reason why several drugs were de-marketed,
  at the same time hERG channel is the therapeutic target for such a drug as ibutilid (https://www.ebi.ac.uk/chembl/explore/compound/CHEMBL533) using to treat specific variant of arrythmia.
- our ability to assess interactions between the drugs' active substances and biomolecules in in vitro experiments is still limited.
Thus, in the course of this project it was decided to study ways to mitigate this limitations using computer prediction:
- conceptual problem of selecting targets related to the potential safety issues may be solved via allowing to predict interactions with all human targets for which training data are available, marking those present in various lists and allowing users to exclude target or several targets from the results of prediction.
- computer prediction is by itself the way to mitigate some of the limitations of experimental studies: time, money, materials (not to replace experimental studies in general, this is distinct topic).
Latter the results of prediction could be compared in groups of successful drugs and drugs, which development have been terminated not like it was described in

[Поройков В. В. и др. Оценка безопасности фармакологически активных веществ in silico c применением методов машинного обучения: обзор //Безопасность и риск фармакотерапии. – 2023. – Т. 11. – №. 4. – С. 372-389.]

on example of prediction of adverse and toxic effects.

Important step is to prepare the training set.

Licences, lincs and some other necessary elements will be added.
