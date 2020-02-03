# ValidCV™ by AyeAI™
```
(C) Copyright 2019-2020 Abhishek Choudhary, Dr Srija Katta
NOTICE: Covered by AyeAI SPL (see below). NO WARRANTY, and ZERO LIABILITY (Limited to INR 1/- only) 
WARNING: ValidCV records are public as of this writing and we cannot offer any form of protection
         Users are strictly forbidden from and advised against submitting personal information into
         the ValidCV records. Any inadvertent release of personal information will be deleted from
         the ValidCV records only if feasible and may involve significant costs that the user making
         such request has to bear. AyeAI or its affiliates do not control 3rd party hosted services
         and data passed onto such services by means of storage or communication whether directly or
         indirectly goes beyond the control of AyeAI and its affiliates. The users explictly waive any
         claims to damages from the usage of the ValidCV platform and associated mechanisms, methods
         and software and indemnify AyeAI and its affiliates, including the original authors, from
         any liability arising out of their actions. There is no guarantee to the accuracy of the data
         contained in these systems, platforms and repositories.
```

### ValidCV™ is a hyperledger / blockchain / GitOps ref [https://www.gitops.tech/] based open skills validation framework promulgated by AyeAI™ for use with AyeLearn™ and AyeVDI™ brand offerings.

ValidCV consists of a persistent repository (current workflows are based on git),
with process automation for evaluation of skill attainment mapped to standard
industrial classifications (as of current release based on ISIC).

Each subscribing offering from vendors may compose a skill certification based
on one or more ValidCV SKUs composed into their respective SKUs.

ValidCV SKU identity are under design deliberation and consist of the following schema
```
VCV.x.y.z.Industry-code.Domain-sku
```
Explanation:
```
VCV: Signature
x.y.z: Version
        x: YYYY
        y: MM
        z: Sequence number of release for the month
Industry-code: As of this writing, based on the ISIC classification
Domain-sku: Domain specific SKU which can mutate independently of the rest of the schema
```
Repository organization:
```
Top-level directory - vcv
1st level sub-directory - x.y.z corresponds to the version
2nd level sub-directory - industry-code
3rd level sub-directory - sku code based validation records
Each 3rd level sub-directory must contain validation automation tools
Description: TBD (TODO)
NOTICE: These schema may change without notice

tools - automation tools
```
# Internship projects
Each country given by the ISO 2 / 3 digit country code should be supported by the tools in this project.
Things to do
1. Identify existing standard statistics structure
2. Create statistics source and formatter
3. Create dataset exploring tools (gather open access data and link to closed or paid data)
4. Perform data analytics, apply SKHF / PoLPEST analysis
5. Define roadmap to singularity based on above
6. Create transalational automation for research in the domain
7. Iff interested in the domain of the statistics, go further into its researh (patents annd publications)
8. Create sustainable biz and operations models for the domain of the statistics towards greater glory for mankind
9. Most importantly, be legally, socially, and ethically correct. When in doubt ASK!

Potential number of projects.
'iso country codes' x 'statistics' x 'types of analysis' x 'acad / commercial'...
150+ x 100+ x 50+ x 2+ ...
### Millions of projects possible... in this simple definition of ValidCV!
### Get! Set! Go!


## Development notes
NOTE: These will be captured in OSTs
TODO: Intern projects TBD

1. For errors in source encoding go to the deepest level of first failure and fi schema

2. To refresh a statistics for a country code use the following construct
e.g. UN ISIC - 4 digit codes
```
sourcefrom http://bit.ly/validcv-ver-pplt ic un 4
```
e.g. INDIA NIC - 5 digit codes
```
sourcefrom http://bit.ly/validcv-ver-pplt ic in 5
```

### To enable support for a new country code
1. Find the source of economic activities, or other statstics, structure
e.g. Download WZ 2008 structure in CSV format from  https://www.klassifikationsserver.de/klassService/jsp/common/url.jsf?variant=wz2008&lang=EN (wz2008.zip) - also see UN ISIC example for CSV with 4 digit codes, and India NIC example for 5 digit codes

2. Unzip the wz2008.zip file and cat the contents of the structure file to stdout
e.g. Captured into an OST https://bit.ly/validcv-source-ic-de
```
sourcefrom https://bit.ly/validcv-source-ic-de
```

