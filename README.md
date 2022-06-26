# LREC22_MetaEval_Tutorial
This repository share the material for LREC22 tutorial "Meta-Evaluation of Translation Evaluation Methods: a systematic up-to-date overview"

A Link to **download our tutorial** draft PPT slides (will be updated after tutorial) https://drive.google.com/drive/folders/1sajkcrnDgTOFiYVkFjYqh9EDYUhneYqA?usp=sharing 

A Group Photo link from our tutorial https://drive.google.com/drive/folders/1ll70UZ2jxivSYhE5S1yFKwAJ9FhvgYtt?usp=sharing 

| Content |
|---|

# Human evaluation methods

## Traditional Human Evaluation

Traditional human evaluation methods of quality of machine translation have been developed for many years and this field has been developed very extensively. There are also new developments on-going.

Here is the list of methods with their brief summary.

### ALPAC report
Description: seminal work on measuring translation quality.
Computers in Translation and Linguistics, a report by the Automatic Language Processing Advisory Committee (ALPAC), Publication 1416, National Academy of Sciences, National Research Council, Washington, D.C., 1966

Report: https://nap.nationalacademies.org/read/9547/chapter/1

### LISA QA Model
Description: Developed by LISA (Localization and Internationalization Standards Association)
Explainatory presentation: http://www.qt21.eu/launchpad/sites/default/files/QTLP%20GALA%20Webinar%203.pdf

### MQM 1.0
Description: MQM 1.0 was developed as deliverable of EU QT21 project.
Definitions: http://www.qt21.eu/mqm-definition/definition-2015-12-30.html
Issue Types: http://www.qt21.eu/mqm-definition/issues-list-2015-12-30.html
Latest version of issue types (MQM Core, see below): https://www.w3.org/community/mqmcg/2018/10/04/draft-2018-10-04/

### SAE J2450
The workgroup: https://www.sae.org/standardsdev/j2450p1.htm<br>
The MT Summit VII paper: Deploying the SAE J2450 Translation Quality Metric in MT Projects
https://aclanthology.org/1999.mtsummit-1.41.pdf

### ATA Translation Certification Program
Description: ATA translation certification program features a very interesting and robust translation quality evaluation metric

