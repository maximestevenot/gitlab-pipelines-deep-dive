## only/except

only and except are two parameters that set a job policy to limit when jobs are created:

    1. only defines the names of branches and tags for which the job will run.
    2. except defines the names of branches and tags for which the job will not run.

There are a few rules that apply to the usage of job policy:

    1. only and except are inclusive. If both only and except are defined in a job specification, the ref is filtered by only and except.
    2. only and except allow the use of regular expressions (supported regexp syntax).
    3. only and except allow to specify a repository path to filter jobs for forks.