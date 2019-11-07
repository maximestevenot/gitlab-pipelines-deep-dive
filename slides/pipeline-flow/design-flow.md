## Importance of Quality Gates

Pipeline design is critical as the artifacts produced in one stage become the inputs for the next.
Eventually they are pushed to production environment.
Thorough tests should be performed before the code is deployed in the production environment
Absence of gates may result in vulnerable ,corrupted,defected code in production environment.
Therefore the code is tested on UAT and Integration environment. Post successful run on staging environments it becomes production ready.