3. Now write a formatter that will convert the output in a format similar to ISIC CSV txt file
Note: In case the level lengths do not match up then the three field line may be used. 1 field lines
get appended to the respective README.md
e.g. The WZ 2008 formatter has been captured in the OST https://bit.ly/validcv-format-ic-de and may be used together with source OST as below
```
sourcefrom https://bit.ly/validcv-source-ic-de | sourcefrom https://bit.ly/validcv-format-ic-de
```

4. If the output from step 3 looks fine you can proceed with trying out the integration directly
e.g. Now try to execute the following command - any errors at this stage will need modifications in formatter,
or may point to a bug in the ValidCV libraries. For instance, we needed a few iterations to the get the WZ 2008 format
correct for the pipeline - had to adjust the initial tail to +14 instead of +10. 
```
sourcefrom http://bit.ly/validcv-ver-pplt ic de 5
```
TODO: RCA needed why that adjustment was needed, could be a bug!

Another example that works fine, but needs some debugging - unterminated string error that does not seem to affect end results (try your hands at fixing it before someone else does!)
e.g. Based on EU NACE codes
```
sourcefrom http://bit.ly/valdicv-source-ic-eu | sourcefrom http://bit.ly/validcv-format-ic-eu
```
Or, run the complete integration
```
sourcefrom http://bit.ly/validcv-ver-pplt ic eu 5
```

5. Beyond this you could try many other features and integrations available in AyeVDI and AyeAI for a complete 
cloud based AI and analytics experience. Do try our experimental "systhesis" feature. We aspire to take it to the 
point of custom "CEMs™ Neuromorphic Quantum Accelerator" - looking forward to your support and participation in the journey
to Singularity!

### WARNING: 
#### Please do not distribute any material where the Copyright information provided is not clear about the rights of distribution, or without permission where one is required. Users may be given directions to manually download the specific object on their own. This defeats automation, however, the original providers legal rights are maintained.

#### Please do not share any sensitive personal information. This project is experimntal and we cannot guarantee any compliance of data protection such as GDPR. As of now we are also unable to assure removal of personal data. Please rest assured this is topmost priority and is one of the first avenues of investment, endowment, funding or donation.

#### This is an experimental system and cannot guarantee any level of accuracy or SLA. The results may be inaccurate and must never be used for any critical or life saving purpose or for any economic activity. The users use this software at their own risk and indemnify the original authors against any losses incurred directly or indirectly by them or by any other 3rd party, including the loss of mental peace, as a result of using this software.

#### These warnings may not be removed from redistribution of this software, even if permitted by license, under any circumstances. These are to be treated as additional clauses to the license.

## Legal Notice
#### ValiCV™ is a trademark of Abhishek Choudhary and others carrying out business as AyeAI Consulting and allied groups in India and other countries.

#### The following lines till the end of this file may not be removed under any circumstances
```
# AYESEC:POST_SHS('18 lines')=9da1fc9afc1b85e1e81e78a53f97d4436d886182eec170ddd6c78ec71e64113d9ade4fd1bf969ed5bbe62baed9a575d2b5e3ccdc0383c27eb7a4b6bc71965afe
# AYESEC:STATUTORY_HEADER
if [ "${ayevdi_sourcefrom}" != "${HOME}/.ayevdi/ayevdi-sourcefrom" ]
then
  echo "AyeVDI by https://ayeai.xyz"
  echo "Copyright (C) 2019-2020 Abhishek Choudhary, Dr Srija Katta"
  echo ""
  echo "NO WARRANTY, and ZERO LIABILITY (Limited to INR 1/- only)"
  echo "Further usage of these software, artifacts or methods"
  echo "are subject to the 'latest' license agreement avaialble at"
  echo "https://raw.githubusercontent.com/ayeai/spl/master/LICENSE"
  echo ""
  echo "AyeVDI not activated. Please use the following command to"
  echo "activate AyeVDI"
  echo '  ayesh=$(tempfile) && wget https://bit.ly/ayevdi-sfrom-init -O${ayesh} -q && . ${ayesh}'
  echo ""
  exit
fi
# AYESEC:STATUTORY_HEADER_COMPLETED
# AYESEC:PREV_SHS('18 lines')=9da1fc9afc1b85e1e81e78a53f97d4436d886182eec170ddd6c78ec71e64113d9ade4fd1bf969ed5bbe62baed9a575d2b5e3ccdc0383c27eb7a4b6bc71965afe
```