Described in: Welcome to the Real World: Professional-Level Translator Certification
The International Journal of Translation and Interpreting Research, 2013
By [Geoff Koby](https://kentstate.academia.edu/GeoffreyKoby)

Additional info: https://www.atanet.org/translation/summary-of-defining-translation-quality/

### TAUS DQF
Description: MQM-like metric.
Evolved out of the QT21/QTLaunchpad projects managed amongst others by DFKI.

References: https://www.taus.net/resources/blog/category/dynamic-quality-framework<br>

Now discontinued. Incorporated in MQM Core

### MQM Core

Many users may be familiar with the historical antecedents of the current MQM Core error typology.
The typology is based on the earlier TAUS system, DQF/MQM, which evolved out of the QT21/QTLaunchpad projects managed amongst others by DFKI.
Some changes appear in the top-level dimensions (where DQF-Fluency is now Linguistic conventions, and DQF-Verity has become Audience Appropriateness. Refinements in the typology deemed these designators to be more transparent to most users. See the TheMQM webpage for further explanations. These changes were agreed upon in collaboration with TAUS, and ISO 5060.<br>
https://www.w3.org/community/mqmcg/2018/10/04/draft-2018-10-04/

### MQM 2.0 (ASTM WK46396) Analytic Evaluation of Translation Quality
The latest version of Multidimensional Quality Framework.

The work item: www.astm.org/workitem-wk46396
More detailed information: https://themqm.org/

### HQuest (ASTM WK54484) - holistic system for measuring translation quality
The work item: https://www.astm.org/workitem-wk54884

### ISO/DIS 5060 - Translation services — Evaluation of translation output — General guidance
The work item: https://www.iso.org/standard/80701.html

## Advanced Human Evaluation methods

With the advent of neural machine translation new human evaluation methods have emerged:

### HOPE: A Task-Oriented and Human-Centric Evaluation Framework Using Professional Post-Editing Towards More Effective MT Evaluation

Description: human metric to quickly assess quality of MT.

Reference: https://arxiv.org/abs/2112.13833

## Evaluating Multi-word Expression (MWE) MT Quality

MWEs play bottleneck in many NLP tasks. MWEs have a broad covery including idioms, metophors, and fixed/semi-fixed patterns.

### AlphaMWE: Construction of Multilingual Parallel Corpora with MWE Annotations. 
AlphaMWE: https://github.com/poethan/AlphaMWE 
 In Proceedings of the Joint Workshop on Multiword Expressions and Electronic Lexicons, pages 44–57, online. Association for Computational Linguistics.


# Automatic evaluation methods

## BLEU
BLEU computes the precision for n-gram of size 1-to-4 with the coefficient of brevity penalty. The theory under this design is that if most of the outputs are right but with too short output (e.g. many meanings of the source sentences lost), then the precision value may be very high but this is not a good translation; the brevity-penalty coefficient will decrease the final score to balance this phenomenon.

First publication: https://aclanthology.org/P02-1040.pdf

## hLEPOR (LEngth penalty, Precision, n-gram pOsition difference penalty and Recall)

First publication: https://arxiv.org/ftp/arxiv/papers/1703/1703.08748.pdf

## COMET (Crosslingual Optimized Metric for Evaluation of Translation)
COMET is designed to learn to predict human judgments of MT quality. It does this by using a neural system to first map the MT-generated translation, the reference translation and the source language text into neural meaning representations. It then leverages these representations in order to learn to predict a quality score that is explicitly optimized for correlation with human judgments of translation quality. 

https://resources.unbabel.com/blog/why-we-believe-high-quality-machine-translation-really-is-possible

## cushLEPOR: customised hLEPOR metric using Optuna for higher agreement with human judgments or pre-trained language model LaBSE
Customised hLEPOR (cushLEPOR) uses Optuna hyper-parameter optimisation framework to fine-tune hLEPOR weighting parameters towards better agreement to pre-trained language models (using LaBSE) regarding the exact MT language pairs that cushLEPOR is deployed to. cushLEPOR metric can be file tuned to correlate with other metrics; in this work authors optimize it towards professional human evaluation.

First publication: https://arxiv.org/abs/2108.09484

## Classification of automatic methods of translation quality evaluation

- N-gram Word Surface Similarity
- Syntax and Semantics
- Statistical Eval and Deep Learning Based Eval 
- Reference-dependent vs Reference-free (QE)

## Meta Evaluation of translation quality metrics

- Eval Model Credibility
- Sample Size Confidentiality 
- Agreement Measuring
- Correlations between AutoEval and HumanEval


| Speakers |
|---|

**Lifeng Han**

- Post-doctoral Research Associate in UoM
- PhD gradauted from ADAPT Research Centre, DCU. Thesis 'An investigation into multi-word expressions in machine translation' https://doras.dcu.ie/26559 
- MSc in Software Engineering, thesis in MT Eval (LEPOR, hLEPOR, nLEPOR) with Excellent Award from UM. Thesis <LEPOR: An Augmented Machine Translation Evaluation Metric> https://arxiv.org/abs/1703.08748 
- BSc in Math from HNU of China
- Reserach topics: Machine Translation, Evaluation, Information Extraction, Linguistics Aware NLP 
- Google Scholar page (https://scholar.google.com/citations?hl=en&user=_vf3E2QAAAAJ&view_op=list_works)


**Serge Gladkoff**

- CEO of Logrus Global (LSP) https://logrusglobal.com 
- Head of R&D of Logrus Global AI Lab http://ai-lab.logrusglobal.com/blog/
- Technical contact of ASTM WK4636 standard
- ISO ANSI expert from United States
- ResearchGate page: https://www.researchgate.net/profile/Serge-Gladkoff/research

| References |
|---|

**Survey and Overview**

- Han and Wong (2016): Machine Translation Evaluation: A Survey https://arxiv.org/abs/1605.04515 (updated in 2018 ->)
- Lifeng Han (2018) Machine Translation Evaluation Resources and Methods: A Survey https://arxiv.org/abs/1605.04515v8
- Han et al. (2021) Translation Quality Assessment: A Brief Survey on Manual and Automatic Methods. https://aclanthology.org/2021.motra-1.3/ 
- Lifeng Han (2022) An Overview on Machine Translation Evaluation. https://arxiv.org/abs/2202.11027 (in Chinese, English update forthcoming)

**HumanEval Metrics**

- S Gladkoff, L Han (2022) HOPE: A Task-Oriented and Human-Centric Evaluation Framework Using Professional Post-Editing Towards More Effective MT Evaluation. LREC22. arXiv preprint arXiv:2112.13833
- Lifeng Han, Gareth Jones, and Alan Smeaton. 2020. AlphaMWE: Construction of Multilingual Parallel Corpora with MWE Annotations. In Proceedings of the Joint Workshop on Multiword Expressions and Electronic Lexicons, pages 44–57, online. Association for Computational Linguistics. https://aclanthology.org/2020.mwe-1.6/ 

**Auto-eval and QE**
- Lifeng Han, Irina Sorokina, Gleb Erofeev, Serge Gladkoff (2021) cushLEPOR: customising hLEPOR metric using Optuna for higher agreement with human judgments or pre-trained language model LaBSE. WMT21. https://aclanthology.org/2021.wmt-1.109/ 
- Gleb Erofeev, Irina Sorokina, Lifeng Han, Serge Gladkoff (2021) cushLEPOR uses LABSE distilled knowledge to improve correlation with human translation evaluations https://aclanthology.org/2021.mtsummit-up.28/
- Lifeng Han. 2014. LEPOR: An Augmented Machine Translation Evaluation Metric. MSc Thesis. University of Macau, Macao. https://arxiv.org/abs/1703.08748
- Han et al. 2014. Unsupervised Quality Estimation Model for English to German Translation and Its Application in Extensive Supervised Evaluation. https://www.hindawi.com/journals/tswj/2014/760301/ Recent Advances in Information Technology (using n-gram for precision and recall)
- Han et al. 2013. Quality Estimation for Machine Translation Using the Joint Method of Evaluation Criteria and Statistical Modeling. WMT13. https://aclanthology.org/W13-2245.pdf
- Han et al. (2013) "Phrase Tagset Mapping for French and English Treebanks and Its Application in Machine Translation Evaluation”. GSCL2013. https://link.springer.com/content/pdf/10.1007/978-3-642-40722-2_13.pdf (Using syntactic phrase structure)
- Han et al. (2013) "Language-independent Model for Machine Translation Evaluation with Reinforced Factors" in MT Summit. https://aclanthology.org/2013.mtsummit-posters.3.pdf (Using POS)
- Han et al. 2012. LEPOR: A Robust Evaluation Metric for Machine Translation with Augmented Factors. COLING12. https://aclanthology.org/C12-2044.pdf

**Meta-eval and Confidence**

- S Gladkoff, I Sorokina, L Han, A Alekseeva (2022) Measuring Uncertainty in Translation Quality Evaluation (TQE). LREC22. arXiv preprint arXiv:2111.07699
https://arxiv.org/abs/2111.07699 

**older Presentations**

- from Motra2021: video link https://drive.google.com/drive/folders/1njFi9FyHp1mURN0_5DXW1ws6szwq2RMo?usp=sharing ppt slides link https://drive.google.com/drive/folders/15YQDJaWoKJZiStuaWXzz-2Y-KOW1Bozh?usp=sharing 
- 
 
 | Acknowledgement |
|---|

- We thank the feedback and discussion on this tutorial structure and presentation form NLP group in The University of Manchester, especially Viktor Schlegel, Nhung Nguen, Haifa, Tharindu, Abdullah, Laura. 
- We also thank the funding support from Uni of Manchester (via Prof Goran Nenadic's project) and previous funding from ADAPT Research Centre, DCU. A link to NLP at UniManchester https://www.cs.manchester.ac.uk/research/expertise/natural-language-processing/ and ADAPT https://www.adaptcentre.ie/ 
- We thank the tutorial attendees from LREC2022 for valuable discussion and feedback to this tutorial and our work.
