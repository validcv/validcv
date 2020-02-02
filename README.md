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
         indirectly goes beyond the control of AyeAI and its affiliates. The users eplictly waive any
         claims to damages from the usage of the ValidCV platform and associated mechanisms, methods
         and software and indemnify AyeAI and its affiliates, including the original authors, from
         any liability arising out of their actions. There is no guarantee to the accuracy of the data
         contained in these systems, platforms and repositories.
```

ValidCV™ is a hyperledger / blockchain based open skills validation framework
promulgated by AyeAI™ for use with AyeLearn™ and AyeVDI™ brand offerings.

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

## Development notes
NOTE: These will be captured in OSTs
TODO: Intern projects TBD

1. For errors in source encoding go to the deepest level of first failure and fi schema

## Legal Notice
ValiCV™ is a trademark of Abhishek Choudhary and others 
carrying out business as AyeAI Consulting and allied 
groups in India and other countries.

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
