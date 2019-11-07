The Quality gates implemented by CICD for spring applications are:

- **unit-tests**: Testing individual units/ components of a software
- **dependency-check**: Identifies project dependencies and checks if there are any known, publicly disclosed vulnerabilities
- **secret-scan**: Scan file or a folder recursively to look for secrets
- **license-finder**: Find dependencies, detect the licenses of the packages in them, compare those licenses against a user-defined whitelist, and give you an actionable exception report.

And for docker images: **container-scanning** (anchore engine) checks your Docker images (or more precisely the containers) for known vulnerabilities