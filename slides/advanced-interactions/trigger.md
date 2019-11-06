## trigger

trigger allows you to define downstream pipeline trigger. When a job created from trigger definition is started by GitLab, a downstream pipeline gets created.

Note: Using a trigger with when:manual together results in the error jobs:#{job-name} when should be on_success, on_failure or always, because when:manual prevents triggers being used.