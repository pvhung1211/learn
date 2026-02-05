https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows

```yml
name: test
	on: push
	# or multiple events
	# on: [push, workflow_dispatch]
```

- Repository related
	- push
	- fork
	- pull_request (opened, closed, ...)
	- issues (opened, deleted, ...)
	- disscustion(created, deleted, ...)
	- create (tag, ...)
	- issue_comment
	- ...

- Other
	- workflow_dispatch (manually trigger)
	- repository_dispatch (trigger via a API request)
	- schedule (workflow is scheduled)
	- workflow_call (called by other workflows)