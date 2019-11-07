## Importance of Quality Gates

Pipeline design is critical as the artifacts produced in one stage become the inputs for the next.
Eventually they are pushed to production environment.
Thorough tests should be performed before the code is deployed in the production environment
Absence of gates may result in vulnerable ,corrupted,defected code in production environment.
Therefore the code is tested on UAT and Integration environment. Post successful run on staging environments it becomes production ready.

The Quality gates implemented by CICD are:
`static-acceptance` stage:
### unit-tests
Testing individual units/ components of a software
### dependency-check
Identifies project dependencies and checks if there are any known, publicly disclosed vulnerabilities
### secret-scan
Scan file or a folder recursively to look for secrets
### license-finder
Find dependencies, detect the licenses of the packages in them, compare those licenses against a user-defined whitelist, and give you an actionable exception report.

## For Docker Images
### container-scanning (anchore engine)
Check your Docker images (or more precisely the containers) for known vulnerabilities