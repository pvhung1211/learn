- Define a Runner (execution environment)
```yml
jobs:
	first-job:
	runs-on: ubuntu-latest
```

- Contain one or more [[Steps]]
```yml
  first-job:
    runs-on: ubuntu-latest
    steps:
      - name: Print Hello
        run: echo "Hello"
      - name: Print Goodbye
        run: echo "Bye"
```

- Run in parallel (default) or sequential
- Can run under certain conditions